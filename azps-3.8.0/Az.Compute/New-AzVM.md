---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 6e2ecda144472bdb35ffe1310f648b277353177b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096924"
---
# <span data-ttu-id="bd071-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd071-101">New-AzVM</span></span>

## <span data-ttu-id="bd071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd071-102">SYNOPSIS</span></span>
<span data-ttu-id="bd071-103">Sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd071-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="bd071-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd071-104">SYNTAX</span></span>

### <span data-ttu-id="bd071-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd071-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd071-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd071-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd071-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd071-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd071-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd071-108">DESCRIPTION</span></span>
<span data-ttu-id="bd071-109">**New-AzVM** cmdlet 'i Azure 'da sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bd071-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="bd071-110">Bu cmdlet, giriş olarak bir sanal makine nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="bd071-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="bd071-111">Sanal makine nesnesi oluşturmak için New-AzVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bd071-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="bd071-112">Diğer cmdlet 'ler, set-AzVMOperatingSystem, set-AzVMSourceImage, Add-Azvmnetworkınterface ve set-Azvmosdısk gibi sanal makineleri yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bd071-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="bd071-113">, `SimpleParameterSet` Ortak VM oluşturma bağımsız değişkenlerini isteğe bağlı olarak yaparak VM oluşturmak için uygun bir yöntem sağlar.</span><span class="sxs-lookup"><span data-stu-id="bd071-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="bd071-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd071-114">EXAMPLES</span></span>

### <span data-ttu-id="bd071-115">Örnek 1: sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bd071-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="bd071-116">Bu örnek komut dosyası, sanal makinenin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd071-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="bd071-117">Komut dosyası, VM için Kullanıcı adı ve parola sorar.</span><span class="sxs-lookup"><span data-stu-id="bd071-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="bd071-118">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="bd071-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="bd071-119">Örnek 2: özel Kullanıcı görüntüsünden sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="bd071-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="bd071-120">Bu örnekte, mevcut bir sys önceden yazılmış, genelleştirilmiş özel işletim sistemi görüntüsü yer alır ve bir veri disketi eklenir; yeni bir ağ sağlar, VHD 'yi dağıtır ve çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="bd071-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="bd071-121">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bd071-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="bd071-122">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="bd071-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="bd071-123">**Get-AzSubscription** cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bd071-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="bd071-124">Örnek 3: ortak IP olmadan Market görüntüsünden VM oluşturma</span><span class="sxs-lookup"><span data-stu-id="bd071-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

<span data-ttu-id="bd071-125">Bu örnek yeni bir ağ sağlar ve ortak IP adresi veya ağ güvenlik grubu oluşturmadan marketten bir Windows VM dağıtır.</span><span class="sxs-lookup"><span data-stu-id="bd071-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="bd071-126">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bd071-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="bd071-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd071-127">PARAMETERS</span></span>

### <span data-ttu-id="bd071-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bd071-128">-AddressPrefix</span></span>
<span data-ttu-id="bd071-129">VM için oluşturulacak sanal ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="bd071-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="bd071-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="bd071-130">-AllocationMethod</span></span>
<span data-ttu-id="bd071-131">VM için oluşturulacak ortak IP için IP ayırma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="bd071-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="bd071-132">-Iş</span><span class="sxs-lookup"><span data-stu-id="bd071-132">-AsJob</span></span>
<span data-ttu-id="bd071-133">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="bd071-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bd071-134">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="bd071-134">-AvailabilitySetName</span></span>
<span data-ttu-id="bd071-135">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd071-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="bd071-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="bd071-136">-Credential</span></span>
<span data-ttu-id="bd071-137">VM için yönetici kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="bd071-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="bd071-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="bd071-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="bd071-139">Veri disklerinin boyutunu GB cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd071-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="bd071-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd071-140">-DefaultProfile</span></span>
<span data-ttu-id="bd071-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd071-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd071-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="bd071-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="bd071-143">Bu cmdlet 'in sanal makinedeki **bg Info** uzantısını yüklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd071-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="bd071-144">-Diskfıle</span><span class="sxs-lookup"><span data-stu-id="bd071-144">-DiskFile</span></span>
<span data-ttu-id="bd071-145">Buluta yüklenecek sanal sabit disk dosyasının yerel yolu ve VM 'i oluşturmak için, soneki olarak '. vhd ' bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="bd071-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="bd071-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="bd071-146">-DomainNameLabel</span></span>
<span data-ttu-id="bd071-147">VM 'nin tam etki alanı adı (FQDN) için alt etki alanı etiketi.</span><span class="sxs-lookup"><span data-stu-id="bd071-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="bd071-148">Bu, formu alır `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="bd071-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="bd071-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="bd071-149">-EnableUltraSSD</span></span>
<span data-ttu-id="bd071-150">VM için UltraSSD diskleri kullanın.</span><span class="sxs-lookup"><span data-stu-id="bd071-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="bd071-151">-Çıkarma Ilkesi</span><span class="sxs-lookup"><span data-stu-id="bd071-151">-EvictionPolicy</span></span>
<span data-ttu-id="bd071-152">Düşük öncelikli sanal makine için çıkarma ilkesi.</span><span class="sxs-lookup"><span data-stu-id="bd071-152">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="bd071-153">Yalnızca desteklenen değer ' ayırması '.</span><span class="sxs-lookup"><span data-stu-id="bd071-153">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="bd071-154">-HostId</span><span class="sxs-lookup"><span data-stu-id="bd071-154">-HostId</span></span>
<span data-ttu-id="bd071-155">Ana bilgisayar kimliği</span><span class="sxs-lookup"><span data-stu-id="bd071-155">The Id of Host</span></span>

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

