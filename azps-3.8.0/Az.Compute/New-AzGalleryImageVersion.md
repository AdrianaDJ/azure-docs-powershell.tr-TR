---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageVersion.md
ms.openlocfilehash: 57520697c0107cdf81bf55e562e78bd991a73fe2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096940"
---
# <span data-ttu-id="8807f-101">New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="8807f-101">New-AzGalleryImageVersion</span></span>

## <span data-ttu-id="8807f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8807f-102">SYNOPSIS</span></span>
<span data-ttu-id="8807f-103">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="8807f-103">Create a gallery image version.</span></span>

## <span data-ttu-id="8807f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8807f-104">SYNTAX</span></span>

```
New-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-AsJob] -Location <String>
 [-DataDiskImage <GalleryDataDiskImage[]>] [-OSDiskImage <GalleryOSDiskImage>]
 [-PublishingProfileEndOfLifeDate <DateTime>] [-PublishingProfileExcludeFromLatest] [-ReplicaCount <Int32>]
 [-SourceImageId <String>] [-StorageAccountType <String>] [-Tag <Hashtable>] [-TargetRegion <Hashtable[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8807f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8807f-105">DESCRIPTION</span></span>
<span data-ttu-id="8807f-106">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="8807f-106">Create a gallery image version.</span></span>

## <span data-ttu-id="8807f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8807f-107">EXAMPLES</span></span>

### <span data-ttu-id="8807f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8807f-108">Example 1</span></span>
```powershell
PS C:\> $region1 = @{Name='West US';ReplicaCount=1}
PS C:\> $region2 = @{Name='East US';ReplicaCount=2}
PS C:\> $region3 = @{Name='Central US'}
PS C:\> $targetRegions = @($region1,$region2,$region3)
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $sourceImageId -ReplicaCount 2 -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegions
```

<span data-ttu-id="8807f-109">Galeri görüntüsü sürümü oluşturma.</span><span class="sxs-lookup"><span data-stu-id="8807f-109">Create a gallery image version.</span></span>

### <span data-ttu-id="8807f-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="8807f-110">Example 2</span></span>
```powershell
PS C:\> $osDiskImageEncryption = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES'}
PS C:\> $dataDiskImageEncryption1 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES1';Lun=1}
PS C:\> $dataDiskImageEncryption2 = @{DiskEncryptionSetId='subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Compute/diskEncryptionSets/myDES2';Lun=2}
PS C:\> $dataDiskImageEncryptions = @($dataDiskImageEncryption1,$dataDiskImageEncryption2)
PS C:\> $encryption1 = @{OSDiskImage=$osDiskImageEncryption;DataDiskImages=$dataDiskImageEncryptions}
PS C:\> $region1 = @{Name='West US';ReplicaCount=1;StorageAccountType=Standard_LRS;Encryption=$encryption1}
PS C:\> $targetRegions = @{$region1}
PS C:\> New-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $galleryName -GalleryImageDefinitionName $imageDefinitionName -Name $versionName -Location $location -SourceImageId $SourceImageId -ReplicaCount 2 -StorageAccountType Standard_LRS -PublishingProfileExcludeFromLatest -PublishingProfileEndOfLifeDate $endOfLifeDate -TargetRegion $targetRegion
```

<span data-ttu-id="8807f-111">Disk görüntüsü şifrelemesiyle bir galeri görüntü sürümü oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8807f-111">Create a gallery image version with disk image encryption.</span></span>

## <span data-ttu-id="8807f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8807f-112">PARAMETERS</span></span>

### <span data-ttu-id="8807f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="8807f-113">-AsJob</span></span>
<span data-ttu-id="8807f-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8807f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8807f-115">-DataDiskImage</span><span class="sxs-lookup"><span data-stu-id="8807f-115">-DataDiskImage</span></span>
<span data-ttu-id="8807f-116">Veri diski görüntüleri.</span><span class="sxs-lookup"><span data-stu-id="8807f-116">Data disk images.</span></span>   <span data-ttu-id="8807f-117">Örneğin @ {Source = @ {ID =<source_id>}; LUN = 1; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="8807f-117">e.g. @{Source = @{Id=<source_id>}; Lun=1; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryDataDiskImage[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8807f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8807f-118">-DefaultProfile</span></span>
<span data-ttu-id="8807f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8807f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8807f-120">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="8807f-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="8807f-121">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="8807f-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="8807f-122">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="8807f-122">-GalleryName</span></span>
<span data-ttu-id="8807f-123">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="8807f-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="8807f-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="8807f-124">-Location</span></span>
<span data-ttu-id="8807f-125">Kaynak konumu</span><span class="sxs-lookup"><span data-stu-id="8807f-125">Resource location</span></span>

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

### <span data-ttu-id="8807f-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="8807f-126">-Name</span></span>
<span data-ttu-id="8807f-127">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="8807f-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="8807f-128">-Osdiskımage</span><span class="sxs-lookup"><span data-stu-id="8807f-128">-OSDiskImage</span></span>
<span data-ttu-id="8807f-129">İşletim sistemi disk görüntüsü örneğin @ {Source = @ {ID =<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly"}</span><span class="sxs-lookup"><span data-stu-id="8807f-129">OS disk image   e.g. @{Source = @{Id=<source_id>}; SizeInGB = 100; HostCaching = "ReadOnly" }</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.GalleryOSDiskImage
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8807f-130">-Publishingprofileendofyaşam tarihi</span><span class="sxs-lookup"><span data-stu-id="8807f-130">-PublishingProfileEndOfLifeDate</span></span>
<span data-ttu-id="8807f-131">Galeri görüntüsünün sürümünün kullanım tarihi.</span><span class="sxs-lookup"><span data-stu-id="8807f-131">The end of life date of the gallery Image Version.</span></span>

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

### <span data-ttu-id="8807f-132">-PublishingProfileExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="8807f-132">-PublishingProfileExcludeFromLatest</span></span>
<span data-ttu-id="8807f-133">Ayarlanmışsa, görüntü tanımının en son sürümünden dağıtılan sanal makineler bu görüntü sürümünü kullanmaz.</span><span class="sxs-lookup"><span data-stu-id="8807f-133">If it is set, Virtual Machines deployed from the latest version of the Image Definition won't use this Image Version.</span></span>

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

### <span data-ttu-id="8807f-134">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="8807f-134">-ReplicaCount</span></span>
<span data-ttu-id="8807f-135">Bölge başına oluşturulacak görüntü sürümünün yineleme sayısı.</span><span class="sxs-lookup"><span data-stu-id="8807f-135">The number of replicas of the Image Version to be created per region.</span></span>

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

### <span data-ttu-id="8807f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8807f-136">-ResourceGroupName</span></span>
<span data-ttu-id="8807f-137">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8807f-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="8807f-138">-Sourceımageıd</span><span class="sxs-lookup"><span data-stu-id="8807f-138">-SourceImageId</span></span>
<span data-ttu-id="8807f-139">Görüntü sürümünün oluşturulduğu kaynak görüntünün KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="8807f-139">The ID of the source image from which the Image Version is going to be created.</span></span>

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

### <span data-ttu-id="8807f-140">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="8807f-140">-StorageAccountType</span></span>
<span data-ttu-id="8807f-141">Yansımayı depolamak için kullanılacak depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8807f-141">Specifies the storage account type to be used to store the image.</span></span> <span data-ttu-id="8807f-142">Bu özellik güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="8807f-142">This property is not updatable.</span></span> <span data-ttu-id="8807f-143">Kullanılabilir değerler Standard_LRS ve Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="8807f-143">Available values are Standard_LRS and Standard_ZRS.</span></span>

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

### <span data-ttu-id="8807f-144">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8807f-144">-Tag</span></span>
<span data-ttu-id="8807f-145">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="8807f-145">Resource tags</span></span>

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

### <span data-ttu-id="8807f-146">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="8807f-146">-TargetRegion</span></span>
<span data-ttu-id="8807f-147">Görüntü sürümünün çoğaltılacağı hedef bölgeler.</span><span class="sxs-lookup"><span data-stu-id="8807f-147">The target regions where the Image Version is going to be replicated to.</span></span>

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

### <span data-ttu-id="8807f-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="8807f-148">-Confirm</span></span>
<span data-ttu-id="8807f-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8807f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8807f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8807f-150">-WhatIf</span></span>
<span data-ttu-id="8807f-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8807f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8807f-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8807f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8807f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8807f-153">CommonParameters</span></span>
<span data-ttu-id="8807f-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8807f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8807f-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8807f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8807f-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8807f-156">INPUTS</span></span>

### <span data-ttu-id="8807f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="8807f-157">System.String</span></span>

### <span data-ttu-id="8807f-158">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8807f-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8807f-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="8807f-159">System.Int32</span></span>

### <span data-ttu-id="8807f-160">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8807f-160">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8807f-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="8807f-161">System.DateTime</span></span>

### <span data-ttu-id="8807f-162">System. topluluklar. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="8807f-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="8807f-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8807f-163">OUTPUTS</span></span>

### <span data-ttu-id="8807f-164">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="8807f-164">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="8807f-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8807f-165">NOTES</span></span>

## <span data-ttu-id="8807f-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8807f-166">RELATED LINKS</span></span>
