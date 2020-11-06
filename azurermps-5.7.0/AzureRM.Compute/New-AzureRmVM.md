---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587617"
---
# <span data-ttu-id="5ab87-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ab87-101">New-AzureRmVM</span></span>

## <span data-ttu-id="5ab87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ab87-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab87-103">Sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ab87-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ab87-104">SYNTAX</span></span>

### <span data-ttu-id="5ab87-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5ab87-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab87-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ab87-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ab87-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ab87-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab87-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ab87-108">DESCRIPTION</span></span>
<span data-ttu-id="5ab87-109">**New-AzureRmVM** cmdlet 'i Azure 'da sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ab87-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="5ab87-110">Bu cmdlet, giriş olarak bir sanal makine nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="5ab87-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="5ab87-111">Sanal makine nesnesi oluşturmak için New-AzureRmVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5ab87-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="5ab87-112">Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi sanal makineyi yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="5ab87-113">, `SimpleParameterSet` Ortak VM oluşturma bağımsız değişkenlerini isteğe bağlı olarak yaparak VM oluşturmak için uygun bir yöntem sağlar.</span><span class="sxs-lookup"><span data-stu-id="5ab87-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="5ab87-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ab87-114">EXAMPLES</span></span>

### <span data-ttu-id="5ab87-115">Örnek 1: sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="5ab87-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="5ab87-116">Bu örnek komut dosyası, sanal makinenin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="5ab87-117">Komut dosyası, VM için Kullanıcı adı ve parola sorar.</span><span class="sxs-lookup"><span data-stu-id="5ab87-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="5ab87-118">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="5ab87-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="5ab87-119">Örnek 2: özel Kullanıcı görüntüsünden sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="5ab87-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="5ab87-120">Bu örnekte, mevcut bir sys önceden yazılmış, genelleştirilmiş özel işletim sistemi görüntüsü yer alır ve bir veri disketi eklenir; yeni bir ağ sağlar, VHD 'yi dağıtır ve çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="5ab87-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="5ab87-121">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="5ab87-122">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="5ab87-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="5ab87-123">**Get-azuyeniden gönderme scripscripts** cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ab87-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="5ab87-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ab87-124">PARAMETERS</span></span>

### <span data-ttu-id="5ab87-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5ab87-125">-AddressPrefix</span></span>
<span data-ttu-id="5ab87-126">VM için oluşturulacak sanal ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="5ab87-126">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="5ab87-127">-AllocationMethod</span></span>
<span data-ttu-id="5ab87-128">VM için oluşturulacak ortak IP için IP ayırma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="5ab87-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-129">-Iş</span><span class="sxs-lookup"><span data-stu-id="5ab87-129">-AsJob</span></span>
<span data-ttu-id="5ab87-130">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="5ab87-130">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-131">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="5ab87-131">-AvailabilitySetName</span></span>
<span data-ttu-id="5ab87-132">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-132">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-133">-Credential</span><span class="sxs-lookup"><span data-stu-id="5ab87-133">-Credential</span></span>
<span data-ttu-id="5ab87-134">VM için yönetici kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="5ab87-134">The administrator credentials for the VM.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="5ab87-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="5ab87-136">Veri disklerinin boyutunu GB cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-136">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab87-137">-DefaultProfile</span></span>
<span data-ttu-id="5ab87-138">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ab87-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="5ab87-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="5ab87-140">Bu cmdlet 'in sanal makinedeki **bg Info** uzantısını yüklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-141">-Diskfıle</span><span class="sxs-lookup"><span data-stu-id="5ab87-141">-DiskFile</span></span>
<span data-ttu-id="5ab87-142">Buluta yüklenecek sanal sabit disk dosyasının yerel yolu ve VM 'i oluşturmak için, soneki olarak '. vhd ' bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5ab87-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="5ab87-143">-DomainNameLabel</span></span>
<span data-ttu-id="5ab87-144">VM 'nin tam etki alanı adı (FQDN) için alt etki alanı etiketi.</span><span class="sxs-lookup"><span data-stu-id="5ab87-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="5ab87-145">Bu, formu alır `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="5ab87-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-146">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="5ab87-146">-ImageName</span></span>
<span data-ttu-id="5ab87-147">VM 'nin dayandığı kolay yansıma adı.</span><span class="sxs-lookup"><span data-stu-id="5ab87-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="5ab87-148">Bunlar şunlardır: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, de, openSUSE-</span><span class="sxs-lookup"><span data-stu-id="5ab87-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5ab87-149">-LicenseType</span></span>
<span data-ttu-id="5ab87-150">Sanal makinenin resmi veya diskinin şirket içi lisanslı olduğunu belirten bir lisans türü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="5ab87-151">Bu değer yalnızca Windows Server işletim sistemi içeren resimler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5ab87-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="5ab87-152">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5ab87-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5ab87-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="5ab87-153">Windows_Client</span></span>
- <span data-ttu-id="5ab87-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="5ab87-154">Windows_Server</span></span>

