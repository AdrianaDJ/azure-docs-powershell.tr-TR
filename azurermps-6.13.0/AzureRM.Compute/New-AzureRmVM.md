---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: da307e1bc5bca5c3127e33a32bb4480148fe14a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763000"
---
# <span data-ttu-id="5d4fc-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d4fc-101">New-AzureRmVM</span></span>

## <span data-ttu-id="5d4fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d4fc-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4fc-103">Sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d4fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d4fc-104">SYNTAX</span></span>

### <span data-ttu-id="5d4fc-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d4fc-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d4fc-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d4fc-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d4fc-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d4fc-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d4fc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d4fc-108">DESCRIPTION</span></span>
<span data-ttu-id="5d4fc-109">**New-AzureRmVM** cmdlet 'i Azure 'da sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="5d4fc-110">Bu cmdlet, giriş olarak bir sanal makine nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="5d4fc-111">Sanal makine nesnesi oluşturmak için New-AzureRmVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="5d4fc-112">Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi sanal makineyi yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>
<span data-ttu-id="5d4fc-113">, `SimpleParameterSet` Ortak VM oluşturma bağımsız değişkenlerini isteğe bağlı olarak yaparak VM oluşturmak için uygun bir yöntem sağlar.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="5d4fc-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d4fc-114">EXAMPLES</span></span>

### <span data-ttu-id="5d4fc-115">Örnek 1: sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="5d4fc-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

<span data-ttu-id="5d4fc-116">Bu örnek komut dosyası, sanal makinenin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="5d4fc-117">Komut dosyası, VM için Kullanıcı adı ve parola sorar.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="5d4fc-118">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="5d4fc-119">Örnek 2: özel Kullanıcı görüntüsünden sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="5d4fc-119">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="5d4fc-120">Bu örnekte, mevcut bir sys önceden yazılmış, genelleştirilmiş özel işletim sistemi görüntüsü yer alır ve bir veri disketi eklenir; yeni bir ağ sağlar, VHD 'yi dağıtır ve çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="5d4fc-121">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="5d4fc-122">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="5d4fc-123">**Get-azuyeniden gönderme scripscripts** cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

### <span data-ttu-id="5d4fc-124">Örnek 3: ortak IP olmadan Market görüntüsünden VM oluşturma</span><span class="sxs-lookup"><span data-stu-id="5d4fc-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="5d4fc-125">Bu örnek yeni bir ağ sağlar ve ortak IP adresi veya ağ güvenlik grubu oluşturmadan marketten bir Windows VM dağıtır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="5d4fc-126">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="5d4fc-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d4fc-127">PARAMETERS</span></span>

