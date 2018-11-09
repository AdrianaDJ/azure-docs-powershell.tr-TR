---
title: Azure PowerShell’i kullanmaya başlama | Microsoft Docs
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 11/15/2017
ms.openlocfilehash: 7eb5e3fad31b5a92be1cfb36aefdaa7b920bae5f
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211035"
---
# <a name="getting-started-with-azure-powershell"></a>Azure PowerShell’i kullanmaya başlama

Azure PowerShell, Azure kaynaklarını komut satırından yönetmek ve Azure Resource Manager’da çalışacak otomasyon betikleri oluşturmak için tasarlanmıştır. [Azure Cloud Shell](/azure/cloud-shell/overview) ile tarayıcınızda kullanabilir veya yerel makinenize yükleyip herhangi bir PowerShell oturumunda kullanabilirsiniz. Bu makale, Azure CLI 2.0’ı kullanmaya başlamanıza yardımcı olur ve bunun ardındaki temel kavramları öğretir.

## <a name="connect"></a>Bağlan

Başlamanın en kolay yolu [Cloud Shell’i başlatmaktır](/azure/cloud-shell/quickstart).

1. Cloud Shell’i Azure portalında en üst gezinti bölmesinden başlatın.

   ![Shell simgesi](~/media/get-started-azureps/shell-icon.png)

2. Kullanmak istediğiniz aboneliği seçin ve bir depolama hesabı oluşturun.

   ![Depolama hesabı oluşturma](~/media/get-started-azureps/storage-prompt.png)

Depolama alanınız oluşturulduktan sonra Cloud Shell, tarayıcıda bir PowerShell oturumu açar.

