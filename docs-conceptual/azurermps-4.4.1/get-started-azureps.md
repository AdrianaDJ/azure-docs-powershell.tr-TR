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
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/08/2018
ms.locfileid: "51273982"
---
# <a name="getting-started-with-azure-powershell"></a><span data-ttu-id="dc949-102">Azure PowerShell’i kullanmaya başlama</span><span class="sxs-lookup"><span data-stu-id="dc949-102">Getting started with Azure PowerShell</span></span>

<span data-ttu-id="dc949-103">Azure PowerShell, Azure kaynaklarını komut satırından yönetmek ve Azure Resource Manager’da çalışacak otomasyon betikleri oluşturmak için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="dc949-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="dc949-104">[Azure Cloud Shell](/azure/cloud-shell/overview) ile tarayıcınızda kullanabilir veya yerel makinenize yükleyip herhangi bir PowerShell oturumunda kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span> <span data-ttu-id="dc949-105">Bu makale, Azure CLI 2.0’ı kullanmaya başlamanıza yardımcı olur ve bunun ardındaki temel kavramları öğretir.</span><span class="sxs-lookup"><span data-stu-id="dc949-105">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

## <a name="connect"></a><span data-ttu-id="dc949-106">Bağlan</span><span class="sxs-lookup"><span data-stu-id="dc949-106">Connect</span></span>

