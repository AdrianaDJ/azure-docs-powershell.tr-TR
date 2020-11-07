---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 6d5731916309baf93552f9b5d71f30943178f11c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761313"
---
# <span data-ttu-id="f1e58-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f1e58-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="f1e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e58-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e58-103">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="f1e58-103">Create a gallery image version.</span></span>

## <span data-ttu-id="f1e58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1e58-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e58-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1e58-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e58-106">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="f1e58-106">Create a gallery image version.</span></span>

## <span data-ttu-id="f1e58-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1e58-107">EXAMPLES</span></span>

### <span data-ttu-id="f1e58-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1e58-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="f1e58-109">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="f1e58-109">Create a gallery image version.</span></span>

## <span data-ttu-id="f1e58-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1e58-110">PARAMETERS</span></span>

### <span data-ttu-id="f1e58-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f1e58-111">-AsJob</span></span>
<span data-ttu-id="f1e58-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f1e58-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1e58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e58-113">-DefaultProfile</span></span>
<span data-ttu-id="f1e58-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1e58-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1e58-115">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="f1e58-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="f1e58-116">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="f1e58-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-117">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="f1e58-117">-GalleryName</span></span>
<span data-ttu-id="f1e58-118">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="f1e58-118">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="f1e58-119">-Location</span></span>
<span data-ttu-id="f1e58-120">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="f1e58-120">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1e58-121">-Name</span></span>
<span data-ttu-id="f1e58-122">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="f1e58-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-123">-Publishingprofileendofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="f1e58-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="f1e58-124">Galeri görüntüsünün sürümünün kullanım tarihi.</span><span class="sxs-lookup"><span data-stu-id="f1e58-124">The end of life date of the gallery Image Version.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="f1e58-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="f1e58-126">Ayarlanmışsa, görüntü tanımının en son sürümünden dağıtılan sanal makineler bu görüntü sürümünü kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="f1e58-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="f1e58-127">-ReplicaCount</span></span>
<span data-ttu-id="f1e58-128">Bölge başına oluşturulacak görüntü sürümünün yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="f1e58-128">The number of replicas of the Image Version to be created per region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e58-129">-ResourceGroupName</span></span>
<span data-ttu-id="f1e58-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f1e58-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-131">-Sourceımageıd</span><span class="sxs-lookup"><span data-stu-id="f1e58-131">-SourceImageId</span></span>
<span data-ttu-id="f1e58-132">Görüntü sürümünün oluşturulduğu kaynak görüntünün KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="f1e58-132">The ID of the source image from which the Image Version is going to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f1e58-133">-Tag</span></span>
<span data-ttu-id="f1e58-134">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="f1e58-134">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="f1e58-135">-TargetRegion</span></span>
<span data-ttu-id="f1e58-136">Görüntü sürümünün çoğaltılacağı hedef bölgeler.</span><span class="sxs-lookup"><span data-stu-id="f1e58-136">The target regions where the Image Version is going to be replicated to.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1e58-137">-Confirm</span></span>
<span data-ttu-id="f1e58-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1e58-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e58-139">-WhatIf</span></span>
<span data-ttu-id="f1e58-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1e58-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1e58-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1e58-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e58-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e58-142">CommonParameters</span></span>
<span data-ttu-id="f1e58-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1e58-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e58-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e58-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e58-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1e58-145">INPUTS</span></span>

### <span data-ttu-id="f1e58-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f1e58-146">System.String</span></span>

### <span data-ttu-id="f1e58-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f1e58-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f1e58-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="f1e58-148">System.Int32</span></span>

### <span data-ttu-id="f1e58-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f1e58-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f1e58-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="f1e58-150">System.DateTime</span></span>

### <span data-ttu-id="f1e58-151">System. topluluklar. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="f1e58-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="f1e58-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1e58-152">OUTPUTS</span></span>

### <span data-ttu-id="f1e58-153">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="f1e58-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="f1e58-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1e58-154">NOTES</span></span>

## <span data-ttu-id="f1e58-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1e58-155">RELATED LINKS</span></span>