<span data-ttu-id="5ab87-155">Bu değer güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="5ab87-155">This value cannot be updated.</span></span>
<span data-ttu-id="5ab87-156">Güncelleştirme için bu parametreyi belirtirseniz, değer sanal makinenin başlangıç değeriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="5ab87-157">-Linux</span></span>
<span data-ttu-id="5ab87-158">Belirtildiyse, disk dosyasının Linux VM için olup olmadığını gösterir; Varsayılan olarak belirtilmezse, pencereler.</span><span class="sxs-lookup"><span data-stu-id="5ab87-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-159">-Konum</span><span class="sxs-lookup"><span data-stu-id="5ab87-159">-Location</span></span>
<span data-ttu-id="5ab87-160">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-160">Specifies a location for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-161">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ab87-161">-Name</span></span>
<span data-ttu-id="5ab87-162">VM kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="5ab87-162">The name of the VM resource.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-163">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="5ab87-163">-OpenPorts</span></span>
<span data-ttu-id="5ab87-164">Oluşturulan VM için ağ güvenlik grubunda (NSG) açılacak bağlantı noktalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="5ab87-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="5ab87-165">Varsayılan değer, seçilen resim türüne (yani, Windows: 3389, 5985 ve Linux: 22) bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="5ab87-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-166">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="5ab87-166">-PublicIpAddressName</span></span>
<span data-ttu-id="5ab87-167">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) genel IP adresinin adı.</span><span class="sxs-lookup"><span data-stu-id="5ab87-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="5ab87-168">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ab87-168">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab87-169">-ResourceGroupName</span></span>
<span data-ttu-id="5ab87-170">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-170">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab87-171">-SecurityGroupName</span></span>
<span data-ttu-id="5ab87-172">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir ağ güvenlik grubunun (NSG) adı.</span><span class="sxs-lookup"><span data-stu-id="5ab87-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="5ab87-173">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ab87-173">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-174">-Boyut</span><span class="sxs-lookup"><span data-stu-id="5ab87-174">-Size</span></span>
<span data-ttu-id="5ab87-175">Sanal makine boyutu.</span><span class="sxs-lookup"><span data-stu-id="5ab87-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="5ab87-176">Varsayılan değer: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="5ab87-176">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5ab87-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="5ab87-178">VM için oluşturulacak alt ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="5ab87-178">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5ab87-179">-SubnetName</span></span>
<span data-ttu-id="5ab87-180">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="5ab87-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="5ab87-181">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ab87-181">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-182">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5ab87-182">-Tag</span></span>
<span data-ttu-id="5ab87-183">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="5ab87-184">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="5ab87-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="5ab87-185">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5ab87-186">-VirtualNetworkName</span></span>
<span data-ttu-id="5ab87-187">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) sanal ağının adı.</span><span class="sxs-lookup"><span data-stu-id="5ab87-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="5ab87-188">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ab87-188">If not specified, a name will be generated.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-189">-VM</span><span class="sxs-lookup"><span data-stu-id="5ab87-189">-VM</span></span>
<span data-ttu-id="5ab87-190">Oluşturulacak yerel sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="5ab87-191">Sanal makine nesnesi edinmek için New-AzureRmVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5ab87-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="5ab87-192">AzureRmVMOperatingSystem, set-AzureRmVMSourceImage ve Add-Azurermvmnetworkınterface gibi sanal makineyi yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-193">-Bölge</span><span class="sxs-lookup"><span data-stu-id="5ab87-193">-Zone</span></span>
<span data-ttu-id="5ab87-194">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-194">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-195">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ab87-195">-Confirm</span></span>
<span data-ttu-id="5ab87-196">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ab87-196">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab87-197">-WhatIf</span></span>
<span data-ttu-id="5ab87-198">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ab87-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5ab87-199">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ab87-199">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ab87-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab87-200">CommonParameters</span></span>
<span data-ttu-id="5ab87-201">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ab87-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab87-202">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab87-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab87-203">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ab87-203">INPUTS</span></span>

### <span data-ttu-id="5ab87-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5ab87-204">PSVirtualMachine</span></span>
<span data-ttu-id="5ab87-205">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5ab87-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="5ab87-206">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ab87-206">OUTPUTS</span></span>

### <span data-ttu-id="5ab87-207">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5ab87-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5ab87-208">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ab87-208">NOTES</span></span>

## <span data-ttu-id="5ab87-209">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ab87-209">RELATED LINKS</span></span>

[<span data-ttu-id="5ab87-210">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ab87-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5ab87-211">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ab87-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="5ab87-212">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ab87-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="5ab87-213">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ab87-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="5ab87-214">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ab87-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="5ab87-215">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5ab87-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="5ab87-216">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5ab87-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="5ab87-217">Add-Azurermvmnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="5ab87-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="5ab87-218">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5ab87-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="5ab87-219">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5ab87-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="5ab87-220">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5ab87-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="5ab87-221">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="5ab87-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