<span data-ttu-id="dc949-107">Başlamanın en kolay yolu [Cloud Shell’i başlatmaktır](/azure/cloud-shell/quickstart).</span><span class="sxs-lookup"><span data-stu-id="dc949-107">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="dc949-108">Cloud Shell’i Azure portalında en üst gezinti bölmesinden başlatın.</span><span class="sxs-lookup"><span data-stu-id="dc949-108">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell simgesi](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="dc949-110">Kullanmak istediğiniz aboneliği seçin ve bir depolama hesabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dc949-110">Choose the subscription you want to use and create a storage account.</span></span>

   ![Depolama hesabı oluşturma](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="dc949-112">Depolama alanınız oluşturulduktan sonra Cloud Shell, tarayıcıda bir PowerShell oturumu açar.</span><span class="sxs-lookup"><span data-stu-id="dc949-112">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![PowerShell için Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="dc949-114">Ayrıca Azure PowerShell yükleyip bir PowerShell oturumunda yerel olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-114">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="dc949-115">Azure PowerShell'i yükleme</span><span class="sxs-lookup"><span data-stu-id="dc949-115">Install Azure PowerShell</span></span>

<span data-ttu-id="dc949-116">İlk adım, Azure PowerShell’in en son sürümünü yüklediğinizden emin olmaktır.</span><span class="sxs-lookup"><span data-stu-id="dc949-116">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="dc949-117">En son sürüm hakkında bilgi edinmek için [sürüm notlarına](./release-notes-azureps.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="dc949-117">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="dc949-118">[Azure PowerShell'i yükleme](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="dc949-118">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="dc949-119">Yüklemenin başarılı olduğunu doğrulamak için, komut satırınızdan `Get-Module AzureRM -ListAvailable` komutunu çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="dc949-119">To verify the installation was successful, run `Get-Module AzureRM -ListAvailable` from your command line.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="dc949-120">Azure'da oturum açma</span><span class="sxs-lookup"><span data-stu-id="dc949-120">Sign in to Azure</span></span>

<span data-ttu-id="dc949-121">Etkileşimli olarak oturum açın:</span><span class="sxs-lookup"><span data-stu-id="dc949-121">Sign on interactively:</span></span>

1. <span data-ttu-id="dc949-122">`Login-AzureRmAccount` yazın.</span><span class="sxs-lookup"><span data-stu-id="dc949-122">Type `Login-AzureRmAccount`.</span></span> <span data-ttu-id="dc949-123">Azure kimlik bilgilerinizi isteyen bir iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="dc949-123">You will get dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="dc949-124">'-EnvironmentName' seçeneğini kullanarak Azure Çin veya Azure Almanya için kimlik doğrulaması yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-124">Option '-EnvironmentName' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="dc949-125">Örneğin: Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="dc949-125">e.g. Login-AzureRmAccount -EnvironmentName AzureChinaCloud</span></span>

2. <span data-ttu-id="dc949-126">Hesabınızla ilişkili e-posta adresini ve parolayı yazın.</span><span class="sxs-lookup"><span data-stu-id="dc949-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="dc949-127">Azure, kimlik bilgilerini doğrulayıp kaydeder ve pencereyi kapatır.</span><span class="sxs-lookup"><span data-stu-id="dc949-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="dc949-128">Bir Azure hesabında oturum açtıktan sonra, Azure PowerShell cmdlet'lerini kullanarak aboneliğinizdeki kaynaklara erişebilir ve bunları yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manager the resources in your subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="dc949-129">Kaynak grubu oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-129">Create a resource group</span></span>

<span data-ttu-id="dc949-130">Artık her şeyi ayarladığımıza göre, şimdi de Azure PowerShell’i kullanarak Azure içinde kaynaklar oluşturabiliriz.</span><span class="sxs-lookup"><span data-stu-id="dc949-130">Now that we've got everything set up, let's use Azure PowerShell to create resources within Azure.</span></span>

<span data-ttu-id="dc949-131">İlk önce bir Kaynak Grubu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="dc949-131">First, create a Resource Group.</span></span> <span data-ttu-id="dc949-132">Azure’daki Kaynak Grupları, mantıksal olarak bir araya getirmek istediğiniz birden çok kaynağı yönetmek için bir yol sağlar.</span><span class="sxs-lookup"><span data-stu-id="dc949-132">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="dc949-133">Örneğin, uygulama veya proje için bir Kaynak Grubu oluşturup, bunu içine bir sanal makine, veritabanı ve CDN hizmeti ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-133">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="dc949-134">Azure’un westeurope bölgesinde "MyResourceGroup" adlı bir kaynak grubu oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="dc949-134">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="dc949-135">Bunu yapmak için aşağıdaki komutu yazın:</span><span class="sxs-lookup"><span data-stu-id="dc949-135">To do so type the following command:</span></span>

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

## <a name="create-a-windows-virtual-machine"></a><span data-ttu-id="dc949-136">Windows Sanal Makinesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-136">Create a Windows Virtual Machine</span></span>

<span data-ttu-id="dc949-137">Artık kaynak grubumuz olduğuna göre, şimdi de bu grubun içinde bir Windows sanal makinesi oluşturalım.</span><span class="sxs-lookup"><span data-stu-id="dc949-137">Now that we have our resource group, let's create a Windows VM within it.</span></span> <span data-ttu-id="dc949-138">Yeni bir VM oluşturmak için önce diğer gerekli kaynakları oluşturup bir yapılandırmaya atamamız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc949-138">To create a new VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="dc949-139">Daha sonra, bu yapılandırmayı kullanarak VM’yi oluşturabiliriz.</span><span class="sxs-lookup"><span data-stu-id="dc949-139">Then we can use that configuration to create the VM.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="dc949-140">Gerekli ağ kaynaklarını oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-140">Create the required network resources</span></span>

<span data-ttu-id="dc949-141">İlk olarak, sanal ağ oluşturma işleminde kullanılacak bir alt ağ yapılandırması oluşturmamız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc949-141">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="dc949-142">Bu VM’ye bağlanabilmek için genel bir IP adresi de oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="dc949-142">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="dc949-143">Genel adrese erişimin güvenliğini sağlamak için bir ağ güvenlik grubu oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="dc949-143">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="dc949-144">Son olarak, önceki kaynakların tamamını kullanarak sanal NIC’yi oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="dc949-144">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="dc949-145">Sanal makineyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-145">Create the virtual machine</span></span>

<span data-ttu-id="dc949-146">Öncelikle işletim sistemi için bir kimlik bilgileri kümesine ihtiyacımız vardır.</span><span class="sxs-lookup"><span data-stu-id="dc949-146">First we need a set of credentials for the OS.</span></span>

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

<span data-ttu-id="dc949-147">Artık gerekli kaynaklara sahip olduğumuza göre, VM’yi oluşturabiliriz.</span><span class="sxs-lookup"><span data-stu-id="dc949-147">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="dc949-148">Bu adım için bir VM yapılandırma nesnesi oluşturur, sonra da bu yapılandırmayı kullanarak VM’yi oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="dc949-148">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="dc949-149">VM tümüyle oluşturulduğunda ve kullanıma hazır olduğunda, `New-AzureRmVM` komutu sonuçları çıkarır.</span><span class="sxs-lookup"><span data-stu-id="dc949-149">The `New-AzureRmVM` command outputs results once the VM has been fully created and is ready to be used.</span></span>

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

<span data-ttu-id="dc949-150">Şimdi, Uzak Masaüstü’nü ve VM’nin genel IP adresini kullanarak yeni oluşturduğunuz Windows Server VM’de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="dc949-150">Now sign in to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM.</span></span> <span data-ttu-id="dc949-151">Aşağıdaki komut, önceki betikte oluşturulan genel IP adresini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="dc949-151">The following command displays the public IP address created in the previous script.</span></span>

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

<span data-ttu-id="dc949-152">Windows tabanlı bir sistemdeyseniz, bunu komut satırından mstsc komutunu kullanarak gerçekleştirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="dc949-152">If you are on a Windows-based system, you can do this from the command line using the mstsc command:</span></span>

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="dc949-153">Oturum açmak için, VM’yi oluştururken kullandığınız kullanıcı adı/parola bileşimini sağlayın.</span><span class="sxs-lookup"><span data-stu-id="dc949-153">Supply the same username/password combination you used when creating the VM to sign in.</span></span>

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="dc949-154">Linux Sanal Makinesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-154">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="dc949-155">Yeni bir Linux VM oluşturmak için önce diğer gerekli kaynakları oluşturup bir yapılandırmaya atamamız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc949-155">To create a new Linux VM we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="dc949-156">Daha sonra, bu yapılandırmayı kullanarak VM’yi oluşturabiliriz.</span><span class="sxs-lookup"><span data-stu-id="dc949-156">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="dc949-157">Burada, kaynak grubunu zaten daha önce gösterildiği gibi oluşturduğunuz varsayılır.</span><span class="sxs-lookup"><span data-stu-id="dc949-157">This assumes that you have already created the resource group as previously shown.</span></span> <span data-ttu-id="dc949-158">Ayrıca, kullanıcı profilinizin .ssh dizininde `id_rsa.pub` adlı bir SSH genel anahtarınız da olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="dc949-158">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

### <a name="create-the-required-network-resources"></a><span data-ttu-id="dc949-159">Gerekli ağ kaynaklarını oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-159">Create the required network resources</span></span>

<span data-ttu-id="dc949-160">İlk olarak, sanal ağ oluşturma işleminde kullanılacak bir alt ağ yapılandırması oluşturmamız gerekir.</span><span class="sxs-lookup"><span data-stu-id="dc949-160">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="dc949-161">Bu VM’ye bağlanabilmek için genel bir IP adresi de oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="dc949-161">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="dc949-162">Genel adrese erişimin güvenliğini sağlamak için bir ağ güvenlik grubu oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="dc949-162">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="dc949-163">Son olarak, önceki kaynakların tamamını kullanarak sanal NIC’yi oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="dc949-163">Finally we create the virtual NIC using all of the previous resources.</span></span>

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

### <a name="create-the-virtual-machine"></a><span data-ttu-id="dc949-164">Sanal makineyi oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-164">Create the virtual machine</span></span>

<span data-ttu-id="dc949-165">Artık gerekli kaynaklara sahip olduğumuza göre, VM’yi oluşturabiliriz.</span><span class="sxs-lookup"><span data-stu-id="dc949-165">Now that we have the required resources we can create the VM.</span></span> <span data-ttu-id="dc949-166">Bu adım için bir VM yapılandırma nesnesi oluşturur, sonra da bu yapılandırmayı kullanarak VM’yi oluştururuz.</span><span class="sxs-lookup"><span data-stu-id="dc949-166">For this step, we create a VM configuration object, then we use the configuration to create the VM.</span></span>

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

<span data-ttu-id="dc949-167">Artık VM oluşturulduğuna göre, bu VM’nin genel IP adresiyle SSH’yi kullanarak yeni Linux VM’nizde oturum açabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="dc949-167">Now that the VM has been created, you can log on to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

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

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="dc949-168">Azure'da diğer kaynakları oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-168">Creating other resources in Azure</span></span>

<span data-ttu-id="dc949-169">Buraya kadar size Kaynak Grubu, Linux VM ve Windows Server VM’nin nasıl oluşturulduğu gösterdik.</span><span class="sxs-lookup"><span data-stu-id="dc949-169">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="dc949-170">Birçok başka türde Azure kaynağı da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-170">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="dc949-171">Örneğin, yeni oluşturduğumuz VM’lerle ilişkilendirebileceğimiz bir Azure Ağ Yük Dengeleyicisi oluşturmak için, aşağıdaki oluşturma komutunu kullanabiliriz:</span><span class="sxs-lookup"><span data-stu-id="dc949-171">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="dc949-172">Ayrıca, aşağıdaki komutu kullanarak altyapımız için yeni bir özel Sanal Ağ (Azure’da adı çoğunlukla "VNet" olarak geçer) oluşturabiliriz:</span><span class="sxs-lookup"><span data-stu-id="dc949-172">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="dc949-173">Azure’u ve Azure PowerShell’i güçlü kılan, bunları yalnızca bulut tabanlı bir altyapı elde etmek için değil yönetilen platform hizmetleri oluşturmak için de kullanabilmemizdir.</span><span class="sxs-lookup"><span data-stu-id="dc949-173">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="dc949-174">Daha güçlü çözümler oluşturmak amacıyla, yönetilen platform hizmetleri ile altyapı da birleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="dc949-174">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="dc949-175">Örneğin, Azure PowerShell’i kullanarak bir Azure Uygulama Hizmeti oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-175">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="dc949-176">Azure Uygulama Hizmeti, altyapı konusunda kaygılanmadan web uygulamalarını barındırmak için harika bir yol sağlayan bir yönetilen platform hizmetidir.</span><span class="sxs-lookup"><span data-stu-id="dc949-176">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="dc949-177">Azure Uygulama Hizmetini oluşturduktan sonra, aşağıdaki komutları kullanarak Uygulama Hizmetinin içinde iki yeni Azure Web Uygulaması oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="dc949-177">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="dc949-178">Dağıtılan kaynakları listeleme</span><span class="sxs-lookup"><span data-stu-id="dc949-178">Listing deployed resources</span></span>

<span data-ttu-id="dc949-179">Azure’da çalışmakta olan kaynakları listelemek için `Get-AzureRmResource` cmdlet’ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-179">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="dc949-180">Aşağıdaki örnekte, yeni kaynak grubunda biraz önce oluşturduğumuz kaynaklar gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="dc949-180">The following example shows the resources we just created in the new resource group.</span></span>

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

## <a name="deleting-resources"></a><span data-ttu-id="dc949-181">Kaynakları silme</span><span class="sxs-lookup"><span data-stu-id="dc949-181">Deleting resources</span></span>

<span data-ttu-id="dc949-182">Azure hesabınızı temizlemek için bu örnekte oluşturduğumuz kaynakları kaldırmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-182">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="dc949-183">Artık ihtiyacınız olmayan kaynakları silmek için `Remove-AzureRm*` cmdlet’lerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-183">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="dc949-184">Oluşturduğumuz Windows VM’yi kaldırmak için aşağıdaki komutu kullanın:</span><span class="sxs-lookup"><span data-stu-id="dc949-184">To remove the Windows VM we created, using the following command:</span></span>

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="dc949-185">Kaynağı kaldırmak istediğinizi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="dc949-185">You will be prompted to confirm that you want to remove the resource.</span></span>

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="dc949-186">Birçok kaynağı tek seferde silme seçeneğini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="dc949-186">You can also use the delete many resources at one time.</span></span> <span data-ttu-id="dc949-187">Örneğin, aşağıdaki komut, bu Başlangıç öğreticisindeki tüm örnekler için kullandığımız "MyResourceGroup" adlı kaynak grubunu tamamen siler.</span><span class="sxs-lookup"><span data-stu-id="dc949-187">For example, the following command deletes all the resource group "MyResourceGroup" that we've used for all the samples in this Get Started tutorial.</span></span> <span data-ttu-id="dc949-188">Bu komut, kaynak grubunu ve gruptaki tüm kaynakları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="dc949-188">This removes the resource group and all of the resources in it.</span></span>

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="dc949-189">Bu işlemin tamamlanması birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="dc949-189">This can take several minutes to complete.</span></span>

## <a name="get-samples"></a><span data-ttu-id="dc949-190">Örnekleri edinin</span><span class="sxs-lookup"><span data-stu-id="dc949-190">Get samples</span></span>

<span data-ttu-id="dc949-191">Azure PowerShell’i kullanmanın yolları hakkında daha fazla bilgi edinmek için [Linux VM’ler](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VM’ler](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) ve [SQL Veritabanları](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)’na yönelik en yaygın betiklerimizi inceleyin.</span><span class="sxs-lookup"><span data-stu-id="dc949-191">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="dc949-192">Sonraki adımlar</span><span class="sxs-lookup"><span data-stu-id="dc949-192">Next steps</span></span>

* [<span data-ttu-id="dc949-193">Azure PowerShell ile oturum açma</span><span class="sxs-lookup"><span data-stu-id="dc949-193">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="dc949-194">Azure PowerShell ile Azure aboneliklerini yönetme</span><span class="sxs-lookup"><span data-stu-id="dc949-194">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="dc949-195">Azure PowerShell’i kullanarak Azure’da hizmet sorumluları oluşturma</span><span class="sxs-lookup"><span data-stu-id="dc949-195">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="dc949-196">Eski bir sürümden geçiş ile ilgili olarak Sürüm notlarını okuyun: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span><span class="sxs-lookup"><span data-stu-id="dc949-196">Read the Release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="dc949-197">Topluluktan yardım alın:</span><span class="sxs-lookup"><span data-stu-id="dc949-197">Get help from the community:</span></span>
  * [<span data-ttu-id="dc949-198">MSDN'deki Azure forumu</span><span class="sxs-lookup"><span data-stu-id="dc949-198">Azure forum on MSDN</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="dc949-199">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="dc949-199">stackoverflow</span></span>](http://go.microsoft.com/fwlink/?LinkId=320213)
