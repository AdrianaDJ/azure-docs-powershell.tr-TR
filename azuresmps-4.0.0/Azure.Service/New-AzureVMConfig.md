---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106197"
---
# <span data-ttu-id="1a54a-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="1a54a-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="1a54a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a54a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a54a-103">Azure sanal makine yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a54a-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="1a54a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a54a-104">SYNTAX</span></span>

### <span data-ttu-id="1a54a-105">GörüntüAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a54a-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1a54a-106">DiskName</span><span class="sxs-lookup"><span data-stu-id="1a54a-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1a54a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a54a-107">DESCRIPTION</span></span>
<span data-ttu-id="1a54a-108">**New-AzureVMConfig** cmdlet 'ı bir Azure sanal makine yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a54a-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="1a54a-109">Bu nesneyi yeni bir dağıtım gerçekleştirmek ve var olan dağıtıma yeni bir sanal makine eklemek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1a54a-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="1a54a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a54a-110">EXAMPLES</span></span>

### <span data-ttu-id="1a54a-111">Örnek 1: Windows sanal makine yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a54a-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="1a54a-112">Bu komut, işletim sistemi diski, veri diski ve sağlama yapılandırması olan bir Windows sanal makine yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a54a-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="1a54a-113">Bu yapılandırma, yeni sanal makine oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a54a-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="1a54a-114">Örnek 2: Linux sanal makine yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="1a54a-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="1a54a-115">Bu komut, işletim sistemi diski, veri diski ve sağlama yapılandırması ile yeni bir Linux sanal makine yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1a54a-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="1a54a-116">Bu yapılandırma, yeni sanal makine oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1a54a-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="1a54a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a54a-117">PARAMETERS</span></span>

### <span data-ttu-id="1a54a-118">-Kullanılabilirlik</span><span class="sxs-lookup"><span data-stu-id="1a54a-118">-AvailabilitySetName</span></span>
<span data-ttu-id="1a54a-119">Kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="1a54a-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="1a54a-121">Yapılandırmanın önyükleme tanılaması 'nı devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="1a54a-122">Varsayılan olarak, sanal makinede önyükleme tanılaması etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

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

### <span data-ttu-id="1a54a-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="1a54a-123">-DiskLabel</span></span>
<span data-ttu-id="1a54a-124">İşletim sistemi diskinin etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-125">-DiskName</span><span class="sxs-lookup"><span data-stu-id="1a54a-125">-DiskName</span></span>
<span data-ttu-id="1a54a-126">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="1a54a-127">-HostCaching</span></span>
<span data-ttu-id="1a54a-128">İşletim sistemi diskinin ana bilgisayar önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="1a54a-129">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="1a54a-129">Valid values are:</span></span>

- <span data-ttu-id="1a54a-130">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="1a54a-130">ReadOnly</span></span>
- <span data-ttu-id="1a54a-131">Yazma</span><span class="sxs-lookup"><span data-stu-id="1a54a-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-132">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="1a54a-132">-ImageName</span></span>
<span data-ttu-id="1a54a-133">İşletim sistemi diski için kullanılacak sanal makine görüntüsünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-134">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1a54a-134">-InformationAction</span></span>
<span data-ttu-id="1a54a-135">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1a54a-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1a54a-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a54a-137">'A</span><span class="sxs-lookup"><span data-stu-id="1a54a-137">Continue</span></span>
- <span data-ttu-id="1a54a-138">Manıza</span><span class="sxs-lookup"><span data-stu-id="1a54a-138">Ignore</span></span>
- <span data-ttu-id="1a54a-139">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="1a54a-139">Inquire</span></span>
- <span data-ttu-id="1a54a-140">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="1a54a-140">SilentlyContinue</span></span>
- <span data-ttu-id="1a54a-141">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="1a54a-141">Stop</span></span>
- <span data-ttu-id="1a54a-142">Biliriz</span><span class="sxs-lookup"><span data-stu-id="1a54a-142">Suspend</span></span>

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

