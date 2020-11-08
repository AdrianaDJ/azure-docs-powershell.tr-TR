---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105909"
---
# <span data-ttu-id="b4909-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="b4909-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="b4909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4909-102">SYNOPSIS</span></span>
<span data-ttu-id="b4909-103">Bir Azure sanal makinesini yapılandırır ve oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="b4909-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4909-104">SYNTAX</span></span>

### <span data-ttu-id="b4909-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4909-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4909-106">UX</span><span class="sxs-lookup"><span data-stu-id="b4909-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4909-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4909-107">DESCRIPTION</span></span>
<span data-ttu-id="b4909-108">**New-Azutalep Ickvm** cmdlet 'i, bir Azure sanal makinesini yapılandırır ve oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="b4909-109">Bu cmdlet, bir sanal makineyi mevcut bir Azure hizmetine dağıtabilir.</span><span class="sxs-lookup"><span data-stu-id="b4909-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="b4909-110">Bu cmdlet, alternatif olarak yeni sanal makineyi barındıran bir Azure hizmeti oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="b4909-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="b4909-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4909-111">EXAMPLES</span></span>

### <span data-ttu-id="b4909-112">Örnek 1: sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4909-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="b4909-113">Bu komut, var olan hizmette Windows işletim sistemini çalıştıran bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="b4909-114">Cmdlet, sanal makineyi belirtilen görüntüde temel alır.</span><span class="sxs-lookup"><span data-stu-id="b4909-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="b4909-115">Komut, *Waitforboot* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="b4909-116">Bu nedenle, cmdlet sanal makinenin başlamasını bekler.</span><span class="sxs-lookup"><span data-stu-id="b4909-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="b4909-117">Örnek 2: sertifikaları kullanarak bir sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4909-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="b4909-118">İlk komut bir mağazadan sertifikaları alır ve $certs değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b4909-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="b4909-119">İkinci komut, bir yansımadan varolan bir hizmette Windows işletim sistemini çalıştıran bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="b4909-120">Varsayılan olarak, sanal makinede WinRM HTTPS dinleyicisi etkindir.</span><span class="sxs-lookup"><span data-stu-id="b4909-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="b4909-121">Komut, *Waitforboot* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="b4909-122">Bu nedenle, cmdlet sanal makinenin başlamasını bekler.</span><span class="sxs-lookup"><span data-stu-id="b4909-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="b4909-123">Komut, bir WinRM sertifikası yükler ve barındırılan hizmete X509Certificates.</span><span class="sxs-lookup"><span data-stu-id="b4909-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="b4909-124">Örnek 3: Linux işletim sistemini çalıştıran bir sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4909-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="b4909-125">Bu komut, bir resimden Linux işletim sistemini çalıştıran bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="b4909-126">Bu komut, yeni sanal makineyi barındırmak için bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="b4909-127">Komut, hizmetin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="b4909-128">Örnek 4: sanal makine oluşturma ve yeni sanal makineyi barındıracak bir hizmet oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4909-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="b4909-129">İlk komut **Get-AzureLocation** cmdlet 'ini kullanarak konumları alır ve bunları $Locations dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b4909-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="b4909-130">İkinci komut **Get-AzureVMImage** cmdlet 'ini kullanarak kullanılabilir resimleri alır ve bunları $Images dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b4909-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="b4909-131">Son komutu, VirtualMachine25 adında büyük bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="b4909-132">Sanal makine Windows işletim sistemini çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="b4909-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="b4909-133">$Images 'deki resimlerden birini temel alabilir.</span><span class="sxs-lookup"><span data-stu-id="b4909-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="b4909-134">Bu komut, yeni sanal makine için ContosoService03 adlı bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="b4909-135">Hizmet $Locations bir konumda.</span><span class="sxs-lookup"><span data-stu-id="b4909-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="b4909-136">Örnek 5: ayrılmış IP adına sahip bir sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="b4909-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="b4909-137">İlk komut konumlar alır ve $Locations dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b4909-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="b4909-138">İkinci komut kullanılabilir resimleri alır ve $Images dizi değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b4909-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="b4909-139">Son komutu, $Images resimlerden birini temel alan VirtualMachine27 adlı bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="b4909-140">Komut, $Locations konumda bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="b4909-141">Sanal makinenin, daha önce $ipName değişkeninde depolanan ayrılmış bir IP adı vardır.</span><span class="sxs-lookup"><span data-stu-id="b4909-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="b4909-142">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4909-142">PARAMETERS</span></span>