### <span data-ttu-id="bd071-156">-Image</span><span class="sxs-lookup"><span data-stu-id="bd071-156">-Image</span></span>
<span data-ttu-id="bd071-157">VM 'nin dayandığı kolay yansıma adı.</span><span class="sxs-lookup"><span data-stu-id="bd071-157">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="bd071-158">Bunlar şunlardır: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, de, openSUSE-</span><span class="sxs-lookup"><span data-stu-id="bd071-158">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="bd071-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="bd071-159">-LicenseType</span></span>
<span data-ttu-id="bd071-160">Sanal makinenin resmi veya diskinin şirket içi lisanslı olduğunu belirten bir lisans türü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd071-160">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="bd071-161">Bu değer yalnızca Windows Server işletim sistemi içeren resimler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bd071-161">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="bd071-162">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="bd071-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bd071-163">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="bd071-163">Windows_Client</span></span>
- <span data-ttu-id="bd071-164">Windows_Server bu değer güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="bd071-164">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="bd071-165">Güncelleştirme için bu parametreyi belirtirseniz, değer sanal makinenin başlangıç değeriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="bd071-165">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="bd071-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="bd071-166">-Linux</span></span>
<span data-ttu-id="bd071-167">Belirtildiyse, disk dosyasının Linux VM için olup olmadığını gösterir; Varsayılan olarak belirtilmezse, pencereler.</span><span class="sxs-lookup"><span data-stu-id="bd071-167">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="bd071-168">-Konum</span><span class="sxs-lookup"><span data-stu-id="bd071-168">-Location</span></span>
<span data-ttu-id="bd071-169">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd071-169">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="bd071-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="bd071-170">-MaxPrice</span></span>
<span data-ttu-id="bd071-171">Düşük öncelikli sanal makinenin faturalandırmanın maks.</span><span class="sxs-lookup"><span data-stu-id="bd071-171">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd071-172">-Ad</span><span class="sxs-lookup"><span data-stu-id="bd071-172">-Name</span></span>
<span data-ttu-id="bd071-173">VM kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="bd071-173">The name of the VM resource.</span></span>

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

