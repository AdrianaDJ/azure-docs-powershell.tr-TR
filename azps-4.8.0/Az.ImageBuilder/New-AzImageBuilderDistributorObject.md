---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderDistributorObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderDistributorObject.md
ms.openlocfilehash: 4b2af3797bde0d27f9f4f18cfd42acdddb4ffcf4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109044"
---
# <span data-ttu-id="dd99c-101">New-AzImageBuilderDistributorObject</span><span class="sxs-lookup"><span data-stu-id="dd99c-101">New-AzImageBuilderDistributorObject</span></span>

## <span data-ttu-id="dd99c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd99c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd99c-103">Genel dağıtım nesnesi</span><span class="sxs-lookup"><span data-stu-id="dd99c-103">Generic distribution object</span></span>

## <span data-ttu-id="dd99c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd99c-104">SYNTAX</span></span>

### <span data-ttu-id="dd99c-105">Managedımagedağıtıcı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd99c-105">ManagedImageDistributor (Default)</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ImageId <String> -Location <String>
 -ManagedImageDistributor -RunOutputName <String> [<CommonParameters>]
```

### <span data-ttu-id="dd99c-106">Paylaşım</span><span class="sxs-lookup"><span data-stu-id="dd99c-106">SharedImageDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -ExcludeFromLatest <Boolean>
 -GalleryImageId <String> -ReplicationRegion <String[]> -RunOutputName <String> -SharedImageDistributor
 [-StorageAccountType <SharedImageStorageAccountType>] [<CommonParameters>]
```

### <span data-ttu-id="dd99c-107">Vhddağıtıcı</span><span class="sxs-lookup"><span data-stu-id="dd99c-107">VhdDistributor</span></span>
```
New-AzImageBuilderDistributorObject -ArtifactTag <Hashtable> -RunOutputName <String> -VhdDistributor
 [<CommonParameters>]
```

## <span data-ttu-id="dd99c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd99c-108">DESCRIPTION</span></span>
<span data-ttu-id="dd99c-109">Genel dağıtım nesnesi</span><span class="sxs-lookup"><span data-stu-id="dd99c-109">Generic distribution object</span></span>

## <span data-ttu-id="dd99c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd99c-110">EXAMPLES</span></span>

### <span data-ttu-id="dd99c-111">Örnek 1: yönetilen görüntü dağıtıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd99c-111">Example 1: Create a managed image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ManagedImageDistributor  -ArtifactTag @{tag='lucasManage'} -ImageId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare -RunOutputName luacas-runout -Location eastus

RunOutputName Type         ImageId                                                                                                                                           Location
------------- ----         -------                                                                                                                                           --------
luacas-runout ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/lucas-linux-imageshare eastus
```

<span data-ttu-id="dd99c-112">Bu komut, yönetilen görüntü dağıtıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd99c-112">This command creates a managed image distributor.</span></span>

### <span data-ttu-id="dd99c-113">Örnek 2: VHD dağıtıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd99c-113">Example 2: Create a VHD distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -ArtifactTag @{tag='vhd'} -VhdDistributor -RunOutputName image-vhd

RunOutputName Type
------------- ----
image-vhd     Vhd
```

<span data-ttu-id="dd99c-114">Bu komut, bir VHD dağıtıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd99c-114">This command creates a VHD distributor.</span></span>

### <span data-ttu-id="dd99c-115">Örnek 3: paylaşılan görüntü dağıtıcısı oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd99c-115">Example 3: Create a shared image distributor</span></span>
```powershell
PS C:\> New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share' -ReplicationRegion eastus2 -RunOutputName 'outname' -ExcludeFromLatest $false 

RunOutputName Type        ExcludeFromLatest GalleryImageId                                                                                                                                                        ReplicationRegi
                                                                                                                                                                                                                  on
------------- ----        ----------------- --------------                                                                                                                                                        ---------------
outname       SharedImage False             /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/myimagegallery/images/lcuas-linux-share {eastus2}
```

<span data-ttu-id="dd99c-116">Bu komut paylaşılan görüntü dağıtıcısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dd99c-116">This command creates a shared image distributor.</span></span>

## <span data-ttu-id="dd99c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd99c-117">PARAMETERS</span></span>

