---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGalleryImageDefinition.md
ms.openlocfilehash: 81323c1a35e36b036e759911bbfec2dde764ac8f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938547"
---
# <span data-ttu-id="9bca8-101">Remove-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="9bca8-101">Remove-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="9bca8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bca8-102">SYNOPSIS</span></span>
<span data-ttu-id="9bca8-103">Galeri görüntüsü tanımını silme.</span><span class="sxs-lookup"><span data-stu-id="9bca8-103">Delete a gallery image definition.</span></span>

## <span data-ttu-id="9bca8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9bca8-104">SYNTAX</span></span>

### <span data-ttu-id="9bca8-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9bca8-105">DefaultParameter (Default)</span></span>
```
Remove-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bca8-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="9bca8-106">ResourceIdParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bca8-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9bca8-107">ObjectParameter</span></span>
```
Remove-AzGalleryImageDefinition [-Force] [-InputObject] <PSGalleryImage> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bca8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9bca8-108">DESCRIPTION</span></span>
<span data-ttu-id="9bca8-109">Galeri görüntüsü tanımını silme.</span><span class="sxs-lookup"><span data-stu-id="9bca8-109">Delete a gallery image definition.</span></span>

## <span data-ttu-id="9bca8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9bca8-110">EXAMPLES</span></span>

### <span data-ttu-id="9bca8-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9bca8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $galleryImage
```

<span data-ttu-id="9bca8-112">Galeri resmi tanımını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="9bca8-112">Remove the gallery image definition.</span></span>

## <span data-ttu-id="9bca8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9bca8-113">PARAMETERS</span></span>

### <span data-ttu-id="9bca8-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="9bca8-114">-AsJob</span></span>
<span data-ttu-id="9bca8-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9bca8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9bca8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bca8-116">-DefaultProfile</span></span>
<span data-ttu-id="9bca8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9bca8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bca8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9bca8-118">-Force</span></span>
<span data-ttu-id="9bca8-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9bca8-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9bca8-120">-Gallertadı</span><span class="sxs-lookup"><span data-stu-id="9bca8-120">-GalleryName</span></span>
<span data-ttu-id="9bca8-121">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="9bca8-121">The name of the gallery.</span></span>

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

### <span data-ttu-id="9bca8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bca8-122">-InputObject</span></span>
<span data-ttu-id="9bca8-123">PS Galerisi görüntü tanımı nesnesi</span><span class="sxs-lookup"><span data-stu-id="9bca8-123">The PS Gallery Image Definition Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bca8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="9bca8-124">-Name</span></span>
<span data-ttu-id="9bca8-125">Galeri resim tanımının adı.</span><span class="sxs-lookup"><span data-stu-id="9bca8-125">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bca8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bca8-126">-ResourceGroupName</span></span>
<span data-ttu-id="9bca8-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9bca8-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9bca8-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9bca8-128">-ResourceId</span></span>
<span data-ttu-id="9bca8-129">Galeri resmi tanımı için kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="9bca8-129">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="9bca8-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="9bca8-130">-Confirm</span></span>
<span data-ttu-id="9bca8-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9bca8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bca8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bca8-132">-WhatIf</span></span>
<span data-ttu-id="9bca8-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9bca8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bca8-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9bca8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bca8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bca8-135">CommonParameters</span></span>
<span data-ttu-id="9bca8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9bca8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bca8-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9bca8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bca8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9bca8-138">INPUTS</span></span>

### <span data-ttu-id="9bca8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9bca8-139">System.String</span></span>

### <span data-ttu-id="9bca8-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psgallerimage</span><span class="sxs-lookup"><span data-stu-id="9bca8-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="9bca8-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9bca8-141">OUTPUTS</span></span>

### <span data-ttu-id="9bca8-142">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="9bca8-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9bca8-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9bca8-143">NOTES</span></span>

## <span data-ttu-id="9bca8-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9bca8-144">RELATED LINKS</span></span>
