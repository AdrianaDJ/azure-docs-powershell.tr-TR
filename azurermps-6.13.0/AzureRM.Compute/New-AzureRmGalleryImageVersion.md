---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageVersion.md
ms.openlocfilehash: f27c861386e7a570fe72a5266362bee7fed39e5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764686"
---
# <span data-ttu-id="1f1b9-101">New-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="1f1b9-101">New-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="1f1b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="1f1b9-103">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-103">Create a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f1b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f1b9-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f1b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f1b9-105">DESCRIPTION</span></span>
<span data-ttu-id="1f1b9-106">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-106">Create a gallery image version.</span></span>

## <span data-ttu-id="1f1b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f1b9-107">EXAMPLES</span></span>

### <span data-ttu-id="1f1b9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f1b9-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="1f1b9-109">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-109">Create a gallery image version.</span></span>

## <span data-ttu-id="1f1b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f1b9-110">PARAMETERS</span></span>

### <span data-ttu-id="1f1b9-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="1f1b9-111">-AsJob</span></span>
<span data-ttu-id="1f1b9-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1f1b9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f1b9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f1b9-113">-DefaultProfile</span></span>
<span data-ttu-id="1f1b9-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f1b9-115">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="1f1b9-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="1f1b9-116">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="1f1b9-117">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="1f1b9-117">-GalleryName</span></span>
<span data-ttu-id="1f1b9-118">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="1f1b9-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="1f1b9-119">-Location</span></span>
<span data-ttu-id="1f1b9-120">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="1f1b9-120">Resource location</span></span>

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

### <span data-ttu-id="1f1b9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f1b9-121">-Name</span></span>
<span data-ttu-id="1f1b9-122">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="1f1b9-123">-Publishingprofileendofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="1f1b9-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="1f1b9-124">Galeri görüntüsünün sürümünün kullanım tarihi.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="1f1b9-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="1f1b9-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="1f1b9-126">Ayarlanmışsa, görüntü tanımının en son sürümünden dağıtılan sanal makineler bu görüntü sürümünü kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="1f1b9-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="1f1b9-127">-ReplicaCount</span></span>
<span data-ttu-id="1f1b9-128">Bölge başına oluşturulacak görüntü sürümünün yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="1f1b9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f1b9-129">-ResourceGroupName</span></span>
<span data-ttu-id="1f1b9-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="1f1b9-131">-Sourceımageıd</span><span class="sxs-lookup"><span data-stu-id="1f1b9-131">-SourceImageId</span></span>
<span data-ttu-id="1f1b9-132">Görüntü sürümünün oluşturulduğu kaynak görüntünün KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="1f1b9-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1f1b9-133">-Tag</span></span>
<span data-ttu-id="1f1b9-134">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="1f1b9-134">Resource tags</span></span>

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

### <span data-ttu-id="1f1b9-135">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="1f1b9-135">-TargetRegion</span></span>
<span data-ttu-id="1f1b9-136">Görüntü sürümünün çoğaltılacağı hedef bölgeler.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-136">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="1f1b9-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f1b9-137">-Confirm</span></span>
<span data-ttu-id="1f1b9-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f1b9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f1b9-139">-WhatIf</span></span>
<span data-ttu-id="1f1b9-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f1b9-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f1b9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f1b9-142">CommonParameters</span></span>
<span data-ttu-id="1f1b9-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f1b9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f1b9-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f1b9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f1b9-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f1b9-145">INPUTS</span></span>

### <span data-ttu-id="1f1b9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1f1b9-146">System.String</span></span>

### <span data-ttu-id="1f1b9-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f1b9-147">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1f1b9-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1f1b9-148">System.Int32</span></span>

### <span data-ttu-id="1f1b9-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1f1b9-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1f1b9-150">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="1f1b9-150">System.DateTime</span></span>

### <span data-ttu-id="1f1b9-151">System. topluluklar. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="1f1b9-151">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="1f1b9-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f1b9-152">OUTPUTS</span></span>

### <span data-ttu-id="1f1b9-153">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="1f1b9-153">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="1f1b9-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f1b9-154">NOTES</span></span>

## <span data-ttu-id="1f1b9-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f1b9-155">RELATED LINKS</span></span>