### <span data-ttu-id="b4909-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="b4909-143">-AdminUsername</span></span>
<span data-ttu-id="b4909-144">Bu cmdlet 'in sanal makinede oluşturduğu yönetici hesabının kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b4909-145">-AffinityGroup</span></span>
<span data-ttu-id="b4909-146">Sanal makine için benzeşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="b4909-147">Bu parametre veya *konum* parametresini yalnızca bu cmdlet sanal makine Için bir Azure hizmeti oluşturursa belirtin.</span><span class="sxs-lookup"><span data-stu-id="b4909-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-148">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="b4909-148">-AvailabilitySetName</span></span>
<span data-ttu-id="b4909-149">Bu cmdlet 'in sanal makineyi oluşturduğu kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-150">-Sertifikalar</span><span class="sxs-lookup"><span data-stu-id="b4909-150">-Certificates</span></span>
<span data-ttu-id="b4909-151">Bu cmdlet 'in hizmeti oluşturmak için kullandığı sertifikaların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-152">-Customveri dosyası</span><span class="sxs-lookup"><span data-stu-id="b4909-152">-CustomDataFile</span></span>
<span data-ttu-id="b4909-153">Sanal makine için bir veri dosyası belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="b4909-154">Bu cmdlet, dosyanın içeriğini Base64 olarak kodlar.</span><span class="sxs-lookup"><span data-stu-id="b4909-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="b4909-155">Dosya 64 kilobayt uzunluğundan az olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b4909-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="b4909-156">Konuk işletim sistemi Windows işletim sistemdeydi, bu cmdlet bu verileri%SYSTEMDRIVE%\AzureData\CustomData.bin. adlı bir ikili dosya olarak kaydeder</span><span class="sxs-lookup"><span data-stu-id="b4909-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="b4909-157">Konuk işletim sistemi Linux ise, bu cmdlet ovf-env.xml dosyasını kullanarak verileri geçirir.</span><span class="sxs-lookup"><span data-stu-id="b4909-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="b4909-158">Yükleme bu dosyayı/var/lib/waagent dizinine kopyalar.</span><span class="sxs-lookup"><span data-stu-id="b4909-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="b4909-159">Aracı Ayrıca,/var/lib/waagent/customdata'de Base64 Ile kodlanmış verileri depolar.</span><span class="sxs-lookup"><span data-stu-id="b4909-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="b4909-160">-DisableGuestAgent</span></span>
<span data-ttu-id="b4909-161">Bu cmdlet 'in altyapıyı hizmet olarak (IaaS) Konuk aracısını sağlayan şekilde devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4909-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="b4909-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="b4909-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="b4909-163">Bu cmdlet 'in HTTPS üzerinde Windows Uzaktan Yönetimi 'ni (WinRM) devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4909-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="b4909-164">Varsayılan olarak, HTTPS HTTPS üzerinden etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b4909-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="b4909-165">-DnsSettings</span></span>
<span data-ttu-id="b4909-166">Yeni dağıtımın DNS ayarlarını tanımlayan bir DNS sunucusu nesneleri dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="b4909-167">Bir **DNSServer** nesnesi oluşturmak Için, **New-AzureDns** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b4909-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="b4909-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="b4909-169">Bu cmdlet 'in HTTP üzerinden WinRM 'yi etkinleştirdiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4909-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="b4909-170">-HostCaching</span></span>
<span data-ttu-id="b4909-171">İşletim sistemi diskinin ana bilgisayar önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="b4909-172">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b4909-172">Valid values are:</span></span> 

