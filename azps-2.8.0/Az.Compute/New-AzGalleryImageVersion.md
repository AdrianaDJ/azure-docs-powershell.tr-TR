---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 80536a8bfce32d713649f3feab4d77b1662206b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752855"
---
# <span data-ttu-id="ce888-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="ce888-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="ce888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce888-102">SYNOPSIS</span></span>
<span data-ttu-id="ce888-103">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="ce888-103">Create a gallery image version.</span></span>

## <span data-ttu-id="ce888-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce888-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String> -SourceImageId <String>
 [-Tag <Hashtable>] [-ReplicaCount <Int32>] [-PublishingProfileExcludeFromLatest]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-StorageAccountType <String>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce888-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce888-105">DESCRIPTION</span></span>
<span data-ttu-id="ce888-106">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="ce888-106">Create a gallery image version.</span></span>

## <span data-ttu-id="ce888-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce888-107">EXAMPLES</span></span>

### <span data-ttu-id="ce888-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ce888-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageName $imageName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="ce888-109">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="ce888-109">Create a gallery image version.</span></span>

## <span data-ttu-id="ce888-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce888-110">PARAMETERS</span></span>

### <span data-ttu-id="ce888-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="ce888-111">-AsJob</span></span>
<span data-ttu-id="ce888-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ce888-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce888-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce888-113">-DefaultProfile</span></span>
<span data-ttu-id="ce888-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce888-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce888-115">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="ce888-115">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="ce888-116">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="ce888-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="ce888-117">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="ce888-117">-GalleryName</span></span>
<span data-ttu-id="ce888-118">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="ce888-118">The name of the gallery.</span></span>

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

### <span data-ttu-id="ce888-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="ce888-119">-Location</span></span>
<span data-ttu-id="ce888-120">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="ce888-120">Resource location</span></span>

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

### <span data-ttu-id="ce888-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce888-121">-Name</span></span>
<span data-ttu-id="ce888-122">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="ce888-122">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="ce888-123">-Publishingprofileendofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="ce888-123">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="ce888-124">Galeri görüntüsünün sürümünün kullanım tarihi.</span><span class="sxs-lookup"><span data-stu-id="ce888-124">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="ce888-125">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="ce888-125">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="ce888-126">Ayarlanmışsa, görüntü tanımının en son sürümünden dağıtılan sanal makineler bu görüntü sürümünü kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="ce888-126">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="ce888-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="ce888-127">-ReplicaCount</span></span>
<span data-ttu-id="ce888-128">Bölge başına oluşturulacak görüntü sürümünün yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="ce888-128">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="ce888-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce888-129">-ResourceGroupName</span></span>
<span data-ttu-id="ce888-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ce888-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce888-131">-Sourceımageıd</span><span class="sxs-lookup"><span data-stu-id="ce888-131">-SourceImageId</span></span>
<span data-ttu-id="ce888-132">Görüntü sürümünün oluşturulduğu kaynak görüntünün KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ce888-132">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="ce888-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ce888-133">-StorageAccountType</span></span>
<span data-ttu-id="ce888-134">Yansımayı depolamak için kullanılacak depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce888-134">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="ce888-135">Bu özellik güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="ce888-135">This property is not updatable.</span></span> <span data-ttu-id="ce888-136">Kullanılabilir değerler Standard_LRS ve Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="ce888-136">Available values are Standard_LRS and Standard_ZRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce888-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ce888-137">-Tag</span></span>
<span data-ttu-id="ce888-138">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="ce888-138">Resource tags</span></span>

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

### <span data-ttu-id="ce888-139">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="ce888-139">-TargetRegion</span></span>
<span data-ttu-id="ce888-140">Görüntü sürümünün çoğaltılacağı hedef bölgeler.</span><span class="sxs-lookup"><span data-stu-id="ce888-140">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="ce888-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce888-141">-Confirm</span></span>
<span data-ttu-id="ce888-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce888-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce888-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce888-143">-WhatIf</span></span>
<span data-ttu-id="ce888-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce888-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce888-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce888-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce888-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce888-146">CommonParameters</span></span>
<span data-ttu-id="ce888-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce888-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce888-148">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ce888-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce888-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce888-149">INPUTS</span></span>

### <span data-ttu-id="ce888-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ce888-150">System.String</span></span>

### <span data-ttu-id="ce888-151">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ce888-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ce888-152">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ce888-152">System.Int32</span></span>

### <span data-ttu-id="ce888-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ce888-153">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ce888-154">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ce888-154">System.DateTime</span></span>

### <span data-ttu-id="ce888-155">System. topluluklar. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="ce888-155">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="ce888-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce888-156">OUTPUTS</span></span>

### <span data-ttu-id="ce888-157">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="ce888-157">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="ce888-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce888-158">NOTES</span></span>

## <span data-ttu-id="ce888-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce888-159">RELATED LINKS</span></span>