### <span data-ttu-id="5d4fc-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5d4fc-128">-AddressPrefix</span></span>
<span data-ttu-id="5d4fc-129">VM için oluşturulacak sanal ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="5d4fc-130">-AllocationMethod</span></span>
<span data-ttu-id="5d4fc-131">VM için oluşturulacak ortak IP için IP ayırma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-132">-Iş</span><span class="sxs-lookup"><span data-stu-id="5d4fc-132">-AsJob</span></span>
<span data-ttu-id="5d4fc-133">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-133">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-134">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="5d4fc-134">-AvailabilitySetName</span></span>
<span data-ttu-id="5d4fc-135">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="5d4fc-136">-Credential</span></span>
<span data-ttu-id="5d4fc-137">VM için yönetici kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-137">The administrator credentials for the VM.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="5d4fc-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="5d4fc-139">Veri disklerinin boyutunu GB cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4fc-140">-DefaultProfile</span></span>
<span data-ttu-id="5d4fc-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="5d4fc-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="5d4fc-143">Bu cmdlet 'in sanal makinedeki **bg Info** uzantısını yüklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-144">-Diskfıle</span><span class="sxs-lookup"><span data-stu-id="5d4fc-144">-DiskFile</span></span>
<span data-ttu-id="5d4fc-145">Buluta yüklenecek sanal sabit disk dosyasının yerel yolu ve VM 'i oluşturmak için, soneki olarak '. vhd ' bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="5d4fc-146">-DomainNameLabel</span></span>
<span data-ttu-id="5d4fc-147">VM 'nin tam etki alanı adı (FQDN) için alt etki alanı etiketi.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="5d4fc-148">Bu, formu alır `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="5d4fc-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-149">-Image</span><span class="sxs-lookup"><span data-stu-id="5d4fc-149">-Image</span></span>
<span data-ttu-id="5d4fc-150">VM 'nin dayandığı kolay yansıma adı.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-150">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="5d4fc-151">Bunlar şunlardır: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, de, openSUSE-</span><span class="sxs-lookup"><span data-stu-id="5d4fc-151">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-152">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5d4fc-152">-LicenseType</span></span>
<span data-ttu-id="5d4fc-153">Sanal makinenin resmi veya diskinin şirket içi lisanslı olduğunu belirten bir lisans türü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-153">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="5d4fc-154">Bu değer yalnızca Windows Server işletim sistemi içeren resimler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-154">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="5d4fc-155">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5d4fc-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d4fc-156">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="5d4fc-156">Windows_Client</span></span>
- <span data-ttu-id="5d4fc-157">Windows_Server bu değer güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-157">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="5d4fc-158">Güncelleştirme için bu parametreyi belirtirseniz, değer sanal makinenin başlangıç değeriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-158">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-159">-Linux</span><span class="sxs-lookup"><span data-stu-id="5d4fc-159">-Linux</span></span>
<span data-ttu-id="5d4fc-160">Belirtildiyse, disk dosyasının Linux VM için olup olmadığını gösterir; Varsayılan olarak belirtilmezse, pencereler.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-160">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-161">-Konum</span><span class="sxs-lookup"><span data-stu-id="5d4fc-161">-Location</span></span>
<span data-ttu-id="5d4fc-162">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-162">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-163">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d4fc-163">-Name</span></span>
<span data-ttu-id="5d4fc-164">VM kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-164">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-165">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="5d4fc-165">-OpenPorts</span></span>
<span data-ttu-id="5d4fc-166">Oluşturulan VM için ağ güvenlik grubunda (NSG) açılacak bağlantı noktalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-166">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="5d4fc-167">Varsayılan değer, seçilen resim türüne (yani, Windows: 3389, 5985 ve Linux: 22) bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-167">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-168">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="5d4fc-168">-PublicIpAddressName</span></span>
<span data-ttu-id="5d4fc-169">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) genel IP adresinin adı.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-169">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="5d4fc-170">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-170">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4fc-171">-ResourceGroupName</span></span>
<span data-ttu-id="5d4fc-172">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-172">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-173">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4fc-173">-SecurityGroupName</span></span>
<span data-ttu-id="5d4fc-174">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir ağ güvenlik grubunun (NSG) adı.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-174">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="5d4fc-175">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-175">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-176">-Boyut</span><span class="sxs-lookup"><span data-stu-id="5d4fc-176">-Size</span></span>
<span data-ttu-id="5d4fc-177">Sanal makine boyutu.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-177">The Virtual Machine Size.</span></span>  <span data-ttu-id="5d4fc-178">Varsayılan değer: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-178">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-179">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5d4fc-179">-SubnetAddressPrefix</span></span>
<span data-ttu-id="5d4fc-180">VM için oluşturulacak alt ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-180">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5d4fc-181">-SubnetName</span></span>
<span data-ttu-id="5d4fc-182">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-182">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="5d4fc-183">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-183">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-184">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5d4fc-184">-SystemAssignedIdentity</span></span>
<span data-ttu-id="5d4fc-185">Parametre varsa, VM 'de otomatik olarak üretilen bir yönetilen sistem kimliği atanır.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-185">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-186">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5d4fc-186">-Tag</span></span>
<span data-ttu-id="5d4fc-187">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-187">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="5d4fc-188">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-188">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="5d4fc-189">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-189">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-190">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="5d4fc-190">-UserAssignedIdentity</span></span>
<span data-ttu-id="5d4fc-191">VM 'ye atanması gereken yönetilen hizmet kimliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-191">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-192">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5d4fc-192">-VirtualNetworkName</span></span>
<span data-ttu-id="5d4fc-193">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) sanal ağının adı.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-193">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="5d4fc-194">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-194">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-195">-VM</span><span class="sxs-lookup"><span data-stu-id="5d4fc-195">-VM</span></span>
<span data-ttu-id="5d4fc-196">Oluşturulacak yerel sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-196">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="5d4fc-197">Sanal makine nesnesi edinmek için New-AzureRmVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-197">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="5d4fc-198">AzureRmVMOperatingSystem, set-AzureRmVMSourceImage ve Add-Azurermvmnetworkınterface gibi sanal makineyi yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-198">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-199">-Bölge</span><span class="sxs-lookup"><span data-stu-id="5d4fc-199">-Zone</span></span>
<span data-ttu-id="5d4fc-200">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-200">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-201">-Onay</span><span class="sxs-lookup"><span data-stu-id="5d4fc-201">-Confirm</span></span>
<span data-ttu-id="5d4fc-202">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-202">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-203">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d4fc-203">-WhatIf</span></span>
<span data-ttu-id="5d4fc-204">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-204">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d4fc-205">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-205">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d4fc-206">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4fc-206">CommonParameters</span></span>
<span data-ttu-id="5d4fc-207">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d4fc-207">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4fc-208">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d4fc-208">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4fc-209">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d4fc-209">INPUTS</span></span>

### <span data-ttu-id="5d4fc-210">System. String</span><span class="sxs-lookup"><span data-stu-id="5d4fc-210">System.String</span></span>

### <span data-ttu-id="5d4fc-211">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5d4fc-211">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5d4fc-212">System. String []</span><span class="sxs-lookup"><span data-stu-id="5d4fc-212">System.String[]</span></span>

### <span data-ttu-id="5d4fc-213">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d4fc-213">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5d4fc-214">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d4fc-214">OUTPUTS</span></span>

### <span data-ttu-id="5d4fc-215">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5d4fc-215">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="5d4fc-216">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5d4fc-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5d4fc-217">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d4fc-217">NOTES</span></span>

## <span data-ttu-id="5d4fc-218">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d4fc-218">RELATED LINKS</span></span>

[<span data-ttu-id="5d4fc-219">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d4fc-219">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5d4fc-220">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d4fc-220">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5d4fc-221">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d4fc-221">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="5d4fc-222">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d4fc-222">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5d4fc-223">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d4fc-223">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="5d4fc-224">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5d4fc-224">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="5d4fc-225">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5d4fc-225">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="5d4fc-226">Add-Azurermvmnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="5d4fc-226">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="5d4fc-227">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5d4fc-227">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="5d4fc-228">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5d4fc-228">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="5d4fc-229">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5d4fc-229">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="5d4fc-230">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="5d4fc-230">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


