---
title: Azure PowerShell’i kullanmaya başlama
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 61d6d19336dd0e1885570c3a4e8874a849317fa3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2020
ms.locfileid: "75722433"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="7bf2e-102">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="7bf2e-102">Get started with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="7bf2e-103">Azure PowerShell, Azure kaynaklarını komut satırından yönetmek ve Azure Resource Manager’da çalışacak otomasyon betikleri oluşturmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="7bf2e-104">Bunu [Azure Cloud Shell](/azure/cloud-shell/overview) ile tarayıcınızda kullanabilir veya yerel makinenize yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="7bf2e-105">Bu makale Azure PowerShell'i kullanmaya başlamanıza yardımcı olur ve bu ürünün ardındaki temel kavramları öğretir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="7bf2e-106">Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="7bf2e-106">Install Azure PowerShell</span></span>

<span data-ttu-id="7bf2e-107">İlk adım, Azure PowerShell’in en son sürümünü yüklediğinizden emin olmaktır.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="7bf2e-108">En son sürüm hakkında bilgi edinmek için [sürüm notlarına](./release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="7bf2e-109">[Azure PowerShell'i yükleme](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="7bf2e-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="7bf2e-110">Yüklemenin başarılı olduğunu doğrulamak için, komut satırınızdan `Get-InstalledModule AzureRM -AllVersions` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-110">To verify the installation was successful, run `Get-InstalledModule AzureRM -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="7bf2e-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="7bf2e-111">Azure Cloud Shell</span></span>

<span data-ttu-id="7bf2e-112">Başlamanın en kolay yolu [Cloud Shell’i başlatmaktır](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="7bf2e-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="7bf2e-113">Cloud Shell’i Azure portalında en üst gezinti bölmesinden başlatın.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell simgesi](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="7bf2e-115">Kullanmak istediğiniz aboneliği seçin ve bir depolama hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![Depolama hesabı oluşturma](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="7bf2e-117">Depolama alanınız oluşturulduktan sonra Cloud Shell, tarayıcıda bir PowerShell oturumu açar.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![PowerShell için Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="7bf2e-119">Ayrıca Azure PowerShell yükleyip bir PowerShell oturumunda yerel olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="7bf2e-120">Azure'da oturum açma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-120">Sign in to Azure</span></span>

<span data-ttu-id="7bf2e-121">Etkileşimli olarak oturum açın:</span><span class="sxs-lookup"><span data-stu-id="7bf2e-121">Sign on interactively:</span></span>

1. <span data-ttu-id="7bf2e-122">`Connect-AzureRmAccount` yazın.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="7bf2e-123">Azure kimlik bilgilerinizi isteyen bir iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-123">You'll get a dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="7bf2e-124">'-Environment' seçeneğini kullanarak Azure Çin veya Azure Almanya için kimlik doğrulaması yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-124">Option '-Environment' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="7bf2e-125">Örneğin: Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="7bf2e-125">for example, Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="7bf2e-126">Hesabınızla ilişkili e-posta adresini ve parolayı yazın.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="7bf2e-127">Azure, kimlik bilgilerini doğrulayıp kaydeder ve pencereyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="7bf2e-128">Bir Azure hesabında oturum açtıktan sonra, Azure PowerShell cmdlet'lerini kullanarak aboneliğinizdeki kaynaklara erişebilir ve bunları yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="7bf2e-129">Basit varsayılanları kullanarak Windows sanal makinesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="7bf2e-130">`New-AzureRmVM` cmdlet’i yeni sanal makine oluşturmayı kolaylaştıran, basitleştirilmiş bir söz dizimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="7bf2e-131">Sağlamanız gereken yalnızca iki parametre değeri vardır: VM’nin adı ve VM’deki yerel yönetici hesabının kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="7bf2e-132">İlk olarak kimlik bilgisi nesnesini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="7bf2e-133">Sonra VM’yi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-133">Next, create the VM.</span></span>

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

<span data-ttu-id="7bf2e-134">Başka nelerin oluşturulduğunu ve VM’nin nasıl yapılandırıldığını merak ediyor olabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-134">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="7bf2e-135">İlk olarak, kaynak gruplarımıza bakalım.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-135">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="7bf2e-136">**cloud-shell-storage-westus** kaynak grubu, Cloud Shell’i ilk kez kullandığınızda oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-136">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="7bf2e-137">**SampleVM** kaynak grubu `New-AzureRmVM` cmdlet’i tarafından oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-137">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="7bf2e-138">Bu yeni kaynak grubunda başka hangi kaynaklar oluşturuldu?</span><span class="sxs-lookup"><span data-stu-id="7bf2e-138">Now, what other resources were created in this new resource group?</span></span>

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

<span data-ttu-id="7bf2e-139">VM hakkında daha fazla bilgi edinelim.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-139">Let's get some more details about the VM.</span></span> <span data-ttu-id="7bf2e-140">Bu örnek, VM oluşturmak için kullanılan İşletim Sistemi Görüntüsü hakkında nasıl bilgi alınacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-140">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

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

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="7bf2e-141">Tam olarak yapılandırılmış bir Linux Sanal Makinesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-141">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="7bf2e-142">Önceki örnekte, Windows sanal makinesi oluşturmak için basitleştirilmiş söz dizimi ve varsayılan parametre değerleri kullanıldı.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-142">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="7bf2e-143">Bu örnekte, sanal makinenin tüm seçenekler için değerler sunuyoruz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-143">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="7bf2e-144">Kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-144">Create a resource group</span></span>

<span data-ttu-id="7bf2e-145">Bu örnekte, bir Kaynak Grubu oluşturmak istiyoruz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-145">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="7bf2e-146">Azure’daki Kaynak Grupları, mantıksal olarak bir araya getirmek istediğiniz birden çok kaynağı yönetmek için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-146">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="7bf2e-147">Örneğin, uygulama veya proje için bir Kaynak Grubu oluşturup, bunu içine bir sanal makine, veritabanı ve CDN hizmeti ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-147">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="7bf2e-148">Azure’un westeurope bölgesinde "MyResourceGroup" adlı bir kaynak grubu oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-148">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="7bf2e-149">Bunu yapmak için aşağıdaki komutu yazın:</span><span class="sxs-lookup"><span data-stu-id="7bf2e-149">To do so type the following command:</span></span>

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

<span data-ttu-id="7bf2e-150">Bu yeni kaynak grubu, oluşturduğumuz yeni VM için gereken tüm kaynakları kapsayacak şekilde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-150">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="7bf2e-151">Yeni bir Linux VM oluşturmak için önce diğer gerekli kaynakları oluşturup bir yapılandırmaya atamamız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-151">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="7bf2e-152">Daha sonra, bu yapılandırmayı kullanarak VM’yi oluşturabiliriz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-152">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="7bf2e-153">Ayrıca, kullanıcı profilinizin .ssh dizininde `id_rsa.pub` adlı bir SSH genel anahtarınız da olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-153">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="7bf2e-154">Gerekli ağ kaynaklarını oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-154">Create the required network resources</span></span>

<span data-ttu-id="7bf2e-155">İlk olarak, sanal ağ oluşturma işleminde kullanılacak bir alt ağ yapılandırması oluşturmamız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-155">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="7bf2e-156">Bu VM’ye bağlanabilmek için genel bir IP adresi de oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-156">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="7bf2e-157">Genel adrese erişimin güvenliğini sağlamak için bir ağ güvenlik grubu oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-157">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="7bf2e-158">Son olarak, önceki kaynakların tamamını kullanarak sanal NIC’yi oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-158">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-vm-configuration"></a><span data-ttu-id="7bf2e-159">VM yapılandırmasını oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-159">Create the VM configuration</span></span>

<span data-ttu-id="7bf2e-160">Gerekli kaynaklara sahip olduğumuza göre artık VM yapılandırması nesnesini oluşturabiliriz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-160">Now that we have the required resources we can create the VM configuration object.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="7bf2e-161">Sanal makineyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-161">Create the virtual machine</span></span>

<span data-ttu-id="7bf2e-162">Artık VM yapılandırması nesnesini kullanarak VM’yi oluşturabiliriz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-162">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="7bf2e-163">Artık VM oluşturulduğundan, bu VM’nin genel IP adresiyle SSH’yi kullanarak yeni Linux VM’nizde oturum açabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7bf2e-163">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="7bf2e-164">Azure'da diğer kaynakları oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-164">Creating other resources in Azure</span></span>

<span data-ttu-id="7bf2e-165">Buraya kadar size Kaynak Grubu, Linux VM ve Windows Server VM’nin nasıl oluşturulduğu gösterdik.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-165">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="7bf2e-166">Birçok başka türde Azure kaynağı da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-166">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="7bf2e-167">Örneğin, yeni oluşturduğumuz VM’lerle ilişkilendirebileceğimiz bir Azure Ağ Yük Dengeleyicisi oluşturmak için, aşağıdaki create komutu kullanabiliriz:</span><span class="sxs-lookup"><span data-stu-id="7bf2e-167">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="7bf2e-168">Ayrıca, aşağıdaki komutu kullanarak altyapımız için yeni bir özel Sanal Ağ (Azure’da adı çoğunlukla "VNet" olarak geçer) oluşturabiliriz:</span><span class="sxs-lookup"><span data-stu-id="7bf2e-168">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="7bf2e-169">Azure’u ve Azure PowerShell’i güçlü kılan, bunları yalnızca bulut tabanlı bir altyapı elde etmek için değil yönetilen platform hizmetleri oluşturmak için de kullanabilmemizdir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-169">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="7bf2e-170">Daha güçlü çözümler oluşturmak için yönetilen platform hizmetleri ile altyapı da birleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-170">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="7bf2e-171">Örneğin, Azure PowerShell’i kullanarak bir Azure Uygulama Hizmeti oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-171">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="7bf2e-172">Azure Uygulama Hizmeti, altyapı konusunda kaygılanmadan web uygulamalarını barındırmak için harika bir yol sağlayan bir yönetilen platform hizmetidir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-172">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="7bf2e-173">Azure Uygulama Hizmetini oluşturduktan sonra, aşağıdaki komutları kullanarak Uygulama Hizmetinin içinde iki yeni Azure Web Uygulaması oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="7bf2e-173">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="7bf2e-174">Dağıtılan kaynakları listeleme</span><span class="sxs-lookup"><span data-stu-id="7bf2e-174">Listing deployed resources</span></span>

<span data-ttu-id="7bf2e-175">Azure’da çalışmakta olan kaynakları listelemek için `Get-AzureRmResource` cmdlet’ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-175">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="7bf2e-176">Aşağıdaki örnekte, yeni kaynak grubunda oluşturduğumuz kaynaklar gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-176">The following example shows the resources we created in the new resource group.</span></span>

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

## <a name="deleting-resources"></a><span data-ttu-id="7bf2e-177">Kaynakları silme</span><span class="sxs-lookup"><span data-stu-id="7bf2e-177">Deleting resources</span></span>

<span data-ttu-id="7bf2e-178">Azure hesabınızı temizlemek için bu örnekte oluşturduğumuz kaynakları kaldırmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-178">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="7bf2e-179">Artık ihtiyacınız olmayan kaynakları silmek için `Remove-AzureRm*` cmdlet’lerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-179">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="7bf2e-180">Oluşturduğumuz Windows VM’yi kaldırmak için aşağıdaki komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="7bf2e-180">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="7bf2e-181">Kaynağı kaldırmak istediğinizi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-181">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="7bf2e-182">Bir kerede birçok kaynağı da silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-182">You can also delete many resources at once.</span></span> <span data-ttu-id="7bf2e-183">Örneğin, aşağıdaki komut, tüm örnekler için kullandığımız "MyResourceGroup" adlı kaynak grubunu siler.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-183">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="7bf2e-184">Gruptaki tüm kaynaklar da silinir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-184">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="7bf2e-185">Kaynakların sayısına ve türüne bağlı olarak bu görevin tamamlanması birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-185">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="7bf2e-186">Örnekleri alın</span><span class="sxs-lookup"><span data-stu-id="7bf2e-186">Get samples</span></span>

<span data-ttu-id="7bf2e-187">Azure PowerShell’i kullanmanın yolları hakkında daha fazla bilgi edinmek için [Linux VM’ler](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VM’ler](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) ve [SQL Veritabanları](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)’na yönelik en yaygın betiklerimizi inceleyin.</span><span class="sxs-lookup"><span data-stu-id="7bf2e-187">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="7bf2e-188">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="7bf2e-188">Next steps</span></span>

* [<span data-ttu-id="7bf2e-189">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-189">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="7bf2e-190">Azure PowerShell ile Azure aboneliklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="7bf2e-190">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="7bf2e-191">Azure PowerShell’i kullanarak Azure’da hizmet sorumluları oluşturma</span><span class="sxs-lookup"><span data-stu-id="7bf2e-191">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="7bf2e-192">Eski bir sürümden geçişle ilgili olarak sürüm notlarını okuyun: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="7bf2e-192">Read the release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="7bf2e-193">Topluluktan yardım alın:</span><span class="sxs-lookup"><span data-stu-id="7bf2e-193">Get help from the community:</span></span>
  * [<span data-ttu-id="7bf2e-194">MSDN'deki Azure forumu</span><span class="sxs-lookup"><span data-stu-id="7bf2e-194">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="7bf2e-195">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="7bf2e-195">stackoverflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