- <span data-ttu-id="b4909-173">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="b4909-173">ReadOnly</span></span>
- <span data-ttu-id="b4909-174">Yazma</span><span class="sxs-lookup"><span data-stu-id="b4909-174">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-175">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="b4909-175">-ImageName</span></span>
<span data-ttu-id="b4909-176">İşletim sistemi disketini oluşturmak için bu cmdlet 'in kullandığı disk görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-177">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b4909-177">-InformationAction</span></span>
<span data-ttu-id="b4909-178">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4909-179">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b4909-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4909-180">'A</span><span class="sxs-lookup"><span data-stu-id="b4909-180">Continue</span></span>
- <span data-ttu-id="b4909-181">Manıza</span><span class="sxs-lookup"><span data-stu-id="b4909-181">Ignore</span></span>
- <span data-ttu-id="b4909-182">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b4909-182">Inquire</span></span>
- <span data-ttu-id="b4909-183">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b4909-183">SilentlyContinue</span></span>
- <span data-ttu-id="b4909-184">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b4909-184">Stop</span></span>
- <span data-ttu-id="b4909-185">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b4909-185">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-186">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b4909-186">-InformationVariable</span></span>
<span data-ttu-id="b4909-187">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-187">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-188">-Instancesize</span><span class="sxs-lookup"><span data-stu-id="b4909-188">-InstanceSize</span></span>
<span data-ttu-id="b4909-189">Örneğin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="b4909-190">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="b4909-190">Valid values are:</span></span> 

