---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 04c51df96a538b32fa42454980ccd4f8cd1f7282
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761307"
---
# <span data-ttu-id="f70c9-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="f70c9-101">New-AzVM</span></span>

## <span data-ttu-id="f70c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f70c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f70c9-103">Sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f70c9-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="f70c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f70c9-104">SYNTAX</span></span>

### <span data-ttu-id="f70c9-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f70c9-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f70c9-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="f70c9-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f70c9-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f70c9-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f70c9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f70c9-108">DESCRIPTION</span></span>
<span data-ttu-id="f70c9-109">**New-AzVM** cmdlet 'i Azure 'da sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f70c9-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="f70c9-110">Bu cmdlet, giriş olarak bir sanal makine nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="f70c9-111">Sanal makine nesnesi oluşturmak için New-AzVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f70c9-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="f70c9-112">Diğer cmdlet 'ler, set-AzVMOperatingSystem, set-AzVMSourceImage, Add-Azvmnetworkınterface ve set-Azvmosdısk gibi sanal makineleri yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="f70c9-113">, `SimpleParameterSet` Ortak VM oluşturma bağımsız değişkenlerini isteğe bağlı olarak yaparak VM oluşturmak için uygun bir yöntem sağlar.</span><span class="sxs-lookup"><span data-stu-id="f70c9-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="f70c9-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f70c9-114">EXAMPLES</span></span>

### <span data-ttu-id="f70c9-115">Örnek 1: sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="f70c9-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="f70c9-116">Bu örnek komut dosyası, sanal makinenin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="f70c9-117">Komut dosyası, VM için Kullanıcı adı ve parola sorar.</span><span class="sxs-lookup"><span data-stu-id="f70c9-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="f70c9-118">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="f70c9-119">Örnek 2: özel Kullanıcı görüntüsünden sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="f70c9-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="f70c9-120">Bu örnekte, mevcut bir sys önceden yazılmış, genelleştirilmiş özel işletim sistemi görüntüsü yer alır ve bir veri disketi eklenir; yeni bir ağ sağlar, VHD 'yi dağıtır ve çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="f70c9-121">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="f70c9-122">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="f70c9-123">**Get-AzSubscription** cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f70c9-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="f70c9-124">Örnek 3: ortak IP olmadan Market görüntüsünden VM oluşturma</span><span class="sxs-lookup"><span data-stu-id="f70c9-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="f70c9-125">Bu örnek yeni bir ağ sağlar ve ortak IP adresi veya ağ güvenlik grubu oluşturmadan marketten bir Windows VM dağıtır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="f70c9-126">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="f70c9-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f70c9-127">PARAMETERS</span></span>