![PowerShell için Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

Ayrıca Azure PowerShell yükleyip bir PowerShell oturumunda yerel olarak kullanabilirsiniz.

## <a name="install-azure-powershell"></a>Azure PowerShell'i yükleme

İlk adım, Azure PowerShell’in en son sürümünü yüklediğinizden emin olmaktır. En son sürüm hakkında bilgi edinmek için [sürüm notlarına](./release-notes-azureps.md) bakın.

1. [Azure PowerShell'i yükleme](install-azurerm-ps.md).

2. Yüklemenin başarılı olduğunu doğrulamak için, komut satırınızdan `Get-Module AzureRM -ListAvailable` komutunu çalıştırın.

## <a name="sign-in-to-azure"></a>Azure'da oturum açma

Etkileşimli olarak oturum açın:

1. `Login-AzureRmAccount` yazın. Azure kimlik bilgilerinizi isteyen bir iletişim kutusu açılır. '-EnvironmentName' seçeneğini kullanarak Azure Çin veya Azure Almanya için kimlik doğrulaması yapabilirsiniz.

   Örneğin: Login-AzureRmAccount -EnvironmentName AzureChinaCloud

2. Hesabınızla ilişkili e-posta adresini ve parolayı yazın. Azure, kimlik bilgilerini doğrulayıp kaydeder ve pencereyi kapatır.

Bir Azure hesabında oturum açtıktan sonra, Azure PowerShell cmdlet'lerini kullanarak aboneliğinizdeki kaynaklara erişebilir ve bunları yönetebilirsiniz.

## <a name="create-a-resource-group"></a>Kaynak grubu oluşturma

Artık her şeyi ayarladığımıza göre, şimdi de Azure PowerShell’i kullanarak Azure içinde kaynaklar oluşturabiliriz.

İlk önce bir Kaynak Grubu oluşturun. Azure’daki Kaynak Grupları, mantıksal olarak bir araya getirmek istediğiniz birden çok kaynağı yönetmek için bir yol sağlar. Örneğin, uygulama veya proje için bir Kaynak Grubu oluşturup, bunu içine bir sanal makine, veritabanı ve CDN hizmeti ekleyebilirsiniz.

Azure’un westeurope bölgesinde "MyResourceGroup" adlı bir kaynak grubu oluşturalım. Bunu yapmak için aşağıdaki komutu yazın:

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a>Windows Sanal Makinesi oluşturma

Artık kaynak grubumuz olduğuna göre, şimdi de bu grubun içinde bir Windows sanal makinesi oluşturalım. Yeni bir VM oluşturmak için önce diğer gerekli kaynakları oluşturup bir yapılandırmaya atamamız gerekir. Daha sonra, bu yapılandırmayı kullanarak VM’yi oluşturabiliriz.

### <a name="create-the-required-network-resources"></a>Gerekli ağ kaynaklarını oluşturma

İlk olarak, sanal ağ oluşturma işleminde kullanılacak bir alt ağ yapılandırması oluşturmamız gerekir. Bu VM’ye bağlanabilmek için genel bir IP adresi de oluştururuz. Genel adrese erişimin güvenliğini sağlamak için bir ağ güvenlik grubu oluştururuz. Son olarak, önceki kaynakların tamamını kullanarak sanal NIC’yi oluştururuz.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Sanal makineyi oluşturma

Öncelikle işletim sistemi için bir kimlik bilgileri kümesine ihtiyacımız vardır.

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

Artık gerekli kaynaklara sahip olduğumuza göre, VM’yi oluşturabiliriz. Bu adım için bir VM yapılandırma nesnesi oluşturur, sonra da bu yapılandırmayı kullanarak VM’yi oluştururuz.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

VM tümüyle oluşturulduğunda ve kullanıma hazır olduğunda, `New-AzureRmVM` komutu sonuçları çıkarır.

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

Şimdi, Uzak Masaüstü’nü ve VM’nin genel IP adresini kullanarak yeni oluşturduğunuz Windows Server VM’de oturum açın. Aşağıdaki komut, önceki betikte oluşturulan genel IP adresini görüntüler.

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

Windows tabanlı bir sistemdeyseniz, bunu komut satırından mstsc komutunu kullanarak gerçekleştirebilirsiniz:

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

Oturum açmak için, VM’yi oluştururken kullandığınız kullanıcı adı/parola bileşimini sağlayın.

## <a name="create-a-linux-virtual-machine"></a>Linux Sanal Makinesi oluşturma

Yeni bir Linux VM oluşturmak için önce diğer gerekli kaynakları oluşturup bir yapılandırmaya atamamız gerekir. Daha sonra, bu yapılandırmayı kullanarak VM’yi oluşturabiliriz. Burada, kaynak grubunu zaten daha önce gösterildiği gibi oluşturduğunuz varsayılır. Ayrıca, kullanıcı profilinizin .ssh dizininde `id_rsa.pub` adlı bir SSH genel anahtarınız da olmalıdır.

### <a name="create-the-required-network-resources"></a>Gerekli ağ kaynaklarını oluşturma

İlk olarak, sanal ağ oluşturma işleminde kullanılacak bir alt ağ yapılandırması oluşturmamız gerekir. Bu VM’ye bağlanabilmek için genel bir IP adresi de oluştururuz. Genel adrese erişimin güvenliğini sağlamak için bir ağ güvenlik grubu oluştururuz. Son olarak, önceki kaynakların tamamını kullanarak sanal NIC’yi oluştururuz.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>Sanal makineyi oluşturma

Artık gerekli kaynaklara sahip olduğumuza göre, VM’yi oluşturabiliriz. Bu adım için bir VM yapılandırma nesnesi oluşturur, sonra da bu yapılandırmayı kullanarak VM’yi oluştururuz.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Artık VM oluşturulduğuna göre, bu VM’nin genel IP adresiyle SSH’yi kullanarak yeni Linux VM’nizde oturum açabilirsiniz:

```bash
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a>Azure'da diğer kaynakları oluşturma

Buraya kadar size Kaynak Grubu, Linux VM ve Windows Server VM’nin nasıl oluşturulduğu gösterdik. Birçok başka türde Azure kaynağı da oluşturabilirsiniz.

Örneğin, yeni oluşturduğumuz VM’lerle ilişkilendirebileceğimiz bir Azure Ağ Yük Dengeleyicisi oluşturmak için, aşağıdaki oluşturma komutunu kullanabiliriz:

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Ayrıca, aşağıdaki komutu kullanarak altyapımız için yeni bir özel Sanal Ağ (Azure’da adı çoğunlukla "VNet" olarak geçer) oluşturabiliriz:

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Azure’u ve Azure PowerShell’i güçlü kılan, bunları yalnızca bulut tabanlı bir altyapı elde etmek için değil yönetilen platform hizmetleri oluşturmak için de kullanabilmemizdir. Daha güçlü çözümler oluşturmak amacıyla, yönetilen platform hizmetleri ile altyapı da birleştirilebilir.

Örneğin, Azure PowerShell’i kullanarak bir Azure Uygulama Hizmeti oluşturabilirsiniz. Azure Uygulama Hizmeti, altyapı konusunda kaygılanmadan web uygulamalarını barındırmak için harika bir yol sağlayan bir yönetilen platform hizmetidir. Azure Uygulama Hizmetini oluşturduktan sonra, aşağıdaki komutları kullanarak Uygulama Hizmetinin içinde iki yeni Azure Web Uygulaması oluşturabilirsiniz:

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Dağıtılan kaynakları listeleme

Azure’da çalışmakta olan kaynakları listelemek için `Get-AzureRmResource` cmdlet’ini kullanabilirsiniz. Aşağıdaki örnekte, yeni kaynak grubunda biraz önce oluşturduğumuz kaynaklar gösterilmektedir.

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a>Kaynakları silme

Azure hesabınızı temizlemek için bu örnekte oluşturduğumuz kaynakları kaldırmak istersiniz. Artık ihtiyacınız olmayan kaynakları silmek için `Remove-AzureRm*` cmdlet’lerini kullanabilirsiniz. Oluşturduğumuz Windows VM’yi kaldırmak için aşağıdaki komutu kullanın:

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Kaynağı kaldırmak istediğinizi onaylamanız istenir.

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Birçok kaynağı tek seferde silme seçeneğini de kullanabilirsiniz. Örneğin, aşağıdaki komut, bu Başlangıç öğreticisindeki tüm örnekler için kullandığımız "MyResourceGroup" adlı kaynak grubunu tamamen siler. Bu komut, kaynak grubunu ve gruptaki tüm kaynakları kaldırır.

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Bu işlemin tamamlanması birkaç dakika sürebilir.

## <a name="get-samples"></a>Örnekleri edinin

Azure PowerShell’i kullanmanın yolları hakkında daha fazla bilgi edinmek için [Linux VM’ler](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VM’ler](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) ve [SQL Veritabanları](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)’na yönelik en yaygın betiklerimizi inceleyin.

## <a name="next-steps"></a>Sonraki adımlar

* [Azure PowerShell ile oturum açma](authenticate-azureps.md)
* [Azure PowerShell ile Azure aboneliklerini yönetme](manage-subscriptions-azureps.md)
* [Azure PowerShell’i kullanarak Azure’da hizmet sorumluları oluşturma](create-azure-service-principal-azureps.md)
* Eski bir sürümden geçiş ile ilgili olarak Sürüm notlarını okuyun: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Topluluktan yardım alın:
  * [MSDN'deki Azure forumu](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