### <span data-ttu-id="1a54a-143">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="1a54a-143">-InformationVariable</span></span>
<span data-ttu-id="1a54a-144">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1a54a-145">-Instancesize</span><span class="sxs-lookup"><span data-stu-id="1a54a-145">-InstanceSize</span></span>
<span data-ttu-id="1a54a-146">Örneğin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="1a54a-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1a54a-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a54a-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="1a54a-148">ExtraSmall</span></span>
- <span data-ttu-id="1a54a-149">Küçük</span><span class="sxs-lookup"><span data-stu-id="1a54a-149">Small</span></span>
- <span data-ttu-id="1a54a-150">Düzey</span><span class="sxs-lookup"><span data-stu-id="1a54a-150">Medium</span></span>
- <span data-ttu-id="1a54a-151">13</span><span class="sxs-lookup"><span data-stu-id="1a54a-151">Large</span></span>
- <span data-ttu-id="1a54a-152">Çok büyük</span><span class="sxs-lookup"><span data-stu-id="1a54a-152">ExtraLarge</span></span>
- <span data-ttu-id="1a54a-153">A5</span><span class="sxs-lookup"><span data-stu-id="1a54a-153">A5</span></span>
- <span data-ttu-id="1a54a-154">A6</span><span class="sxs-lookup"><span data-stu-id="1a54a-154">A6</span></span>
- <span data-ttu-id="1a54a-155">A7</span><span class="sxs-lookup"><span data-stu-id="1a54a-155">A7</span></span>
- <span data-ttu-id="1a54a-156">A8</span><span class="sxs-lookup"><span data-stu-id="1a54a-156">A8</span></span>
- <span data-ttu-id="1a54a-157">A9</span><span class="sxs-lookup"><span data-stu-id="1a54a-157">A9</span></span>
- <span data-ttu-id="1a54a-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="1a54a-158">Basic_A0</span></span>
- <span data-ttu-id="1a54a-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="1a54a-159">Basic_A1</span></span>
- <span data-ttu-id="1a54a-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="1a54a-160">Basic_A2</span></span>
- <span data-ttu-id="1a54a-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="1a54a-161">Basic_A3</span></span>
- <span data-ttu-id="1a54a-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="1a54a-162">Basic_A4</span></span>
- <span data-ttu-id="1a54a-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="1a54a-163">Standard_D1</span></span>
- <span data-ttu-id="1a54a-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="1a54a-164">Standard_D2</span></span>
- <span data-ttu-id="1a54a-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="1a54a-165">Standard_D3</span></span>
- <span data-ttu-id="1a54a-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="1a54a-166">Standard_D4</span></span>
- <span data-ttu-id="1a54a-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="1a54a-167">Standard_D11</span></span>
- <span data-ttu-id="1a54a-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="1a54a-168">Standard_D12</span></span>
- <span data-ttu-id="1a54a-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="1a54a-169">Standard_D13</span></span>
- <span data-ttu-id="1a54a-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="1a54a-170">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-171">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1a54a-171">-Label</span></span>
<span data-ttu-id="1a54a-172">Sanal makineye atanacak bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-172">Specifies a label to assign to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="1a54a-173">-LicenseType</span></span>
<span data-ttu-id="1a54a-174">Şirket içi lisansa sahip bir yansıma veya disk için lisans türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="1a54a-175">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1a54a-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1a54a-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="1a54a-176">Windows_Client</span></span>
- <span data-ttu-id="1a54a-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="1a54a-177">Windows_Server</span></span> 

<span data-ttu-id="1a54a-178">Bu parametreyi yalnızca Windows Server işletim sistemi içeren resimler için belirtin.</span><span class="sxs-lookup"><span data-stu-id="1a54a-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

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

### <span data-ttu-id="1a54a-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="1a54a-179">-MediaLocation</span></span>
<span data-ttu-id="1a54a-180">Yeni sanal makine diskinin Azure depolama konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-181">-Ad</span><span class="sxs-lookup"><span data-stu-id="1a54a-181">-Name</span></span>
<span data-ttu-id="1a54a-182">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a54a-183">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a54a-183">-Profile</span></span>
<span data-ttu-id="1a54a-184">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a54a-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a54a-185">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1a54a-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a54a-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a54a-186">CommonParameters</span></span>
<span data-ttu-id="1a54a-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a54a-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a54a-188">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a54a-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a54a-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a54a-189">INPUTS</span></span>

## <span data-ttu-id="1a54a-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a54a-190">OUTPUTS</span></span>

## <span data-ttu-id="1a54a-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a54a-191">NOTES</span></span>

## <span data-ttu-id="1a54a-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a54a-192">RELATED LINKS</span></span>

