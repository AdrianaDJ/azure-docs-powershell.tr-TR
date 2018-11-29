---
title: Azure PowerShell’i kullanmaya başlama
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 09/11/2018
ms.openlocfilehash: 5378cdb9d70aa0d2dc617d06d3c887ec20eb7767
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/29/2018
ms.locfileid: "52587100"
---
# <a name="get-started-with-azure-powershell"></a>Azure PowerShell’i kullanmaya başlama

Azure PowerShell, Azure kaynaklarını komut satırından yönetmek ve Azure Resource Manager’da çalışacak otomasyon betikleri oluşturmak için tasarlanmıştır. Bunu [Azure Cloud Shell](/azure/cloud-shell/overview) ile tarayıcınızda kullanabilir veya yerel makinenize yükleyebilirsiniz. Bu makale Azure PowerShell'i kullanmaya başlamanıza yardımcı olur ve bu ürünün ardındaki temel kavramları öğretir.

## <a name="install-azure-powershell"></a>Azure PowerShell'i yükleme

İlk adım, Azure PowerShell’in en son sürümünü yüklediğinizden emin olmaktır. En son sürüm hakkında bilgi edinmek için [sürüm notlarına](./release-notes-azureps.md) bakın.

1. [Azure PowerShell'i yükleme](install-azurerm-ps.md).

2. Yüklemenin başarılı olduğunu doğrulamak için, komut satırınızdan `Get-Module AzureRM -ListAvailable` komutunu çalıştırın.

## <a name="azure-cloud-shell"></a>Azure Cloud Shell

Başlamanın en kolay yolu [Cloud Shell’i başlatmaktır](/azure/cloud-shell/quickstart).

1. Cloud Shell’i Azure portalında en üst gezinti bölmesinden başlatın.

   ![Shell simgesi](~/media/get-started-azureps/shell-icon.png)

2. Kullanmak istediğiniz aboneliği seçin ve bir depolama hesabı oluşturun.

   ![Depolama hesabı oluşturma](~/media/get-started-azureps/storage-prompt.png)

Depolama alanınız oluşturulduktan sonra Cloud Shell, tarayıcıda bir PowerShell oturumu açar.

![PowerShell için Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

Ayrıca Azure PowerShell yükleyip bir PowerShell oturumunda yerel olarak kullanabilirsiniz.

## <a name="sign-in-to-azure"></a>Azure'da oturum açma

Etkileşimli olarak oturum açın:

1. `Connect-AzureRmAccount` yazın. Azure kimlik bilgilerinizi isteyen bir iletişim kutusu açılır. '-Environment' seçeneğini kullanarak Azure Çin veya Azure Almanya için kimlik doğrulaması yapabilirsiniz.

   Örneğin: Connect-AzureRmAccount -Environment AzureChinaCloud

2. Hesabınızla ilişkili e-posta adresini ve parolayı yazın. Azure, kimlik bilgilerini doğrulayıp kaydeder ve pencereyi kapatır.

Bir Azure hesabında oturum açtıktan sonra, Azure PowerShell cmdlet'lerini kullanarak aboneliğinizdeki kaynaklara erişebilir ve bunları yönetebilirsiniz.

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a>Basit varsayılanları kullanarak Windows sanal makinesi oluşturma

`New-AzureRmVM` cmdlet’i yeni sanal makine oluşturmayı kolaylaştıran, basitleştirilmiş bir söz dizimi sağlar. Sağlamanız gereken yalnızca iki parametre değeri vardır: VM’nin adı ve VM’deki yerel yönetici hesabının kimlik bilgileri.

İlk olarak kimlik bilgisi nesnesini oluşturun.

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

Sonra VM’yi oluşturun.

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

Başka nelerin oluşturulduğunu ve VM’nin nasıl yapılandırıldığını merak ediyor olabilirsiniz. İlk olarak, kaynak gruplarımıza bakalım.

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

**cloud-shell-storage-westus** kaynak grubu, Cloud Shell’i ilk kez kullandığınızda oluşturulur. **SampleVM** kaynak grubu `New-AzureRmVM` cmdlet’i tarafından oluşturuldu.

Bu yeni kaynak grubunda başka hangi kaynaklar oluşturuldu?

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

VM hakkında daha fazla bilgi edinelim. Bu örnek, VM oluşturmak için kullanılan İşletim Sistemi Görüntüsü hakkında nasıl bilgi alınacağını gösterir.

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a>Tam olarak yapılandırılmış bir Linux Sanal Makinesi oluşturma

Önceki örnekte, Windows sanal makinesi oluşturmak için basitleştirilmiş söz dizimi ve varsayılan parametre değerleri kullanıldı. Bu örnekte, sanal makinenin tüm seçenekler için değerler sunuyoruz.

### <a name="create-a-resource-group"></a>Kaynak grubu oluşturma

Bu örnekte, bir Kaynak Grubu oluşturmak istiyoruz. Azure’daki Kaynak Grupları, mantıksal olarak bir araya getirmek istediğiniz birden çok kaynağı yönetmek için bir yol sağlar. Örneğin, uygulama veya proje için bir Kaynak Grubu oluşturup, bunu içine bir sanal makine, veritabanı ve CDN hizmeti ekleyebilirsiniz.

Azure’un westeurope bölgesinde "MyResourceGroup" adlı bir kaynak grubu oluşturalım. Bunu yapmak için aşağıdaki komutu yazın:

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

Bu yeni kaynak grubu, oluşturduğumuz yeni VM için gereken tüm kaynakları kapsayacak şekilde kullanılır. Yeni bir Linux VM oluşturmak için önce diğer gerekli kaynakları oluşturup bir yapılandırmaya atamamız gerekir. Daha sonra, bu yapılandırmayı kullanarak VM’yi oluşturabiliriz. Ayrıca, kullanıcı profilinizin .ssh dizininde `id_rsa.pub` adlı bir SSH genel anahtarınız da olmalıdır.

#### <a name="create-the-required-network-resources"></a>Gerekli ağ kaynaklarını oluşturma

İlk olarak, sanal ağ oluşturma işleminde kullanılacak bir alt ağ yapılandırması oluşturmamız gerekir. Bu VM’ye bağlanabilmek için genel bir IP adresi de oluştururuz. Genel adrese erişimin güvenliğini sağlamak için bir ağ güvenlik grubu oluştururuz. Son olarak, önceki kaynakların tamamını kullanarak sanal NIC’yi oluştururuz.

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
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

### <a name="create-the-vm-configuration"></a>VM yapılandırmasını oluşturma

Gerekli kaynaklara sahip olduğumuza göre artık VM yapılandırması nesnesini oluşturabiliriz.

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a>Sanal makineyi oluşturma

Artık VM yapılandırması nesnesini kullanarak VM’yi oluşturabiliriz.

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

Artık VM oluşturulduğundan, bu VM’nin genel IP adresiyle SSH’yi kullanarak yeni Linux VM’nizde oturum açabilirsiniz:

```bash
ssh xx.xxx.xxx.xxx
```

```output
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

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

Ayrıca, aşağıdaki komutu kullanarak altyapımız için yeni bir özel Sanal Ağ (Azure’da adı çoğunlukla "VNet" olarak geçer) oluşturabiliriz:

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Azure’u ve Azure PowerShell’i güçlü kılan, bunları yalnızca bulut tabanlı bir altyapı elde etmek için değil yönetilen platform hizmetleri oluşturmak için de kullanabilmemizdir. Daha güçlü çözümler oluşturmak amacıyla, yönetilen platform hizmetleri ile altyapı da birleştirilebilir.

Örneğin, Azure PowerShell’i kullanarak bir Azure Uygulama Hizmeti oluşturabilirsiniz. Azure Uygulama Hizmeti, altyapı konusunda kaygılanmadan web uygulamalarını barındırmak için harika bir yol sağlayan bir yönetilen platform hizmetidir. Azure Uygulama Hizmetini oluşturduktan sonra, aşağıdaki komutları kullanarak Uygulama Hizmetinin içinde iki yeni Azure Web Uygulaması oluşturabilirsiniz:

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>Dağıtılan kaynakları listeleme

Azure’da çalışmakta olan kaynakları listelemek için `Get-AzureRmResource` cmdlet’ini kullanabilirsiniz. Aşağıdaki örnekte, yeni kaynak grubunda oluşturduğumuz kaynaklar gösterilir.

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
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

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

Kaynağı kaldırmak istediğinizi onaylamanız istenir.

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Bir kerede birçok kaynağı da silebilirsiniz. Örneğin, aşağıdaki komut, tüm örnekler için kullandığımız "MyResourceGroup" adlı kaynak grubunu siler.
Gruptaki tüm kaynaklar da silinir.

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Kaynakların sayısına ve türüne bağlı olarak bu görevin tamamlanması birkaç dakika sürebilir.

## <a name="get-samples"></a>Örnekleri alın

Azure PowerShell’i kullanmanın yolları hakkında daha fazla bilgi edinmek için [Linux VM’ler](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VM’ler](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) ve [SQL Veritabanları](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)’na yönelik en yaygın betiklerimizi inceleyin.

## <a name="next-steps"></a>Sonraki adımlar

* [Azure PowerShell ile oturum açma](authenticate-azureps.md)
* [Azure PowerShell ile Azure aboneliklerini yönetme](manage-subscriptions-azureps.md)
* [Azure PowerShell’i kullanarak Azure’da hizmet sorumluları oluşturma](create-azure-service-principal-azureps.md)
* Eski bir sürümden geçişle ilgili olarak sürüm notlarını okuyun: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).
* Topluluktan yardım alın:
  * [MSDN'deki Azure forumu](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](http://go.microsoft.com/fwlink/?LinkId=320213)
