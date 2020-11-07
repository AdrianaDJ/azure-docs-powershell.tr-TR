---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934884"
---
# <span data-ttu-id="acdf7-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="acdf7-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="acdf7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acdf7-102">SYNOPSIS</span></span>
<span data-ttu-id="acdf7-103">Temsilci teklifini kaldırır</span><span class="sxs-lookup"><span data-stu-id="acdf7-103">Removes the offer delegation</span></span>

## <span data-ttu-id="acdf7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acdf7-104">SYNTAX</span></span>

### <span data-ttu-id="acdf7-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="acdf7-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acdf7-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="acdf7-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acdf7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="acdf7-107">DESCRIPTION</span></span>
<span data-ttu-id="acdf7-108">Temsilci teklifini kaldırır</span><span class="sxs-lookup"><span data-stu-id="acdf7-108">Removes the offer delegation</span></span>

## <span data-ttu-id="acdf7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acdf7-109">EXAMPLES</span></span>

### <span data-ttu-id="acdf7-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="acdf7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="acdf7-111">Temsilci teklifini kaldırır</span><span class="sxs-lookup"><span data-stu-id="acdf7-111">Removes the offer delegation</span></span>

## <span data-ttu-id="acdf7-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acdf7-112">PARAMETERS</span></span>

### <span data-ttu-id="acdf7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="acdf7-113">-Force</span></span>
<span data-ttu-id="acdf7-114">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="acdf7-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="acdf7-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="acdf7-115">-Name</span></span>
<span data-ttu-id="acdf7-116">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="acdf7-116">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdf7-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="acdf7-117">-OfferName</span></span>
<span data-ttu-id="acdf7-118">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="acdf7-118">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdf7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acdf7-119">-ResourceGroupName</span></span>
<span data-ttu-id="acdf7-120">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="acdf7-120">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acdf7-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="acdf7-121">-ResourceId</span></span>
<span data-ttu-id="acdf7-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="acdf7-122">The resource id.</span></span>

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

### <span data-ttu-id="acdf7-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="acdf7-123">-Confirm</span></span>
<span data-ttu-id="acdf7-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="acdf7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acdf7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acdf7-125">-WhatIf</span></span>
<span data-ttu-id="acdf7-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acdf7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acdf7-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="acdf7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acdf7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acdf7-128">CommonParameters</span></span>
<span data-ttu-id="acdf7-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acdf7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acdf7-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acdf7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acdf7-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acdf7-131">INPUTS</span></span>

## <span data-ttu-id="acdf7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acdf7-132">OUTPUTS</span></span>

## <span data-ttu-id="acdf7-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acdf7-133">NOTES</span></span>

## <span data-ttu-id="acdf7-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acdf7-134">RELATED LINKS</span></span>