### <span data-ttu-id="f70c9-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f70c9-128">-AddressPrefix</span></span>
<span data-ttu-id="f70c9-129">VM için oluşturulacak sanal ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="f70c9-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="f70c9-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="f70c9-130">-AllocationMethod</span></span>
<span data-ttu-id="f70c9-131">VM için oluşturulacak ortak IP için IP ayırma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="f70c9-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="f70c9-132">-Iş</span><span class="sxs-lookup"><span data-stu-id="f70c9-132">-AsJob</span></span>
<span data-ttu-id="f70c9-133">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="f70c9-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f70c9-134">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="f70c9-134">-AvailabilitySetName</span></span>
<span data-ttu-id="f70c9-135">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="f70c9-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="f70c9-136">-Credential</span></span>
<span data-ttu-id="f70c9-137">VM için yönetici kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f70c9-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="f70c9-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="f70c9-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="f70c9-139">Veri disklerinin boyutunu GB cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="f70c9-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f70c9-140">-DefaultProfile</span></span>
<span data-ttu-id="f70c9-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f70c9-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f70c9-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="f70c9-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="f70c9-143">Bu cmdlet 'in sanal makinedeki **bg Info** uzantısını yüklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="f70c9-144">-Diskfıle</span><span class="sxs-lookup"><span data-stu-id="f70c9-144">-DiskFile</span></span>
<span data-ttu-id="f70c9-145">Buluta yüklenecek sanal sabit disk dosyasının yerel yolu ve VM 'i oluşturmak için, soneki olarak '. vhd ' bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="f70c9-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f70c9-146">-DomainNameLabel</span></span>
<span data-ttu-id="f70c9-147">VM 'nin tam etki alanı adı (FQDN) için alt etki alanı etiketi.</span><span class="sxs-lookup"><span data-stu-id="f70c9-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="f70c9-148">Bu, formu alır `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="f70c9-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="f70c9-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="f70c9-149">-EnableUltraSSD</span></span>
<span data-ttu-id="f70c9-150">VM için UltraSSD diskleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="f70c9-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="f70c9-151">-Image</span><span class="sxs-lookup"><span data-stu-id="f70c9-151">-Image</span></span>
<span data-ttu-id="f70c9-152">VM 'nin dayandığı kolay yansıma adı.</span><span class="sxs-lookup"><span data-stu-id="f70c9-152">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="f70c9-153">Bunlar şunlardır: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, de, openSUSE-</span><span class="sxs-lookup"><span data-stu-id="f70c9-153">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="f70c9-154">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f70c9-154">-LicenseType</span></span>
<span data-ttu-id="f70c9-155">Sanal makinenin resmi veya diskinin şirket içi lisanslı olduğunu belirten bir lisans türü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-155">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="f70c9-156">Bu değer yalnızca Windows Server işletim sistemi içeren resimler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-156">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="f70c9-157">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f70c9-157">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f70c9-158">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="f70c9-158">Windows_Client</span></span>
- <span data-ttu-id="f70c9-159">Windows_Server bu değer güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="f70c9-159">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="f70c9-160">Güncelleştirme için bu parametreyi belirtirseniz, değer sanal makinenin başlangıç değeriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-160">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="f70c9-161">-Linux</span><span class="sxs-lookup"><span data-stu-id="f70c9-161">-Linux</span></span>
<span data-ttu-id="f70c9-162">Belirtildiyse, disk dosyasının Linux VM için olup olmadığını gösterir; Varsayılan olarak belirtilmezse, pencereler.</span><span class="sxs-lookup"><span data-stu-id="f70c9-162">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="f70c9-163">-Konum</span><span class="sxs-lookup"><span data-stu-id="f70c9-163">-Location</span></span>
<span data-ttu-id="f70c9-164">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-164">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="f70c9-165">-Ad</span><span class="sxs-lookup"><span data-stu-id="f70c9-165">-Name</span></span>
<span data-ttu-id="f70c9-166">VM kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="f70c9-166">The name of the VM resource.</span></span>

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

