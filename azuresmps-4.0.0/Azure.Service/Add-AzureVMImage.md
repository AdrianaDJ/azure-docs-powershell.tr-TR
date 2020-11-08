---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DECCEE-86C8-4662-9ED0-D1BDB4E687C2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68efd1c750646abffa90eb8318d0df189a4c9eb9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105715"
---
# <span data-ttu-id="7545d-101">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7545d-101">Add-AzureVMImage</span></span>

## <span data-ttu-id="7545d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7545d-102">SYNOPSIS</span></span>
<span data-ttu-id="7545d-103">Görüntü deposuna yeni bir işletim sistemi görüntüsü veya yeni bir sanal makine görüntüsü ekler.</span><span class="sxs-lookup"><span data-stu-id="7545d-103">Adds a new operating system image or a new virtual machine image to the image repository.</span></span>

## <span data-ttu-id="7545d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7545d-104">SYNTAX</span></span>

### <span data-ttu-id="7545d-105">OSImage (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7545d-105">OSImage (Default)</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-MediaLocation] <String> [-OS] <String> [[-Label] <String>]
 [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>]
 [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>] [[-SmallIconName] <String>]
 [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7545d-106">Vmımage</span><span class="sxs-lookup"><span data-stu-id="7545d-106">VMImage</span></span>
```
Add-AzureVMImage [-ImageName] <String> [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-OS] <String>]
 [[-Label] <String>] [[-Eula] <String>] [[-Description] <String>] [[-ImageFamily] <String>]
 [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-ShowInGui] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7545d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7545d-107">DESCRIPTION</span></span>
<span data-ttu-id="7545d-108">**Add-AzureVMImage** cmdlet 'i, görüntü deposuna yeni bir işletim sistemi görüntüsü veya yeni bir sanal makine görüntüsü ekler.</span><span class="sxs-lookup"><span data-stu-id="7545d-108">The **Add-AzureVMImage** cmdlet adds a new operating system image or a new virtual machine image to the image repository.</span></span>
<span data-ttu-id="7545d-109">Görüntü, Windows için Sysprep veya Linux için, dağıtım için uygun aracı kullanarak genelleştirilmiş bir işletim sistemi yansıdır.</span><span class="sxs-lookup"><span data-stu-id="7545d-109">The image is a generalized operating system image, using either Sysprep for Windows or, for Linux, using the appropriate tool for the distribution.</span></span>

## <span data-ttu-id="7545d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7545d-110">EXAMPLES</span></span>

### <span data-ttu-id="7545d-111">Örnek 1: depoya işletim sistemi görüntüsü ekleme</span><span class="sxs-lookup"><span data-stu-id="7545d-111">Example 1: Add an operating system image to the repository</span></span>
```
PS C:\> $S = New-AzureVMImageDiskConfigSet
PS C:\> Set-AzureVMImageOSDiskConfig -DiskConfig $S -HostCaching ReadWrite -OSState "Generalized" -OS "Windows" -MediaLink $Link
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test1" -HostCaching ReadWrite -Lun 0 -MediaLink $Link1
PS C:\> Set-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4" -HostCaching ReadWrite -Lun 0 -MediaLink $Link
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $S -DataDiskName "Test4"
PS C:\> $IMGName = "TestCREATEvmimage2";
PS C:\> Add-AzureVMImage -ImageName $IMGName -Label "Test1" -Description "Test1" -DiskConfig $S -Eula "http://www.contoso.com" -ImageFamily Windows -PublishedDate (Get-Date) -PrivacyUri "http://www.test.com" -RecommendedVMSize Small -IconName "Icon01" -SmallIconName "SmallIcon01" -ShowInGui
```

<span data-ttu-id="7545d-112">Bu örnek, depoya bir işletim sistemi görüntüsü ekler.</span><span class="sxs-lookup"><span data-stu-id="7545d-112">This example adds an operating system image to the repository.</span></span>

## <span data-ttu-id="7545d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7545d-113">PARAMETERS</span></span>

### <span data-ttu-id="7545d-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="7545d-114">-Description</span></span>
<span data-ttu-id="7545d-115">İşletim sistemi görüntüsünün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-115">Specifies the description of the operating system image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="7545d-116">-DiskConfig</span></span>
<span data-ttu-id="7545d-117">Sanal makine görüntüsünün işletim sistemi disk yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-117">Specifies the operating system disk configuration for the virtual machine image.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: VMImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-118">-EULA</span><span class="sxs-lookup"><span data-stu-id="7545d-118">-Eula</span></span>
<span data-ttu-id="7545d-119">Son Kullanıcı Lisans anlaşmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-119">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="7545d-120">Bu değer için bir URL kullanmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="7545d-120">It is recommended that you use an URL for this value.</span></span>

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

### <span data-ttu-id="7545d-121">-IconName</span><span class="sxs-lookup"><span data-stu-id="7545d-121">-IconName</span></span>
<span data-ttu-id="7545d-122">Görüntü depoya eklendiğinde kullanılan simgenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-122">Specifies the name of the icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IconUri

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-123">-Imagefamily</span><span class="sxs-lookup"><span data-stu-id="7545d-123">-ImageFamily</span></span>
<span data-ttu-id="7545d-124">İşletim sistemi resimlerini gruplandırmak için kullanılan bir değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-124">Specifies a value that is used to group operating system images.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-125">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="7545d-125">-ImageName</span></span>
<span data-ttu-id="7545d-126">Görüntü deposuna eklenen resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-126">Specifies the name of the image being added to the image repository.</span></span>

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

### <span data-ttu-id="7545d-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="7545d-127">-InformationAction</span></span>
<span data-ttu-id="7545d-128">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7545d-129">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7545d-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7545d-130">'A</span><span class="sxs-lookup"><span data-stu-id="7545d-130">Continue</span></span>
- <span data-ttu-id="7545d-131">Manıza</span><span class="sxs-lookup"><span data-stu-id="7545d-131">Ignore</span></span>
- <span data-ttu-id="7545d-132">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="7545d-132">Inquire</span></span>
- <span data-ttu-id="7545d-133">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="7545d-133">SilentlyContinue</span></span>
- <span data-ttu-id="7545d-134">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="7545d-134">Stop</span></span>
- <span data-ttu-id="7545d-135">Biliriz</span><span class="sxs-lookup"><span data-stu-id="7545d-135">Suspend</span></span>

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

### <span data-ttu-id="7545d-136">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="7545d-136">-InformationVariable</span></span>
<span data-ttu-id="7545d-137">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7545d-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7545d-138">-Label</span></span>
<span data-ttu-id="7545d-139">Resme vermek için bir etiket belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-139">Specifies a label to give the image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-140">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="7545d-140">-MediaLocation</span></span>
<span data-ttu-id="7545d-141">Resmin bulunduğu fiziksel blob sayfasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-141">Specifies the location of the physical blob page where the image resides.</span></span>
<span data-ttu-id="7545d-142">Bu, geçerli aboneliğin depolama alanındaki blob sayfasına yönelik bir bağlantıdır.</span><span class="sxs-lookup"><span data-stu-id="7545d-142">This is a link to a blob page in the current subscription's storage.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-143">-İşletim sistemi</span><span class="sxs-lookup"><span data-stu-id="7545d-143">-OS</span></span>
<span data-ttu-id="7545d-144">Resmin işletim sistemi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-144">Specifies the operating system version of the image.</span></span>

```yaml
Type: String
Parameter Sets: OSImage
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: VMImage
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-145">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="7545d-145">-PrivacyUri</span></span>
<span data-ttu-id="7545d-146">İşletim sistemi görüntüsüyle ilgili gizlilik ilkesini içeren bir belgeyi gösteren URL 'YI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-146">Specifies the URL that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="7545d-147">-Profile</span></span>
<span data-ttu-id="7545d-148">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7545d-149">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="7545d-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7545d-150">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="7545d-150">-PublishedDate</span></span>
<span data-ttu-id="7545d-151">İşletim sistemi görüntüsünün görüntü deposuna eklendiği tarihi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-151">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-152">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="7545d-152">-RecommendedVMSize</span></span>
<span data-ttu-id="7545d-153">İşletim sistemi görüntüsünden oluşturulan sanal makine için kullanılacak boyutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-153">Specifies the size to use for the virtual machine that is created from the operating system image.</span></span>

<span data-ttu-id="7545d-154">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7545d-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7545d-155">Düzey</span><span class="sxs-lookup"><span data-stu-id="7545d-155">Medium</span></span>
- <span data-ttu-id="7545d-156">13</span><span class="sxs-lookup"><span data-stu-id="7545d-156">Large</span></span>
- <span data-ttu-id="7545d-157">Çok büyük</span><span class="sxs-lookup"><span data-stu-id="7545d-157">ExtraLarge</span></span>
- <span data-ttu-id="7545d-158">A5</span><span class="sxs-lookup"><span data-stu-id="7545d-158">A5</span></span>
- <span data-ttu-id="7545d-159">A6</span><span class="sxs-lookup"><span data-stu-id="7545d-159">A6</span></span>
- <span data-ttu-id="7545d-160">A7</span><span class="sxs-lookup"><span data-stu-id="7545d-160">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-161">-Showınguı</span><span class="sxs-lookup"><span data-stu-id="7545d-161">-ShowInGui</span></span>
<span data-ttu-id="7545d-162">Bu cmdlet 'in GUI 'deki resmi gösterir.</span><span class="sxs-lookup"><span data-stu-id="7545d-162">Indicates that this cmdlet shows the image in the GUI.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-163">-Smallıconname</span><span class="sxs-lookup"><span data-stu-id="7545d-163">-SmallIconName</span></span>
<span data-ttu-id="7545d-164">Görüntü depoya eklendiğinde kullanılan küçük simgenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7545d-164">Specifies the name of the small icon that is used when the image is added to the repository.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmallIconUri

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7545d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7545d-165">CommonParameters</span></span>
<span data-ttu-id="7545d-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7545d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7545d-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7545d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7545d-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7545d-168">INPUTS</span></span>

## <span data-ttu-id="7545d-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7545d-169">OUTPUTS</span></span>

### <span data-ttu-id="7545d-170">Içerik</span><span class="sxs-lookup"><span data-stu-id="7545d-170">OSImageContext</span></span>

## <span data-ttu-id="7545d-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7545d-171">NOTES</span></span>

## <span data-ttu-id="7545d-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7545d-172">RELATED LINKS</span></span>

[<span data-ttu-id="7545d-173">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7545d-173">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="7545d-174">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7545d-174">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="7545d-175">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7545d-175">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="7545d-176">Güncelleştirme-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="7545d-176">Update-AzureVMImage</span></span>](./Update-AzureVMImage.md)