### <span data-ttu-id="bd071-174">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="bd071-174">-OpenPorts</span></span>
<span data-ttu-id="bd071-175">Oluşturulan VM için ağ güvenlik grubunda (NSG) açılacak bağlantı noktalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="bd071-175">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="bd071-176">Varsayılan değer, seçilen resim türüne (yani, Windows: 3389, 5985 ve Linux: 22) bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="bd071-176">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="bd071-177">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="bd071-177">-Priority</span></span>
<span data-ttu-id="bd071-178">Sanal makinenin önceliği.</span><span class="sxs-lookup"><span data-stu-id="bd071-178">The priority for the virtual machine.</span></span>  <span data-ttu-id="bd071-179">Yalnızca desteklenen değerler ' Regular ', ' nokta ' ve ' düşük ' değerleridir.</span><span class="sxs-lookup"><span data-stu-id="bd071-179">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="bd071-180">' Regular ' normal sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="bd071-180">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="bd071-181">' Spot ', spot sanal makine içindir.</span><span class="sxs-lookup"><span data-stu-id="bd071-181">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="bd071-182">' Low ', spot sanal makine için de, ancak ' nokta ' ile değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bd071-182">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="bd071-183">Lütfen ' düşük ' yerine ' nokta ' kullanın.</span><span class="sxs-lookup"><span data-stu-id="bd071-183">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="bd071-184">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="bd071-184">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="bd071-185">Bu sanal makineyle kullanılacak yakınlık Yerleşim grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bd071-185">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd071-186">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="bd071-186">-PublicIpAddressName</span></span>
<span data-ttu-id="bd071-187">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) genel IP adresinin adı.</span><span class="sxs-lookup"><span data-stu-id="bd071-187">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="bd071-188">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bd071-188">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="bd071-189">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd071-189">-ResourceGroupName</span></span>
<span data-ttu-id="bd071-190">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd071-190">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bd071-191">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="bd071-191">-SecurityGroupName</span></span>
<span data-ttu-id="bd071-192">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir ağ güvenlik grubunun (NSG) adı.</span><span class="sxs-lookup"><span data-stu-id="bd071-192">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="bd071-193">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bd071-193">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="bd071-194">-Boyut</span><span class="sxs-lookup"><span data-stu-id="bd071-194">-Size</span></span>
<span data-ttu-id="bd071-195">Sanal makine boyutu.</span><span class="sxs-lookup"><span data-stu-id="bd071-195">The Virtual Machine Size.</span></span>  <span data-ttu-id="bd071-196">Varsayılan değer: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="bd071-196">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="bd071-197">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="bd071-197">-SubnetAddressPrefix</span></span>
<span data-ttu-id="bd071-198">VM için oluşturulacak alt ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="bd071-198">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="bd071-199">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="bd071-199">-SubnetName</span></span>
<span data-ttu-id="bd071-200">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="bd071-200">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="bd071-201">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bd071-201">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="bd071-202">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="bd071-202">-SystemAssignedIdentity</span></span>
<span data-ttu-id="bd071-203">Parametre varsa, VM 'de otomatik olarak üretilen bir yönetilen sistem kimliği atanır.</span><span class="sxs-lookup"><span data-stu-id="bd071-203">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="bd071-204">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bd071-204">-Tag</span></span>
<span data-ttu-id="bd071-205">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd071-205">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="bd071-206">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="bd071-206">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="bd071-207">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="bd071-207">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="bd071-208">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="bd071-208">-UserAssignedIdentity</span></span>
<span data-ttu-id="bd071-209">VM 'ye atanması gereken yönetilen hizmet kimliğinin adı.</span><span class="sxs-lookup"><span data-stu-id="bd071-209">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="bd071-210">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bd071-210">-VirtualNetworkName</span></span>
<span data-ttu-id="bd071-211">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) sanal ağının adı.</span><span class="sxs-lookup"><span data-stu-id="bd071-211">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="bd071-212">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bd071-212">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="bd071-213">-VM</span><span class="sxs-lookup"><span data-stu-id="bd071-213">-VM</span></span>
<span data-ttu-id="bd071-214">Oluşturulacak yerel sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd071-214">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="bd071-215">Sanal makine nesnesi edinmek için New-AzVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bd071-215">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="bd071-216">Set-AzVMOperatingSystem, set-AzVMSourceImage ve Add-Azvmnetworkınterface gibi sanal makineyi yapılandırmak için diğer cmdlet 'ler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="bd071-216">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="bd071-217">-Bölge</span><span class="sxs-lookup"><span data-stu-id="bd071-217">-Zone</span></span>
<span data-ttu-id="bd071-218">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bd071-218">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="bd071-219">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd071-219">-Confirm</span></span>
<span data-ttu-id="bd071-220">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd071-220">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd071-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd071-221">-WhatIf</span></span>
<span data-ttu-id="bd071-222">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd071-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd071-223">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd071-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd071-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd071-224">CommonParameters</span></span>
<span data-ttu-id="bd071-225">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd071-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd071-226">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bd071-226">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd071-227">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd071-227">INPUTS</span></span>

### <span data-ttu-id="bd071-228">System. String</span><span class="sxs-lookup"><span data-stu-id="bd071-228">System.String</span></span>

### <span data-ttu-id="bd071-229">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bd071-229">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="bd071-230">System. String []</span><span class="sxs-lookup"><span data-stu-id="bd071-230">System.String[]</span></span>

### <span data-ttu-id="bd071-231">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd071-231">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bd071-232">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd071-232">OUTPUTS</span></span>

### <span data-ttu-id="bd071-233">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bd071-233">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="bd071-234">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="bd071-234">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="bd071-235">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd071-235">NOTES</span></span>

## <span data-ttu-id="bd071-236">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd071-236">RELATED LINKS</span></span>

[<span data-ttu-id="bd071-237">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd071-237">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bd071-238">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd071-238">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="bd071-239">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd071-239">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="bd071-240">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd071-240">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="bd071-241">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd071-241">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="bd071-242">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bd071-242">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="bd071-243">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="bd071-243">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="bd071-244">Add-Azvmnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="bd071-244">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="bd071-245">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="bd071-245">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="bd071-246">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bd071-246">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="bd071-247">Set-Azvmsourceımage</span><span class="sxs-lookup"><span data-stu-id="bd071-247">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="bd071-248">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="bd071-248">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)

