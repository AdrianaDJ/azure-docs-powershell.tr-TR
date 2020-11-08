---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5544F2E2-27EF-4079-8E13-6B85DF2018A2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a71ad8b25a17c1c2933cdcf305ba0b53f67bf0f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106583"
---
# <span data-ttu-id="efacc-101">Update-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="efacc-101">Update-AzureVMImage</span></span>

## <span data-ttu-id="efacc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efacc-102">SYNOPSIS</span></span>
<span data-ttu-id="efacc-103">Görüntü deposundaki bir işletim sistemi görüntüsünün etiketini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efacc-103">Updates the label of an operating system image in the image repository.</span></span>

## <span data-ttu-id="efacc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="efacc-104">SYNTAX</span></span>

```
Update-AzureVMImage [-ImageName] <String> [-Label] <String> [[-Eula] <String>] [[-Description] <String>]
 [[-ImageFamily] <String>] [[-PublishedDate] <DateTime>] [[-PrivacyUri] <Uri>] [[-RecommendedVMSize] <String>]
 [[-DiskConfig] <VirtualMachineImageDiskConfigSet>] [[-Language] <String>] [[-IconName] <String>]
 [[-SmallIconName] <String>] [-DontShowInGui] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="efacc-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="efacc-105">DESCRIPTION</span></span>
<span data-ttu-id="efacc-106">**Update-AzureVMImage** cmdlet 'i, görüntü deposundaki bir işletim sistemi görüntüsünün etiketini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efacc-106">The **Update-AzureVMImage** cmdlet updates the label on an operating system image in the image repository.</span></span>
<span data-ttu-id="efacc-107">Güncellenmiş resim hakkında bilgi içeren bir resim nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="efacc-107">It returns an image object with information about the updated image.</span></span>

## <span data-ttu-id="efacc-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="efacc-108">EXAMPLES</span></span>

### <span data-ttu-id="efacc-109">Örnek 1: resim etiketini değiştirerek görüntü güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="efacc-109">Example 1: Update an image by changing the image label</span></span>
```
PS C:\> Update-AzureVMImage -ImageName "Windows-Server-2008-SP2" -Label "DoNotUse"
```

<span data-ttu-id="efacc-110">Bu komut, resim etiketini DoNotUse olarak değiştirerek Windows-Server-2008-SP2 adlı yansımayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="efacc-110">This command updates the image named Windows-Server-2008-SP2 by changing the image label to DoNotUse.</span></span>

### <span data-ttu-id="efacc-111">Örnek 2: tüm işletim sistemlerini etikete göre alın ve etiketi güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="efacc-111">Example 2: Get all operating systems by label and then update the label</span></span>
```
PS C:\> Get-AzureVMImage | Where-Object {$_.Label -eq "DoNotUse" } | Update-AzureVMImage -Label "Updated"
```

<span data-ttu-id="efacc-112">Bu komut, DoNotUse etiketli tüm işletim sistemi resimlerini alır ve etiketi güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="efacc-112">This command gets all the operating system images labeled DoNotUse and changes the label to Updated.</span></span>

## <span data-ttu-id="efacc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="efacc-113">PARAMETERS</span></span>

### <span data-ttu-id="efacc-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="efacc-114">-Description</span></span>
<span data-ttu-id="efacc-115">İşletim sistemi görüntüsünün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-115">Specifies the description of the operating system image.</span></span>

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

### <span data-ttu-id="efacc-116">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="efacc-116">-DiskConfig</span></span>
<span data-ttu-id="efacc-117">**New-AzureVMImageDiskConfigSet** , **set-AzureVMImageOSDiskConfig** ve **set-AzureVMImageDataDiskConfig** cmdlet 'lerini kullanarak oluşturulan sanal makine görüntüsünün işletim sistemi diskini ve veri diski yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-117">Specifies the operating system disk and data disk configuration for the virtual machine image created by using the **New-AzureVMImageDiskConfigSet** , **Set-AzureVMImageOSDiskConfig** , and **Set-AzureVMImageDataDiskConfig** cmdlets.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efacc-118">-DontShowInGui</span><span class="sxs-lookup"><span data-stu-id="efacc-118">-DontShowInGui</span></span>
<span data-ttu-id="efacc-119">Bu cmdlet 'in GUI 'deki resmi göstermediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-119">Indicates that this cmdlet does not show the image in the GUI.</span></span>

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

### <span data-ttu-id="efacc-120">-EULA</span><span class="sxs-lookup"><span data-stu-id="efacc-120">-Eula</span></span>
<span data-ttu-id="efacc-121">Son Kullanıcı Lisans anlaşmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-121">Specifies the End User License Agreement.</span></span>
<span data-ttu-id="efacc-122">Değerin URL olmasını öneririz.</span><span class="sxs-lookup"><span data-stu-id="efacc-122">We recommend that the value is a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efacc-123">-IconName</span><span class="sxs-lookup"><span data-stu-id="efacc-123">-IconName</span></span>
<span data-ttu-id="efacc-124">İşletim sisteminin veya sanal makine görüntüsünün standart simge adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-124">Specifies the standard icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="efacc-125">-Imagefamily</span><span class="sxs-lookup"><span data-stu-id="efacc-125">-ImageFamily</span></span>
<span data-ttu-id="efacc-126">İşletim sistemi veya sanal makine resimlerini gruplandırmak için kullanılabilecek bir değer belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-126">Specifies a value that can be used to group operating system or virtual machine images.</span></span>

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

### <span data-ttu-id="efacc-127">-GörüntüAdı</span><span class="sxs-lookup"><span data-stu-id="efacc-127">-ImageName</span></span>
<span data-ttu-id="efacc-128">Görüntü deposundaki, güncelleştirilecek resmin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-128">Specifies the name of the image to update in the image repository.</span></span>

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

### <span data-ttu-id="efacc-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="efacc-129">-InformationAction</span></span>
<span data-ttu-id="efacc-130">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="efacc-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="efacc-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="efacc-132">'A</span><span class="sxs-lookup"><span data-stu-id="efacc-132">Continue</span></span>
- <span data-ttu-id="efacc-133">Manıza</span><span class="sxs-lookup"><span data-stu-id="efacc-133">Ignore</span></span>
- <span data-ttu-id="efacc-134">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="efacc-134">Inquire</span></span>
- <span data-ttu-id="efacc-135">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="efacc-135">SilentlyContinue</span></span>
- <span data-ttu-id="efacc-136">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="efacc-136">Stop</span></span>
- <span data-ttu-id="efacc-137">Biliriz</span><span class="sxs-lookup"><span data-stu-id="efacc-137">Suspend</span></span>

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

### <span data-ttu-id="efacc-138">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="efacc-138">-InformationVariable</span></span>
<span data-ttu-id="efacc-139">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="efacc-140">Etiketli</span><span class="sxs-lookup"><span data-stu-id="efacc-140">-Label</span></span>
<span data-ttu-id="efacc-141">Resmin yeni etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-141">Specifies the new label of the image.</span></span>

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

### <span data-ttu-id="efacc-142">-Dil</span><span class="sxs-lookup"><span data-stu-id="efacc-142">-Language</span></span>
<span data-ttu-id="efacc-143">Sanal makine veya işletim sistemi yansımasındaki işletim sisteminin dilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-143">Specifies the language for the operating system in the virtual machine or operating system image.</span></span>

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

### <span data-ttu-id="efacc-144">-PrivacyUri</span><span class="sxs-lookup"><span data-stu-id="efacc-144">-PrivacyUri</span></span>
<span data-ttu-id="efacc-145">İşletim sistemi görüntüsüyle ilgili gizlilik ilkesini içeren bir belgeyi gösteren URI 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-145">Specifies the URI that points to a document that contains the privacy policy related to the operating system image.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efacc-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="efacc-146">-Profile</span></span>
<span data-ttu-id="efacc-147">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="efacc-148">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="efacc-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="efacc-149">-PublishedDate</span><span class="sxs-lookup"><span data-stu-id="efacc-149">-PublishedDate</span></span>
<span data-ttu-id="efacc-150">İşletim sistemi görüntüsünün görüntü deposuna eklendiği tarihi belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-150">Specifies the date when the operating system image was added to the image repository.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efacc-151">-RecommendedVMSize</span><span class="sxs-lookup"><span data-stu-id="efacc-151">-RecommendedVMSize</span></span>
<span data-ttu-id="efacc-152">Sanal makinenin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-152">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="efacc-153">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="efacc-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="efacc-154">Düzey</span><span class="sxs-lookup"><span data-stu-id="efacc-154">Medium</span></span>
- <span data-ttu-id="efacc-155">13</span><span class="sxs-lookup"><span data-stu-id="efacc-155">Large</span></span>
- <span data-ttu-id="efacc-156">Çok büyük</span><span class="sxs-lookup"><span data-stu-id="efacc-156">ExtraLarge</span></span>
- <span data-ttu-id="efacc-157">A5</span><span class="sxs-lookup"><span data-stu-id="efacc-157">A5</span></span>
- <span data-ttu-id="efacc-158">A6</span><span class="sxs-lookup"><span data-stu-id="efacc-158">A6</span></span>
- <span data-ttu-id="efacc-159">A7</span><span class="sxs-lookup"><span data-stu-id="efacc-159">A7</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efacc-160">-Smallıconname</span><span class="sxs-lookup"><span data-stu-id="efacc-160">-SmallIconName</span></span>
<span data-ttu-id="efacc-161">İşletim sisteminin veya sanal makine görüntüsünün küçük simge adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="efacc-161">Specifies the small icon name for the operating system or virtual machine image.</span></span>

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

### <span data-ttu-id="efacc-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efacc-162">CommonParameters</span></span>
<span data-ttu-id="efacc-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="efacc-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efacc-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efacc-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efacc-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="efacc-165">INPUTS</span></span>

## <span data-ttu-id="efacc-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="efacc-166">OUTPUTS</span></span>

### <span data-ttu-id="efacc-167">Içerik</span><span class="sxs-lookup"><span data-stu-id="efacc-167">OSImageContext</span></span>

## <span data-ttu-id="efacc-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="efacc-168">NOTES</span></span>

## <span data-ttu-id="efacc-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="efacc-169">RELATED LINKS</span></span>

[<span data-ttu-id="efacc-170">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="efacc-170">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="efacc-171">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="efacc-171">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="efacc-172">Remove-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="efacc-172">Remove-AzureVMImage</span></span>](./Remove-AzureVMImage.md)

[<span data-ttu-id="efacc-173">Save-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="efacc-173">Save-AzureVMImage</span></span>](./Save-AzureVMImage.md)

[<span data-ttu-id="efacc-174">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="efacc-174">New-AzureVMImageDiskConfigSet</span></span>](./New-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="efacc-175">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="efacc-175">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="efacc-176">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="efacc-176">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


