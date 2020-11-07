---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 107441c07e958099d330859a5003a2dafcd64bf9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936959"
---
# <span data-ttu-id="33211-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="33211-101">New-AzVM</span></span>

## <span data-ttu-id="33211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33211-102">SYNOPSIS</span></span>
<span data-ttu-id="33211-103">Sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="33211-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="33211-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33211-104">SYNTAX</span></span>

### <span data-ttu-id="33211-105">SimpleParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33211-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33211-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="33211-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33211-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="33211-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33211-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="33211-108">DESCRIPTION</span></span>
<span data-ttu-id="33211-109">**New-AzVM** cmdlet 'i Azure 'da sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="33211-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="33211-110">Bu cmdlet, giriş olarak bir sanal makine nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="33211-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="33211-111">Sanal makine nesnesi oluşturmak için New-AzVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="33211-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="33211-112">Diğer cmdlet 'ler, set-AzVMOperatingSystem, set-AzVMSourceImage, Add-Azvmnetworkınterface ve set-Azvmosdısk gibi sanal makineleri yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="33211-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>

<span data-ttu-id="33211-113">, `SimpleParameterSet` Ortak VM oluşturma bağımsız değişkenlerini isteğe bağlı olarak yaparak VM oluşturmak için uygun bir yöntem sağlar.</span><span class="sxs-lookup"><span data-stu-id="33211-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="33211-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33211-114">EXAMPLES</span></span>