### <span data-ttu-id="dd99c-118">-ArtifactTag</span><span class="sxs-lookup"><span data-stu-id="dd99c-118">-ArtifactTag</span></span>
<span data-ttu-id="dd99c-119">Dağıtımcı tarafından oluşturulduktan/güncelleştirildikten sonra yapıya uygulanacak Etiketler.</span><span class="sxs-lookup"><span data-stu-id="dd99c-119">Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-120">-ExcludeFromLatest</span><span class="sxs-lookup"><span data-stu-id="dd99c-120">-ExcludeFromLatest</span></span>
<span data-ttu-id="dd99c-121">Oluşturulan görüntü sürümünün en son dışında dışlanıp dışlanmayacağını belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="dd99c-121">Flag that indicates whether created image version should be excluded from latest.</span></span>
<span data-ttu-id="dd99c-122">Varsayılanı (yanlış) kullanmak için atlayın.</span><span class="sxs-lookup"><span data-stu-id="dd99c-122">Omit to use the default (false).</span></span>

```yaml
Type: System.Boolean
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-123">-Gallerımageıd</span><span class="sxs-lookup"><span data-stu-id="dd99c-123">-GalleryImageId</span></span>
<span data-ttu-id="dd99c-124">Paylaşılan görüntü Galerisi görüntüsünün kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dd99c-124">Resource Id of the Shared Image Gallery image.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-125">-ImageID</span><span class="sxs-lookup"><span data-stu-id="dd99c-125">-ImageId</span></span>
<span data-ttu-id="dd99c-126">Yönetilen disk görüntüsünün kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="dd99c-126">Resource Id of the Managed Disk Image.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="dd99c-127">-Location</span></span>
<span data-ttu-id="dd99c-128">Görüntü zaten varsa, resim için Azure konumu eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="dd99c-128">Azure location for the image, should match if image already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-129">-Managedımagedağıtıcı</span><span class="sxs-lookup"><span data-stu-id="dd99c-129">-ManagedImageDistributor</span></span>
<span data-ttu-id="dd99c-130">Yönetilen disk görüntüsü olarak dağıtın.</span><span class="sxs-lookup"><span data-stu-id="dd99c-130">Distribute as a Managed Disk Image.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-131">-ReplicationRegion</span><span class="sxs-lookup"><span data-stu-id="dd99c-131">-ReplicationRegion</span></span>
<span data-ttu-id="dd99c-132">Yansımanın çoğaltılacağı bölgelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="dd99c-132">A list of regions that the image will be replicated to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-133">-RunOutputName</span><span class="sxs-lookup"><span data-stu-id="dd99c-133">-RunOutputName</span></span>
<span data-ttu-id="dd99c-134">İlişkili RunOutput için kullanılacak ad.</span><span class="sxs-lookup"><span data-stu-id="dd99c-134">The name to be used for the associated RunOutput.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-135">-Sharedımagedağıtıcı</span><span class="sxs-lookup"><span data-stu-id="dd99c-135">-SharedImageDistributor</span></span>
<span data-ttu-id="dd99c-136">Paylaşılan görüntü Galerisi aracılığıyla dağıtın.</span><span class="sxs-lookup"><span data-stu-id="dd99c-136">Distribute via Shared Image Gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="dd99c-137">-StorageAccountType</span></span>
<span data-ttu-id="dd99c-138">Paylaşılan Yansımayı depolamak için kullanılacak depolama hesabı türü.</span><span class="sxs-lookup"><span data-stu-id="dd99c-138">Storage account type to be used to store the shared image.</span></span>
<span data-ttu-id="dd99c-139">Varsayılanı (Standard_LRS) kullanmak için atlayın.</span><span class="sxs-lookup"><span data-stu-id="dd99c-139">Omit to use the default (Standard_LRS).</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.SharedImageStorageAccountType
Parameter Sets: SharedImageDistributor
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-140">-Vhddağıtıcı</span><span class="sxs-lookup"><span data-stu-id="dd99c-140">-VhdDistributor</span></span>
<span data-ttu-id="dd99c-141">Depolama hesabında VHD ile dağıtın.</span><span class="sxs-lookup"><span data-stu-id="dd99c-141">Distribute via VHD in a storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VhdDistributor
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd99c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd99c-142">CommonParameters</span></span>
<span data-ttu-id="dd99c-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd99c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd99c-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dd99c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd99c-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd99c-145">INPUTS</span></span>

## <span data-ttu-id="dd99c-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd99c-146">OUTPUTS</span></span>

### <span data-ttu-id="dd99c-147">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. modeller. Api20200214. ıımagetemplatedağıtıcı</span><span class="sxs-lookup"><span data-stu-id="dd99c-147">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor</span></span>

## <span data-ttu-id="dd99c-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd99c-148">NOTES</span></span>

<span data-ttu-id="dd99c-149">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="dd99c-149">ALIASES</span></span>

## <span data-ttu-id="dd99c-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd99c-150">RELATED LINKS</span></span>

