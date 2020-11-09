---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzGallery.md
ms.openlocfilehash: 13964bf668533aa5c1bc09b9c4eaaab83c6c421e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322534"
---
# <span data-ttu-id="4bce3-101">Remove-AzGallery</span><span class="sxs-lookup"><span data-stu-id="4bce3-101">Remove-AzGallery</span></span>

## <span data-ttu-id="4bce3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bce3-102">SYNOPSIS</span></span>
<span data-ttu-id="4bce3-103">Galeriyi silme.</span><span class="sxs-lookup"><span data-stu-id="4bce3-103">Delete a gallery.</span></span>

## <span data-ttu-id="4bce3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bce3-104">SYNTAX</span></span>

### <span data-ttu-id="4bce3-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bce3-105">DefaultParameter (Default)</span></span>
```
Remove-AzGallery [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bce3-106">Resourceıdparameter</span><span class="sxs-lookup"><span data-stu-id="4bce3-106">ResourceIdParameter</span></span>
```
Remove-AzGallery [-Force] [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bce3-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4bce3-107">ObjectParameter</span></span>
```
Remove-AzGallery [-Force] [-InputObject] <PSGallery> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bce3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bce3-108">DESCRIPTION</span></span>
<span data-ttu-id="4bce3-109">Galeriyi silme.</span><span class="sxs-lookup"><span data-stu-id="4bce3-109">Delete a gallery.</span></span>

## <span data-ttu-id="4bce3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bce3-110">EXAMPLES</span></span>

### <span data-ttu-id="4bce3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4bce3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzGallery -ResourceGroupName $rgname -GalleryName $galleryName
```

<span data-ttu-id="4bce3-112">Verilen galeriyi silin.</span><span class="sxs-lookup"><span data-stu-id="4bce3-112">Delete the given gallery.</span></span>

## <span data-ttu-id="4bce3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bce3-113">PARAMETERS</span></span>

### <span data-ttu-id="4bce3-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="4bce3-114">-AsJob</span></span>
<span data-ttu-id="4bce3-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4bce3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bce3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bce3-116">-DefaultProfile</span></span>
<span data-ttu-id="4bce3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bce3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bce3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4bce3-118">-Force</span></span>
<span data-ttu-id="4bce3-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4bce3-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4bce3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bce3-120">-InputObject</span></span>
<span data-ttu-id="4bce3-121">PS Galerisi nesnesi</span><span class="sxs-lookup"><span data-stu-id="4bce3-121">The PS Gallery Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery
Parameter Sets: ObjectParameter
Aliases: Gallery

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bce3-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4bce3-122">-Name</span></span>
<span data-ttu-id="4bce3-123">Galeri adı.</span><span class="sxs-lookup"><span data-stu-id="4bce3-123">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bce3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bce3-124">-ResourceGroupName</span></span>
<span data-ttu-id="4bce3-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4bce3-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="4bce3-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4bce3-126">-ResourceId</span></span>
<span data-ttu-id="4bce3-127">Galeri için kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="4bce3-127">The resource Id for the gallery</span></span>

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

### <span data-ttu-id="4bce3-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bce3-128">-Confirm</span></span>
<span data-ttu-id="4bce3-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bce3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bce3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bce3-130">-WhatIf</span></span>
<span data-ttu-id="4bce3-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bce3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bce3-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bce3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bce3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bce3-133">CommonParameters</span></span>
<span data-ttu-id="4bce3-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bce3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bce3-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4bce3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bce3-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bce3-136">INPUTS</span></span>

### <span data-ttu-id="4bce3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4bce3-137">System.String</span></span>

### <span data-ttu-id="4bce3-138">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSGallery</span><span class="sxs-lookup"><span data-stu-id="4bce3-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="4bce3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bce3-139">OUTPUTS</span></span>

### <span data-ttu-id="4bce3-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="4bce3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4bce3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bce3-141">NOTES</span></span>

## <span data-ttu-id="4bce3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bce3-142">RELATED LINKS</span></span>