### <span data-ttu-id="33211-115">Örnek 1: sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="33211-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm
```

<span data-ttu-id="33211-116">Bu örnek komut dosyası, sanal makinenin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="33211-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="33211-117">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="33211-117">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="33211-118">Örnek 2: özel Kullanıcı görüntüsünden sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="33211-118">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="33211-119">Bu örnekte, mevcut bir sys önceden yazılmış, genelleştirilmiş özel işletim sistemi görüntüsü yer alır ve bir veri disketi eklenir; yeni bir ağ sağlar, VHD 'yi dağıtır ve çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="33211-119">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="33211-120">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="33211-120">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="33211-121">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="33211-121">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="33211-122">**Get-azuyeniden gönderme scripscripts** cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="33211-122">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="33211-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33211-123">PARAMETERS</span></span>

### <span data-ttu-id="33211-124">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="33211-124">-AddressPrefix</span></span>
<span data-ttu-id="33211-125">VM için oluşturulacak sanal ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="33211-125">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="33211-126">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="33211-126">-AllocationMethod</span></span>
<span data-ttu-id="33211-127">VM için oluşturulacak ortak IP için IP ayırma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="33211-127">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="33211-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="33211-128">-AsJob</span></span>
<span data-ttu-id="33211-129">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="33211-129">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="33211-130">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="33211-130">-AvailabilitySetName</span></span>
<span data-ttu-id="33211-131">Kullanılabilirlik kümesi için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="33211-131">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="33211-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="33211-132">-Credential</span></span>
<span data-ttu-id="33211-133">VM için yönetici kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="33211-133">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="33211-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33211-134">-DefaultProfile</span></span>
<span data-ttu-id="33211-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33211-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33211-136">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="33211-136">-DisableBginfoExtension</span></span>
<span data-ttu-id="33211-137">Bu cmdlet 'in sanal makinedeki **bg Info** uzantısını yüklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="33211-137">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="33211-138">-Diskfıle</span><span class="sxs-lookup"><span data-stu-id="33211-138">-DiskFile</span></span>
<span data-ttu-id="33211-139">Buluta yüklenecek sanal sabit disk dosyasının yerel yolu ve VM 'i oluşturmak için, soneki olarak '. vhd ' bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="33211-139">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="33211-140">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="33211-140">-DomainNameLabel</span></span>
<span data-ttu-id="33211-141">VM 'nin tam etki alanı adı (FQDN) için alt etki alanı etiketi.</span><span class="sxs-lookup"><span data-stu-id="33211-141">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="33211-142">Bu, formu alır `{domainNameLabel}.{location}.cloudapp.azure.com` .</span><span class="sxs-lookup"><span data-stu-id="33211-142">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="33211-143">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="33211-143">-ImageName</span></span>
<span data-ttu-id="33211-144">VM 'nin dayandığı kolay yansıma adı.</span><span class="sxs-lookup"><span data-stu-id="33211-144">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="33211-145">Bunlar şunlardır: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, de, openSUSE-</span><span class="sxs-lookup"><span data-stu-id="33211-145">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="33211-146">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="33211-146">-LicenseType</span></span>
<span data-ttu-id="33211-147">Sanal makinenin resmi veya diskinin şirket içi lisanslı olduğunu belirten bir lisans türü belirtir.</span><span class="sxs-lookup"><span data-stu-id="33211-147">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="33211-148">Bu değer yalnızca Windows Server işletim sistemi içeren resimler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="33211-148">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="33211-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="33211-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="33211-150">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="33211-150">Windows_Client</span></span> 
- <span data-ttu-id="33211-151">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="33211-151">Windows_Server</span></span>

<span data-ttu-id="33211-152">Bu değer güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="33211-152">This value cannot be updated.</span></span>
<span data-ttu-id="33211-153">Güncelleştirme için bu parametreyi belirtirseniz, değer sanal makinenin başlangıç değeriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="33211-153">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="33211-154">-Linux</span><span class="sxs-lookup"><span data-stu-id="33211-154">-Linux</span></span>
<span data-ttu-id="33211-155">Belirtildiyse, disk dosyasının Linux VM için olup olmadığını gösterir; Varsayılan olarak belirtilmezse, pencereler.</span><span class="sxs-lookup"><span data-stu-id="33211-155">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="33211-156">-Konum</span><span class="sxs-lookup"><span data-stu-id="33211-156">-Location</span></span>
<span data-ttu-id="33211-157">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="33211-157">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="33211-158">-Ad</span><span class="sxs-lookup"><span data-stu-id="33211-158">-Name</span></span>
<span data-ttu-id="33211-159">VM kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="33211-159">The name of the VM resource.</span></span>

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

### <span data-ttu-id="33211-160">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="33211-160">-OpenPorts</span></span>
<span data-ttu-id="33211-161">Oluşturulan VM için ağ güvenlik grubunda (NSG) açılacak bağlantı noktalarının listesi.</span><span class="sxs-lookup"><span data-stu-id="33211-161">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="33211-162">Varsayılan değer, seçilen resim türüne (yani, Windows: 3389, 5985 ve Linux: 22) bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="33211-162">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="33211-163">-Publicıpaddressname</span><span class="sxs-lookup"><span data-stu-id="33211-163">-PublicIpAddressName</span></span>
<span data-ttu-id="33211-164">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) genel IP adresinin adı.</span><span class="sxs-lookup"><span data-stu-id="33211-164">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="33211-165">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="33211-165">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="33211-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33211-166">-ResourceGroupName</span></span>
<span data-ttu-id="33211-167">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="33211-167">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="33211-168">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="33211-168">-SecurityGroupName</span></span>
<span data-ttu-id="33211-169">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir ağ güvenlik grubunun (NSG) adı.</span><span class="sxs-lookup"><span data-stu-id="33211-169">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="33211-170">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="33211-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="33211-171">-Boyut</span><span class="sxs-lookup"><span data-stu-id="33211-171">-Size</span></span>
<span data-ttu-id="33211-172">Sanal makine boyutu.</span><span class="sxs-lookup"><span data-stu-id="33211-172">The Virtual Machine Size.</span></span>  <span data-ttu-id="33211-173">Varsayılan değer: Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="33211-173">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="33211-174">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="33211-174">-SubnetAddressPrefix</span></span>
<span data-ttu-id="33211-175">VM için oluşturulacak alt ağın adres öneki.</span><span class="sxs-lookup"><span data-stu-id="33211-175">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="33211-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="33211-176">-SubnetName</span></span>
<span data-ttu-id="33211-177">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="33211-177">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="33211-178">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="33211-178">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="33211-179">Etiketli</span><span class="sxs-lookup"><span data-stu-id="33211-179">-Tag</span></span>
<span data-ttu-id="33211-180">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="33211-180">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="33211-181">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="33211-181">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="33211-182">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="33211-182">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="33211-183">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="33211-183">-VirtualNetworkName</span></span>
<span data-ttu-id="33211-184">Oluşturulan VM 'nin kullanması için yeni (veya mevcut) sanal ağının adı.</span><span class="sxs-lookup"><span data-stu-id="33211-184">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="33211-185">Belirtilmezse, bir ad oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="33211-185">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="33211-186">-VM</span><span class="sxs-lookup"><span data-stu-id="33211-186">-VM</span></span>
<span data-ttu-id="33211-187">Oluşturulacak yerel sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="33211-187">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="33211-188">Sanal makine nesnesi edinmek için New-AzVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="33211-188">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="33211-189">Set-AzVMOperatingSystem, set-AzVMSourceImage ve Add-Azvmnetworkınterface gibi sanal makineyi yapılandırmak için diğer cmdlet 'ler kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="33211-189">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="33211-190">-Bölge</span><span class="sxs-lookup"><span data-stu-id="33211-190">-Zone</span></span>
<span data-ttu-id="33211-191">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="33211-191">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="33211-192">-Onay</span><span class="sxs-lookup"><span data-stu-id="33211-192">-Confirm</span></span>
<span data-ttu-id="33211-193">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="33211-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33211-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33211-194">-WhatIf</span></span>
<span data-ttu-id="33211-195">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="33211-195">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="33211-196">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="33211-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33211-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33211-197">CommonParameters</span></span>
<span data-ttu-id="33211-198">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33211-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33211-199">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33211-199">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33211-200">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33211-200">INPUTS</span></span>

### <span data-ttu-id="33211-201">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="33211-201">PSVirtualMachine</span></span>
<span data-ttu-id="33211-202">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="33211-202">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="33211-203">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33211-203">OUTPUTS</span></span>

### <span data-ttu-id="33211-204">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="33211-204">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="33211-205">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33211-205">NOTES</span></span>

## <span data-ttu-id="33211-206">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33211-206">RELATED LINKS</span></span>

[<span data-ttu-id="33211-207">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="33211-207">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="33211-208">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="33211-208">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="33211-209">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="33211-209">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="33211-210">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="33211-210">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="33211-211">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="33211-211">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="33211-212">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="33211-212">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="33211-213">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="33211-213">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="33211-214">Add-Azvmnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="33211-214">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="33211-215">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="33211-215">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="33211-216">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="33211-216">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="33211-217">Set-Azvmsourceımage</span><span class="sxs-lookup"><span data-stu-id="33211-217">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="33211-218">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="33211-218">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


