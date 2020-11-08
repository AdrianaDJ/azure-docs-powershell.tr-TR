---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageVersion.md
ms.openlocfilehash: 4c4809ed022595af7c0ad977d082c6a52616e920
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275608"
---
# <span data-ttu-id="28cf5-101">Remove-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="28cf5-101">Remove-AzGalleryImageVersion</span></span>

## <span data-ttu-id="28cf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="28cf5-103">Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="28cf5-103">Delete a gallery image version.</span></span>

## <span data-ttu-id="28cf5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28cf5-104">SYNTAX</span></span>

### <span data-ttu-id="28cf5-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="28cf5-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cf5-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="28cf5-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cf5-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="28cf5-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28cf5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="28cf5-108">DESCRIPTION</span></span>
<span data-ttu-id="28cf5-109">Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="28cf5-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="28cf5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28cf5-110">EXAMPLES</span></span>

### <span data-ttu-id="28cf5-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="28cf5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image -Name $version
```

<span data-ttu-id="28cf5-112">Verilen Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="28cf5-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="28cf5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28cf5-113">PARAMETERS</span></span>

### <span data-ttu-id="28cf5-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="28cf5-114">-AsJob</span></span>
<span data-ttu-id="28cf5-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="28cf5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28cf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cf5-116">-DefaultProfile</span></span>
<span data-ttu-id="28cf5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28cf5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28cf5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="28cf5-118">-Force</span></span>
<span data-ttu-id="28cf5-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="28cf5-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28cf5-120">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="28cf5-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="28cf5-121">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="28cf5-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="28cf5-122">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="28cf5-122">-GalleryName</span></span>
<span data-ttu-id="28cf5-123">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="28cf5-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="28cf5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28cf5-124">-InputObject</span></span>
<span data-ttu-id="28cf5-125">PS Galerisi görüntü sürümü nesnesi</span><span class="sxs-lookup"><span data-stu-id="28cf5-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="28cf5-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="28cf5-126">-Name</span></span>
<span data-ttu-id="28cf5-127">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="28cf5-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="28cf5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cf5-128">-ResourceGroupName</span></span>
<span data-ttu-id="28cf5-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="28cf5-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="28cf5-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="28cf5-130">-ResourceId</span></span>
<span data-ttu-id="28cf5-131">Galeri görüntüsü sürümü için kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="28cf5-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="28cf5-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="28cf5-132">-Confirm</span></span>
<span data-ttu-id="28cf5-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="28cf5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cf5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cf5-134">-WhatIf</span></span>
<span data-ttu-id="28cf5-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="28cf5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cf5-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="28cf5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cf5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cf5-137">CommonParameters</span></span>
<span data-ttu-id="28cf5-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28cf5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cf5-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="28cf5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cf5-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28cf5-140">INPUTS</span></span>

### <span data-ttu-id="28cf5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="28cf5-141">System.String</span></span>

### <span data-ttu-id="28cf5-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="28cf5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="28cf5-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28cf5-143">OUTPUTS</span></span>

### <span data-ttu-id="28cf5-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="28cf5-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="28cf5-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28cf5-145">NOTES</span></span>

## <span data-ttu-id="28cf5-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28cf5-146">RELATED LINKS</span></span>
