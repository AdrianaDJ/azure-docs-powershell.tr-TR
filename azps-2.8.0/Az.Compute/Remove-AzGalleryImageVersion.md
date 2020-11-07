---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 7c62860f3829c07621c951175b00a4be4960c95f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752802"
---
# <span data-ttu-id="f057a-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="f057a-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="f057a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f057a-102">SYNOPSIS</span></span>
<span data-ttu-id="f057a-103">Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="f057a-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="f057a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f057a-104">SYNTAX</span></span>

### <span data-ttu-id="f057a-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f057a-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f057a-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="f057a-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f057a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="f057a-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f057a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f057a-108">DESCRIPTION</span></span>
<span data-ttu-id="f057a-109">Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="f057a-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="f057a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f057a-110">EXAMPLES</span></span>

### <span data-ttu-id="f057a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f057a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="f057a-112">Verilen Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="f057a-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="f057a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f057a-113">PARAMETERS</span></span>

### <span data-ttu-id="f057a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="f057a-114">-AsJob</span></span>
<span data-ttu-id="f057a-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f057a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f057a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f057a-116">-DefaultProfile</span></span>
<span data-ttu-id="f057a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f057a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f057a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f057a-118">-Force</span></span>
<span data-ttu-id="f057a-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f057a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f057a-120">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="f057a-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="f057a-121">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="f057a-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="f057a-122">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="f057a-122">-GalleryName</span></span>
<span data-ttu-id="f057a-123">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="f057a-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="f057a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f057a-124">-InputObject</span></span>
<span data-ttu-id="f057a-125">PS Galerisi görüntü sürümü nesnesi</span><span class="sxs-lookup"><span data-stu-id="f057a-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="f057a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="f057a-126">-Name</span></span>
<span data-ttu-id="f057a-127">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="f057a-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="f057a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f057a-128">-ResourceGroupName</span></span>
<span data-ttu-id="f057a-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f057a-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="f057a-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f057a-130">-ResourceId</span></span>
<span data-ttu-id="f057a-131">Galeri görüntüsü sürümü için kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="f057a-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="f057a-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="f057a-132">-Confirm</span></span>
<span data-ttu-id="f057a-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f057a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f057a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f057a-134">-WhatIf</span></span>
<span data-ttu-id="f057a-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f057a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f057a-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f057a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f057a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f057a-137">CommonParameters</span></span>
<span data-ttu-id="f057a-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f057a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f057a-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f057a-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f057a-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f057a-140">INPUTS</span></span>

### <span data-ttu-id="f057a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f057a-141">System.String</span></span>

### <span data-ttu-id="f057a-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="f057a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="f057a-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f057a-143">OUTPUTS</span></span>

### <span data-ttu-id="f057a-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="f057a-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="f057a-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f057a-145">NOTES</span></span>

## <span data-ttu-id="f057a-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f057a-146">RELATED LINKS</span></span>
