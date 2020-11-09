---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderSourceObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderSourceObject.md
ms.openlocfilehash: 2717e77283019787a4f8b7a2426247968c81c70a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319513"
---
# <span data-ttu-id="9bc63-101">New-AzImageBuilderSourceObject</span><span class="sxs-lookup"><span data-stu-id="9bc63-101">New-AzImageBuilderSourceObject</span></span>

## <span data-ttu-id="9bc63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bc63-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc63-103">Oluşturmak, özelleştirmek ve dağıtmak için sanal makine görüntü kaynağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="9bc63-103">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="9bc63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bc63-104">SYNTAX</span></span>

### <span data-ttu-id="9bc63-105">Managedımage (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9bc63-105">ManagedImage (Default)</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeManagedImage [-ImageId <String>] [<CommonParameters>]
```

### <span data-ttu-id="9bc63-106">Plaformimage</span><span class="sxs-lookup"><span data-stu-id="9bc63-106">PlatformImage</span></span>
```
New-AzImageBuilderSourceObject -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>]
 [-Sku <String>] [-Version <String>] [<CommonParameters>]
```

### <span data-ttu-id="9bc63-107">Platformımageplanınfo</span><span class="sxs-lookup"><span data-stu-id="9bc63-107">PlatformImagePlanInfo</span></span>
```
New-AzImageBuilderSourceObject -PlanName <String> -PlanProduct <String> -PlanPublisher <String>
 -SourceTypePlatformImage [-Offer <String>] [-Publisher <String>] [-Sku <String>] [-Version <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="9bc63-108">Paylaşım sürümü</span><span class="sxs-lookup"><span data-stu-id="9bc63-108">SharedImageVersion</span></span>
```
New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion [-ImageVersionId <String>] [<CommonParameters>]
```

## <span data-ttu-id="9bc63-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bc63-109">DESCRIPTION</span></span>
<span data-ttu-id="9bc63-110">Oluşturmak, özelleştirmek ve dağıtmak için sanal makine görüntü kaynağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="9bc63-110">Describes a virtual machine image source for building, customizing and distributing.</span></span>

## <span data-ttu-id="9bc63-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bc63-111">EXAMPLES</span></span>

### <span data-ttu-id="9bc63-112">Örnek 1: yönetilen görüntü kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9bc63-112">Example 1: Create a managed image source</span></span>
```powershell
PS C:\> $imageid = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image'
PS C:\> New-AzImageBuilderSourceObject -SourceTypeManagedImage -ImageId $imageid

Type         ImageId
----         -------
ManagedImage /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/images/test-linux-image
```

<span data-ttu-id="9bc63-113">Bu komut bir yönetilen görüntü kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bc63-113">This command creates a managed image source.</span></span>

### <span data-ttu-id="9bc63-114">Örnek 2: paylaşılan görüntü kaynağı oluşturma</span><span class="sxs-lookup"><span data-stu-id="9bc63-114">Example 2: Create a shared image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypeSharedImageVersion -ImageVersionId /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0 

Type               ImageVersionId
----               --------------
SharedImageVersion /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/lucasimagegallery/images/myimagedefinition/versions/1.0.0
```

<span data-ttu-id="9bc63-115">Bu komut, paylaşılan bir yansıma kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bc63-115">This command creates a shared image source.</span></span>

### <span data-ttu-id="9bc63-116">Örnek 3: resim kaynağı</span><span class="sxs-lookup"><span data-stu-id="9bc63-116">Example 3: Create a platfrom image source</span></span>
```powershell
PS C:\> New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical' -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'

Type          Offer        Publisher Sku       Version
----          -----        --------- ---       -------
PlatformImage UbuntuServer Canonical 18.04-LTS latest
```

<span data-ttu-id="9bc63-117">Bu komut, bir resim kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9bc63-117">This command creates a platfrom image source.</span></span>

## <span data-ttu-id="9bc63-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bc63-118">PARAMETERS</span></span>

### <span data-ttu-id="9bc63-119">-ImageID</span><span class="sxs-lookup"><span data-stu-id="9bc63-119">-ImageId</span></span>
<span data-ttu-id="9bc63-120">Müşteri aboneliğindeki yönetilen yansımanın ARM kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9bc63-120">ARM resource id of the managed image in customer subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-121">-Imageversionıd</span><span class="sxs-lookup"><span data-stu-id="9bc63-121">-ImageVersionId</span></span>
<span data-ttu-id="9bc63-122">Paylaşılan görüntü galerisinde görüntü sürümünün ARM kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="9bc63-122">ARM resource id of the image version in the shared image gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: SharedImageVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-123">-Teklif</span><span class="sxs-lookup"><span data-stu-id="9bc63-123">-Offer</span></span>
<span data-ttu-id="9bc63-124">[Azure Galeri resimlerinde](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)görüntü teklif.</span><span class="sxs-lookup"><span data-stu-id="9bc63-124">Image offer from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-125">-PlanName</span><span class="sxs-lookup"><span data-stu-id="9bc63-125">-PlanName</span></span>
<span data-ttu-id="9bc63-126">Satın alma planının adı.</span><span class="sxs-lookup"><span data-stu-id="9bc63-126">Name of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-127">-Planürün</span><span class="sxs-lookup"><span data-stu-id="9bc63-127">-PlanProduct</span></span>
<span data-ttu-id="9bc63-128">Satın alma planının çarpımı.</span><span class="sxs-lookup"><span data-stu-id="9bc63-128">Product of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-129">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="9bc63-129">-PlanPublisher</span></span>
<span data-ttu-id="9bc63-130">Satın alma planının yayıncısı.</span><span class="sxs-lookup"><span data-stu-id="9bc63-130">Publisher of the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-131">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9bc63-131">-Publisher</span></span>
<span data-ttu-id="9bc63-132">[Azure Galeri resimlerinde](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)görüntü yayımcısı.</span><span class="sxs-lookup"><span data-stu-id="9bc63-132">Image Publisher in [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="9bc63-133">-Sku</span></span>
<span data-ttu-id="9bc63-134">[Azure Galeri resimlerinde](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)görüntü SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="9bc63-134">Image sku from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-135">-Sourcettypeınfo \ DIMAGE</span><span class="sxs-lookup"><span data-stu-id="9bc63-135">-SourceTypeManagedImage</span></span>
<span data-ttu-id="9bc63-136">Müşteri aboneliğindeki yönetilen bir yansıma olan görüntü kaynağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="9bc63-136">Describes an image source that is a managed image in customer subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-137">-Sourcettypeınfo</span><span class="sxs-lookup"><span data-stu-id="9bc63-137">-SourceTypePlatformImage</span></span>
<span data-ttu-id="9bc63-138">[Azure Galeri resimlerinde](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)görüntü kaynağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="9bc63-138">Describes an image source from [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-139">-Sourcetypesharedımageversion</span><span class="sxs-lookup"><span data-stu-id="9bc63-139">-SourceTypeSharedImageVersion</span></span>
<span data-ttu-id="9bc63-140">Paylaşılan görüntü galerisindeki görüntü sürümü olan bir resim kaynağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="9bc63-140">Describes an image source that is an image version in a shared image gallery.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SharedImageVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-141">-Version</span><span class="sxs-lookup"><span data-stu-id="9bc63-141">-Version</span></span>
<span data-ttu-id="9bc63-142">[Azure Galeri resimlerinde](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages)görüntü sürümü.</span><span class="sxs-lookup"><span data-stu-id="9bc63-142">Image version from the [Azure Gallery Images](https://docs.microsoft.com/en-us/rest/api/compute/virtualmachineimages).</span></span>

```yaml
Type: System.String
Parameter Sets: PlatformImage, PlatformImagePlanInfo
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc63-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc63-143">CommonParameters</span></span>
<span data-ttu-id="9bc63-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bc63-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc63-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9bc63-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc63-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bc63-146">INPUTS</span></span>

## <span data-ttu-id="9bc63-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bc63-147">OUTPUTS</span></span>

### <span data-ttu-id="9bc63-148">Microsoft. Azure. PowerShell. cmdlet. ımagebuilder. modeller. Api20200214. ıımagetemplatesource</span><span class="sxs-lookup"><span data-stu-id="9bc63-148">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource</span></span>

## <span data-ttu-id="9bc63-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bc63-149">NOTES</span></span>

<span data-ttu-id="9bc63-150">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="9bc63-150">ALIASES</span></span>

## <span data-ttu-id="9bc63-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bc63-151">RELATED LINKS</span></span>