- <span data-ttu-id="b4909-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="b4909-191">ExtraSmall</span></span>
- <span data-ttu-id="b4909-192">Küçük</span><span class="sxs-lookup"><span data-stu-id="b4909-192">Small</span></span>
- <span data-ttu-id="b4909-193">Düzey</span><span class="sxs-lookup"><span data-stu-id="b4909-193">Medium</span></span>
- <span data-ttu-id="b4909-194">13</span><span class="sxs-lookup"><span data-stu-id="b4909-194">Large</span></span>
- <span data-ttu-id="b4909-195">Çok büyük</span><span class="sxs-lookup"><span data-stu-id="b4909-195">ExtraLarge</span></span>
- <span data-ttu-id="b4909-196">A5</span><span class="sxs-lookup"><span data-stu-id="b4909-196">A5</span></span>
- <span data-ttu-id="b4909-197">A6</span><span class="sxs-lookup"><span data-stu-id="b4909-197">A6</span></span>
- <span data-ttu-id="b4909-198">A7</span><span class="sxs-lookup"><span data-stu-id="b4909-198">A7</span></span>
- <span data-ttu-id="b4909-199">A8</span><span class="sxs-lookup"><span data-stu-id="b4909-199">A8</span></span>
- <span data-ttu-id="b4909-200">A9</span><span class="sxs-lookup"><span data-stu-id="b4909-200">A9</span></span>
- <span data-ttu-id="b4909-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="b4909-201">Basic_A0</span></span>
- <span data-ttu-id="b4909-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="b4909-202">Basic_A1</span></span>
- <span data-ttu-id="b4909-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="b4909-203">Basic_A2</span></span>
- <span data-ttu-id="b4909-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="b4909-204">Basic_A3</span></span>
- <span data-ttu-id="b4909-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="b4909-205">Basic_A4</span></span>
- <span data-ttu-id="b4909-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="b4909-206">Standard_D1</span></span>
- <span data-ttu-id="b4909-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="b4909-207">Standard_D2</span></span>
- <span data-ttu-id="b4909-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="b4909-208">Standard_D3</span></span>
- <span data-ttu-id="b4909-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="b4909-209">Standard_D4</span></span>
- <span data-ttu-id="b4909-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="b4909-210">Standard_D11</span></span>
- <span data-ttu-id="b4909-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="b4909-211">Standard_D12</span></span>
- <span data-ttu-id="b4909-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="b4909-212">Standard_D13</span></span>
- <span data-ttu-id="b4909-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="b4909-213">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="b4909-214">-Linux</span></span>
<span data-ttu-id="b4909-215">Bu cmdlet 'in Linux tabanlı bir sanal makine oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4909-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="b4909-216">-LinuxUser</span></span>
<span data-ttu-id="b4909-217">Bu cmdlet 'in sanal makinede oluşturduğu Linux yönetim hesabının kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-218">-Konum</span><span class="sxs-lookup"><span data-stu-id="b4909-218">-Location</span></span>
<span data-ttu-id="b4909-219">Sanal makineyi barındıran Azure veri merkezi 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="b4909-220">Bu parametreyi belirtirseniz, cmdlet belirtilen konumda bir Azure hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="b4909-221">Bu *parametreyi, yalnızca* bu cmdlet sanal makine Için bir Azure hizmeti oluşturursa belirtin.</span><span class="sxs-lookup"><span data-stu-id="b4909-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="b4909-222">-MediaLocation</span></span>
<span data-ttu-id="b4909-223">Bu cmdlet 'in sanal makineler disklerini oluşturduğu Azure depolama konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-224">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4909-224">-Name</span></span>
<span data-ttu-id="b4909-225">Bu cmdlet 'in oluşturduğu sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="b4909-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="b4909-227">Bu yapılandırmanın özel anahtarı yükleymediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-228">-Nowinrmenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="b4909-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="b4909-229">Bu cmdlet 'in sanal makine için WinRM uç noktası eklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4909-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-230">-Parola</span><span class="sxs-lookup"><span data-stu-id="b4909-230">-Password</span></span>
<span data-ttu-id="b4909-231">Yönetim hesabının parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-231">Specifies the password for the administrative account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-232">-Profil</span><span class="sxs-lookup"><span data-stu-id="b4909-232">-Profile</span></span>
<span data-ttu-id="b4909-233">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4909-234">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b4909-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-235">-Rezervedıpname</span><span class="sxs-lookup"><span data-stu-id="b4909-235">-ReservedIPName</span></span>
<span data-ttu-id="b4909-236">Ayrılmış IP adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-236">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-237">-Smardnsfqdn</span><span class="sxs-lookup"><span data-stu-id="b4909-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="b4909-238">Geriye doğru DNS arama için tam nitelikli etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-239">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="b4909-239">-ServiceName</span></span>
<span data-ttu-id="b4909-240">Bu cmdlet 'in yeni sanal makineyi eklediği yeni veya mevcut bir Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="b4909-241">Yeni bir hizmet belirtirseniz, bu cmdlet 'ler bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4909-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="b4909-242">Yeni hizmet oluşturmak için *konum* veya *affinitygroup* parametresini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b4909-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="b4909-243">Var olan bir hizmet belirtirseniz, *konum* veya *affinitygroup* belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="b4909-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="b4909-244">-SSHKeyPairs</span></span>
<span data-ttu-id="b4909-245">SSH anahtar çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-245">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="b4909-246">-SSHPublicKeys</span></span>
<span data-ttu-id="b4909-247">SSH ortak anahtarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-247">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="b4909-248">-SubnetNames</span></span>
<span data-ttu-id="b4909-249">Sanal makine için alt ağ adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-250">-Vağ adı</span><span class="sxs-lookup"><span data-stu-id="b4909-250">-VNetName</span></span>
<span data-ttu-id="b4909-251">Sanal makine için sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-251">Specifies the name of a virtual network for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="b4909-252">-WaitForBoot</span></span>
<span data-ttu-id="b4909-253">Bu cmdlet 'in sanal makinenin State ReadyRole ulaşmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4909-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="b4909-254">Sanal makine aşağıdaki durumlardan birine ulaşırsa cmdlet başarısız olur: FailedStartingVM, ProvisioningFailed veya ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="b4909-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="b4909-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="b4909-255">-Windows</span></span>
<span data-ttu-id="b4909-256">Bu cmdlet 'in Windows sanal makinesini oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4909-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-257">-Winrmcercertificate</span><span class="sxs-lookup"><span data-stu-id="b4909-257">-WinRMCertificate</span></span>
<span data-ttu-id="b4909-258">Bu cmdlet 'in bir WinRM uç noktasına ilişki kurduğu sertifikayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="b4909-259">-X509Certificates</span></span>
<span data-ttu-id="b4909-260">Barındırılan bir hizmete dağıtılan x509 sertifikalarının dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4909-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4909-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4909-261">CommonParameters</span></span>
<span data-ttu-id="b4909-262">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4909-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4909-263">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4909-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4909-264">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4909-264">INPUTS</span></span>

## <span data-ttu-id="b4909-265">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4909-265">OUTPUTS</span></span>

## <span data-ttu-id="b4909-266">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4909-266">NOTES</span></span>

## <span data-ttu-id="b4909-267">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4909-267">RELATED LINKS</span></span>

[<span data-ttu-id="b4909-268">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="b4909-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="b4909-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="b4909-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="b4909-270">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b4909-270">New-AzureDns</span></span>](./New-AzureDns.md)


