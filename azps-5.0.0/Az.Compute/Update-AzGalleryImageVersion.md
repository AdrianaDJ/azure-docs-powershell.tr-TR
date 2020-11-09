---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageVersion.md
ms.openlocfilehash: 9705cfbee28a462c0579205fdbde6b69bdc34e44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319617"
---
# <span data-ttu-id="02fee-101">Update-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="02fee-101">Update-AzGalleryImageVersion</span></span>

## <span data-ttu-id="02fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02fee-102">SYNOPSIS</span></span>
<span data-ttu-id="02fee-103">Galeri görüntüsü sürümünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="02fee-103">Update a gallery image version.</span></span>

## <span data-ttu-id="02fee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02fee-104">SYNTAX</span></span>

### <span data-ttu-id="02fee-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02fee-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02fee-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="02fee-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageVersion [-ResourceId] <String> [-AsJob] [-PublishingProfileEndOfLifeDate <DateTime>]
 [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02fee-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="02fee-107">ObjectParameter</span></span>
```
Update-AzGalleryImageVersion [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02fee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="02fee-108">DESCRIPTION</span></span>
<span data-ttu-id="02fee-109">Galeri görüntüsü sürümünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="02fee-109">Update a gallery image version.</span></span>

## <span data-ttu-id="02fee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02fee-110">EXAMPLES</span></span>

### <span data-ttu-id="02fee-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02fee-111">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> Update-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="02fee-112">Galeri görüntüsü sürümünü güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="02fee-112">Update a gallery image version.</span></span>

## <span data-ttu-id="02fee-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02fee-113">PARAMETERS</span></span>

### <span data-ttu-id="02fee-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="02fee-114">-AsJob</span></span>
<span data-ttu-id="02fee-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="02fee-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02fee-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02fee-116">-DefaultProfile</span></span>
<span data-ttu-id="02fee-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02fee-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02fee-118">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="02fee-118">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="02fee-119">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="02fee-119">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="02fee-120">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="02fee-120">-GalleryName</span></span>
<span data-ttu-id="02fee-121">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="02fee-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="02fee-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02fee-122">-InputObject</span></span>
<span data-ttu-id="02fee-123">PS Galerisi görüntü sürümü nesnesi.</span><span class="sxs-lookup"><span data-stu-id="02fee-123">The PS Gallery Image Version Object.</span></span>

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

### <span data-ttu-id="02fee-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="02fee-124">-Name</span></span>
<span data-ttu-id="02fee-125">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="02fee-125">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="02fee-126">-Publishingprofileendofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="02fee-126">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="02fee-127">Galeri görüntüsünün sürümünün kullanım tarihi.</span><span class="sxs-lookup"><span data-stu-id="02fee-127">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="02fee-128">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="02fee-128">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="02fee-129">Ayarlanmışsa, görüntü tanımının en son sürümünden dağıtılan sanal makineler bu görüntü sürümünü kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="02fee-129">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="02fee-130">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="02fee-130">-ReplicaCount</span></span>
<span data-ttu-id="02fee-131">Bölge başına oluşturulacak görüntü sürümünün yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="02fee-131">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="02fee-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02fee-132">-ResourceGroupName</span></span>
<span data-ttu-id="02fee-133">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="02fee-133">The name of the resource group.</span></span>

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

### <span data-ttu-id="02fee-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02fee-134">-ResourceId</span></span>
<span data-ttu-id="02fee-135">Galeri görüntüsü sürümü için kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="02fee-135">The resource ID for the gallery image version.</span></span>

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

### <span data-ttu-id="02fee-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="02fee-136">-Tag</span></span>
<span data-ttu-id="02fee-137">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="02fee-137">Resource tags</span></span>

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

### <span data-ttu-id="02fee-138">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="02fee-138">-TargetRegion</span></span>
<span data-ttu-id="02fee-139">Görüntü sürümünün çoğaltılacağı hedef bölgeler.</span><span class="sxs-lookup"><span data-stu-id="02fee-139">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="02fee-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="02fee-140">-Confirm</span></span>
<span data-ttu-id="02fee-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02fee-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02fee-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02fee-142">-WhatIf</span></span>
<span data-ttu-id="02fee-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02fee-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02fee-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02fee-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02fee-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02fee-145">CommonParameters</span></span>
<span data-ttu-id="02fee-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02fee-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02fee-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02fee-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02fee-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02fee-148">INPUTS</span></span>

### <span data-ttu-id="02fee-149">System. String</span><span class="sxs-lookup"><span data-stu-id="02fee-149">System.String</span></span>

### <span data-ttu-id="02fee-150">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="02fee-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

### <span data-ttu-id="02fee-151">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="02fee-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="02fee-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="02fee-152">System.Int32</span></span>

### <span data-ttu-id="02fee-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="02fee-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="02fee-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="02fee-154">System.DateTime</span></span>

### <span data-ttu-id="02fee-155">System. topluluklar. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="02fee-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="02fee-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02fee-156">OUTPUTS</span></span>

### <span data-ttu-id="02fee-157">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="02fee-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="02fee-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02fee-158">NOTES</span></span>

## <span data-ttu-id="02fee-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02fee-159">RELATED LINKS</span></span>
