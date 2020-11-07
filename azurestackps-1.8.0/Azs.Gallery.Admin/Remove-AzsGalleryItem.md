---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934711"
---
# <span data-ttu-id="b3e6f-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="b3e6f-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="b3e6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e6f-103">Belirli bir galeri öğesini silme.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="b3e6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3e6f-104">SYNTAX</span></span>

### <span data-ttu-id="b3e6f-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3e6f-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3e6f-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b3e6f-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e6f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3e6f-107">DESCRIPTION</span></span>
<span data-ttu-id="b3e6f-108">Belirli bir galeri öğesini silme.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="b3e6f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3e6f-109">EXAMPLES</span></span>

### <span data-ttu-id="b3e6f-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="b3e6f-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="b3e6f-111">Galeri öğesini silme.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-111">Delete a gallery item.</span></span>

## <span data-ttu-id="b3e6f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3e6f-112">PARAMETERS</span></span>

### <span data-ttu-id="b3e6f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3e6f-113">-Name</span></span>
<span data-ttu-id="b3e6f-114">Galeri öğesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-114">Identity of the gallery item.</span></span>
<span data-ttu-id="b3e6f-115">Publisher adını, öğe adını içerir ve süre karakteriyle ayrı sürüm içerebilir.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e6f-116">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b3e6f-116">-ResourceId</span></span>
<span data-ttu-id="b3e6f-117">Tam nitelikli Azure kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-117">Fully qualified Azure resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e6f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b3e6f-118">-Force</span></span>
<span data-ttu-id="b3e6f-119">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-119">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e6f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e6f-120">-WhatIf</span></span>
<span data-ttu-id="b3e6f-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e6f-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e6f-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3e6f-123">-Confirm</span></span>
<span data-ttu-id="b3e6f-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e6f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e6f-125">CommonParameters</span></span>
<span data-ttu-id="b3e6f-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3e6f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e6f-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e6f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e6f-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3e6f-128">INPUTS</span></span>

## <span data-ttu-id="b3e6f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3e6f-129">OUTPUTS</span></span>

## <span data-ttu-id="b3e6f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3e6f-130">NOTES</span></span>

## <span data-ttu-id="b3e6f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3e6f-131">RELATED LINKS</span></span>
