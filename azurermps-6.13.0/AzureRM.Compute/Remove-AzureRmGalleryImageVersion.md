---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmGalleryImageVersion.md
ms.openlocfilehash: c2a65eeb742d4182dfad0cd32be1d78951977096
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588537"
---
# <span data-ttu-id="251f1-101">Remove-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="251f1-101">Remove-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="251f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="251f1-102">SYNOPSIS</span></span>
<span data-ttu-id="251f1-103">Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="251f1-103">Delete a gallery image version.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="251f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="251f1-104">SYNTAX</span></span>

### <span data-ttu-id="251f1-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="251f1-105">DefaultParameter (Default)</span></span>
```
Remove-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="251f1-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="251f1-106">ResourceIdParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="251f1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="251f1-107">ObjectParameter</span></span>
```
Remove-AzureRmGalleryImageVersion [-Force] [-InputObject] <PSGalleryImageVersion> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="251f1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="251f1-108">DESCRIPTION</span></span>
<span data-ttu-id="251f1-109">Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="251f1-109">Delete a gallery image version.</span></span>

## <span data-ttu-id="251f1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="251f1-110">EXAMPLES</span></span>

### <span data-ttu-id="251f1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="251f1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="251f1-112">Verilen Galeri görüntüsü sürümünü silme.</span><span class="sxs-lookup"><span data-stu-id="251f1-112">Delete the given gallery image version.</span></span>

## <span data-ttu-id="251f1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="251f1-113">PARAMETERS</span></span>

### <span data-ttu-id="251f1-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="251f1-114">-AsJob</span></span>
<span data-ttu-id="251f1-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="251f1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="251f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="251f1-116">-DefaultProfile</span></span>
<span data-ttu-id="251f1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="251f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="251f1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="251f1-118">-Force</span></span>
<span data-ttu-id="251f1-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="251f1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="251f1-120">-Gallerımagedefinitionname</span><span class="sxs-lookup"><span data-stu-id="251f1-120">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="251f1-121">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="251f1-121">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="251f1-122">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="251f1-122">-GalleryName</span></span>
<span data-ttu-id="251f1-123">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="251f1-123">The name of the gallery.</span></span>

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

### <span data-ttu-id="251f1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="251f1-124">-InputObject</span></span>
<span data-ttu-id="251f1-125">PS Galerisi görüntü sürümü nesnesi</span><span class="sxs-lookup"><span data-stu-id="251f1-125">The PS Gallery Image Version Object</span></span>

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

### <span data-ttu-id="251f1-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="251f1-126">-Name</span></span>
<span data-ttu-id="251f1-127">Galeri görüntüsü sürümünün adı.</span><span class="sxs-lookup"><span data-stu-id="251f1-127">The name of the gallery image version.</span></span>

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

### <span data-ttu-id="251f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="251f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="251f1-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="251f1-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="251f1-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="251f1-130">-ResourceId</span></span>
<span data-ttu-id="251f1-131">Galeri görüntüsü sürümü için kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="251f1-131">The resource ID for gallery image version</span></span>

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

### <span data-ttu-id="251f1-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="251f1-132">-Confirm</span></span>
<span data-ttu-id="251f1-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="251f1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="251f1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="251f1-134">-WhatIf</span></span>
<span data-ttu-id="251f1-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="251f1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="251f1-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="251f1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="251f1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251f1-137">CommonParameters</span></span>
<span data-ttu-id="251f1-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="251f1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251f1-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="251f1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251f1-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="251f1-140">INPUTS</span></span>

### <span data-ttu-id="251f1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="251f1-141">System.String</span></span>

### <span data-ttu-id="251f1-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerımageversion</span><span class="sxs-lookup"><span data-stu-id="251f1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="251f1-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="251f1-143">OUTPUTS</span></span>

### <span data-ttu-id="251f1-144">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="251f1-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="251f1-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="251f1-145">NOTES</span></span>

## <span data-ttu-id="251f1-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="251f1-146">RELATED LINKS</span></span>
