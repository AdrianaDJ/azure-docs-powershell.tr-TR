---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934449"
---
# <span data-ttu-id="483c6-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="483c6-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="483c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483c6-102">SYNOPSIS</span></span>
<span data-ttu-id="483c6-103">Belirli bir galeri öğesini silme.</span><span class="sxs-lookup"><span data-stu-id="483c6-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="483c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="483c6-104">SYNTAX</span></span>

### <span data-ttu-id="483c6-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="483c6-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="483c6-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="483c6-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="483c6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="483c6-107">DESCRIPTION</span></span>
<span data-ttu-id="483c6-108">Belirli bir galeri öğesini silme.</span><span class="sxs-lookup"><span data-stu-id="483c6-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="483c6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="483c6-109">EXAMPLES</span></span>

### <span data-ttu-id="483c6-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="483c6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="483c6-111">Galeri öğesini silme.</span><span class="sxs-lookup"><span data-stu-id="483c6-111">Delete a gallery item.</span></span>

## <span data-ttu-id="483c6-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="483c6-112">PARAMETERS</span></span>

### <span data-ttu-id="483c6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="483c6-113">-Force</span></span>
<span data-ttu-id="483c6-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="483c6-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="483c6-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="483c6-115">-Name</span></span>
<span data-ttu-id="483c6-116">Galeri öğesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="483c6-116">Identity of the gallery item.</span></span>
<span data-ttu-id="483c6-117">Publisher adını, öğe adını içerir ve süre karakteriyle ayrı sürüm içerebilir.</span><span class="sxs-lookup"><span data-stu-id="483c6-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="483c6-118">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="483c6-118">-ResourceId</span></span>
<span data-ttu-id="483c6-119">Tam nitelikli Azure kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="483c6-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="483c6-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="483c6-120">-Confirm</span></span>
<span data-ttu-id="483c6-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="483c6-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483c6-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483c6-122">-WhatIf</span></span>
<span data-ttu-id="483c6-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="483c6-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="483c6-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="483c6-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483c6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483c6-125">CommonParameters</span></span>
<span data-ttu-id="483c6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="483c6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483c6-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="483c6-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483c6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="483c6-128">INPUTS</span></span>

## <span data-ttu-id="483c6-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="483c6-129">OUTPUTS</span></span>

## <span data-ttu-id="483c6-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="483c6-130">NOTES</span></span>

## <span data-ttu-id="483c6-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="483c6-131">RELATED LINKS</span></span>