### <span data-ttu-id="f70c9-167">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="f70c9-167">-OpenPorts</span></span>
<span data-ttu-id="f70c9-168">Oluşturulan VM için ağ güvenlik grubunda (NSG) açılacak bağlantı noktalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="f70c9-168">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="f70c9-169">Varsayılan değer, seçilen resim türüne (yani, Windows: 3389, 5985 ve Linux: 22) bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-169">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="f70c9-170">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="f70c9-170">-PublicIpAddressName</span></span>
<span data-ttu-id="f70c9-171">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) genel IP adresinin adı.</span><span class="sxs-lookup"><span data-stu-id="f70c9-171">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="f70c9-172">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f70c9-172">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="f70c9-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f70c9-173">-ResourceGroupName</span></span>
<span data-ttu-id="f70c9-174">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-174">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f70c9-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="f70c9-175">-SecurityGroupName</span></span>
<span data-ttu-id="f70c9-176">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir ağ güvenlik grubunun (NSG) adı.</span><span class="sxs-lookup"><span data-stu-id="f70c9-176">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="f70c9-177">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f70c9-177">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="f70c9-178">-Boyut</span><span class="sxs-lookup"><span data-stu-id="f70c9-178">-Size</span></span>
<span data-ttu-id="f70c9-179">Sanal makine boyutu.</span><span class="sxs-lookup"><span data-stu-id="f70c9-179">The Virtual Machine Size.</span></span>  <span data-ttu-id="f70c9-180">Varsayılan değer: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="f70c9-180">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="f70c9-181">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f70c9-181">-SubnetAddressPrefix</span></span>
<span data-ttu-id="f70c9-182">VM için oluşturulacak alt ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="f70c9-182">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="f70c9-183">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f70c9-183">-SubnetName</span></span>
<span data-ttu-id="f70c9-184">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="f70c9-184">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="f70c9-185">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f70c9-185">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="f70c9-186">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f70c9-186">-SystemAssignedIdentity</span></span>
<span data-ttu-id="f70c9-187">Parametre varsa, VM 'de otomatik olarak üretilen bir yönetilen sistem kimliği atanır.</span><span class="sxs-lookup"><span data-stu-id="f70c9-187">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="f70c9-188">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f70c9-188">-Tag</span></span>
<span data-ttu-id="f70c9-189">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-189">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="f70c9-190">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="f70c9-190">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="f70c9-191">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-191">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="f70c9-192">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="f70c9-192">-UserAssignedIdentity</span></span>
<span data-ttu-id="f70c9-193">VM 'ye atanması gereken yönetilen hizmet kimliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="f70c9-193">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="f70c9-194">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f70c9-194">-VirtualNetworkName</span></span>
<span data-ttu-id="f70c9-195">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) sanal ağının adı.</span><span class="sxs-lookup"><span data-stu-id="f70c9-195">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="f70c9-196">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f70c9-196">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="f70c9-197">-VM</span><span class="sxs-lookup"><span data-stu-id="f70c9-197">-VM</span></span>
<span data-ttu-id="f70c9-198">Oluşturulacak yerel sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-198">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="f70c9-199">Sanal makine nesnesi edinmek için New-AzVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f70c9-199">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="f70c9-200">Set-AzVMOperatingSystem, set-AzVMSourceImage ve Add-Azvmnetworkınterface gibi sanal makineyi yapılandırmak için diğer cmdlet 'ler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-200">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="f70c9-201">-Bölge</span><span class="sxs-lookup"><span data-stu-id="f70c9-201">-Zone</span></span>
<span data-ttu-id="f70c9-202">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-202">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="f70c9-203">-Onay</span><span class="sxs-lookup"><span data-stu-id="f70c9-203">-Confirm</span></span>
<span data-ttu-id="f70c9-204">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f70c9-204">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f70c9-205">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f70c9-205">-WhatIf</span></span>
<span data-ttu-id="f70c9-206">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f70c9-206">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f70c9-207">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f70c9-207">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f70c9-208">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f70c9-208">CommonParameters</span></span>
<span data-ttu-id="f70c9-209">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f70c9-209">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f70c9-210">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f70c9-210">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f70c9-211">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f70c9-211">INPUTS</span></span>

### <span data-ttu-id="f70c9-212">System. String</span><span class="sxs-lookup"><span data-stu-id="f70c9-212">System.String</span></span>

### <span data-ttu-id="f70c9-213">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f70c9-213">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="f70c9-214">System. String []</span><span class="sxs-lookup"><span data-stu-id="f70c9-214">System.String[]</span></span>

### <span data-ttu-id="f70c9-215">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f70c9-215">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f70c9-216">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f70c9-216">OUTPUTS</span></span>

### <span data-ttu-id="f70c9-217">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f70c9-217">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="f70c9-218">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f70c9-218">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f70c9-219">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f70c9-219">NOTES</span></span>

## <span data-ttu-id="f70c9-220">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f70c9-220">RELATED LINKS</span></span>

[<span data-ttu-id="f70c9-221">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="f70c9-221">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="f70c9-222">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="f70c9-222">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="f70c9-223">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="f70c9-223">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="f70c9-224">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="f70c9-224">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="f70c9-225">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="f70c9-225">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="f70c9-226">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="f70c9-226">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="f70c9-227">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f70c9-227">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="f70c9-228">Add-Azvmnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="f70c9-228">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="f70c9-229">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="f70c9-229">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="f70c9-230">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f70c9-230">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="f70c9-231">Set-Azvmsourceımage</span><span class="sxs-lookup"><span data-stu-id="f70c9-231">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="f70c9-232">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="f70c9-232">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)

