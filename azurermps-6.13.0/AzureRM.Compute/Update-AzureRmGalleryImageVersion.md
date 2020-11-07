---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageVersion.md
ms.openlocfilehash: e8c50ffb2ac60c65f64806781d9155600c9bbe0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762988"
---
# <span data-ttu-id="d1e33-101">Update-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="d1e33-101">Update-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="d1e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1e33-102">SYNOPSIS</span></span>
<span data-ttu-id="d1e33-103">Galeri görüntüsü sürümünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d1e33-103">Update a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1e33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1e33-104">SYNTAX</span></span>

### <span data-ttu-id="d1e33-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d1e33-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1e33-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="d1e33-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageVersion [-ResourceId] <String> [-AsJob] [-Tag <Hashtable>] [-ReplicaCount <Int32>]
 [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1e33-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="d1e33-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob] [-Tag <Hashtable>]
 [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1e33-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1e33-108">DESCRIPTION</span></span>
<span data-ttu-id="d1e33-109">Galeri görüntüsü sürümünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d1e33-109">Update a gallery image version.</span></span>

## <span data-ttu-id="d1e33-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1e33-110">EXAMPLES</span></span>

### <span data-ttu-id="d1e33-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d1e33-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="d1e33-112">Galeri görüntüsü sürümünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="d1e33-112">Update a gallery image version.</span></span>

## <span data-ttu-id="d1e33-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1e33-113">PARAMETERS</span></span>

### <span data-ttu-id="d1e33-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d1e33-114">-AsJob</span></span>
<span data-ttu-id="d1e33-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d1e33-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1e33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1e33-116">-DefaultProfile</span></span>
<span data-ttu-id="d1e33-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1e33-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1e33-118">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="d1e33-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="d1e33-119">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="d1e33-119">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e33-120">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="d1e33-120">-GalleryName</span></span>
<span data-ttu-id="d1e33-121">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="d1e33-121">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e33-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1e33-122">-InputObject</span></span>
<span data-ttu-id="d1e33-123">PS Galerisi görüntü sürümü nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d1e33-123">The PS Gallery Image Version Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion
Parameter Sets: ObjectParameter
Aliases: GalleryImageVersion

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e33-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1e33-124">-Name</span></span>
<span data-ttu-id="d1e33-125">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="d1e33-125">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e33-126">-Publishingprofileendofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="d1e33-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="d1e33-127">Galeri görüntüsünün sürümünün kullanım tarihi.</span><span class="sxs-lookup"><span data-stu-id="d1e33-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="d1e33-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="d1e33-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="d1e33-129">Ayarlanmışsa, görüntü tanımının en son sürümünden dağıtılan sanal makineler bu görüntü sürümünü kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="d1e33-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="d1e33-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="d1e33-130">-ReplicaCount</span></span>
<span data-ttu-id="d1e33-131">Bölge başına oluşturulacak görüntü sürümünün yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="d1e33-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="d1e33-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1e33-132">-ResourceGroupName</span></span>
<span data-ttu-id="d1e33-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d1e33-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e33-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d1e33-134">-ResourceId</span></span>
<span data-ttu-id="d1e33-135">Galeri görüntüsü sürümü için kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d1e33-135">The resource ID for the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1e33-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d1e33-136">-Tag</span></span>
<span data-ttu-id="d1e33-137">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="d1e33-137">Resource tags</span></span>

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

### <span data-ttu-id="d1e33-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="d1e33-138">-TargetRegion</span></span>
<span data-ttu-id="d1e33-139">Görüntü sürümünün çoğaltılacağı hedef bölgeler.</span><span class="sxs-lookup"><span data-stu-id="d1e33-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="d1e33-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1e33-140">-Confirm</span></span>
<span data-ttu-id="d1e33-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1e33-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1e33-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1e33-142">-WhatIf</span></span>
<span data-ttu-id="d1e33-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1e33-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1e33-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1e33-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1e33-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1e33-145">CommonParameters</span></span>
<span data-ttu-id="d1e33-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1e33-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1e33-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1e33-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1e33-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1e33-148">INPUTS</span></span>

### <span data-ttu-id="d1e33-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d1e33-149">System.String</span></span>

### <span data-ttu-id="d1e33-150">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="d1e33-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="d1e33-151">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d1e33-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d1e33-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d1e33-152">System.Int32</span></span>

### <span data-ttu-id="d1e33-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1e33-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d1e33-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d1e33-154">System.DateTime</span></span>

### <span data-ttu-id="d1e33-155">System. topluluklar. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="d1e33-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="d1e33-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1e33-156">OUTPUTS</span></span>

### <span data-ttu-id="d1e33-157">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="d1e33-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="d1e33-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1e33-158">NOTES</span></span>

## <span data-ttu-id="d1e33-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1e33-159">RELATED LINKS</span></span>
