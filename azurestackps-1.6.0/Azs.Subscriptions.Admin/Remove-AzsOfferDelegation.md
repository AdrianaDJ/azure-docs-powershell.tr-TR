---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec978cebfaa12f574ce20638347839fd70099df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572153"
---
# <span data-ttu-id="6bcbc-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="6bcbc-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="6bcbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bcbc-102">SYNOPSIS</span></span>
<span data-ttu-id="6bcbc-103">Temsilci teklifini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6bcbc-103">Removes the offer delegation</span></span>

## <span data-ttu-id="6bcbc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bcbc-104">SYNTAX</span></span>

### <span data-ttu-id="6bcbc-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6bcbc-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bcbc-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="6bcbc-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bcbc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bcbc-107">DESCRIPTION</span></span>
<span data-ttu-id="6bcbc-108">Temsilci teklifini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6bcbc-108">Removes the offer delegation</span></span>

## <span data-ttu-id="6bcbc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bcbc-109">EXAMPLES</span></span>

### <span data-ttu-id="6bcbc-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6bcbc-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="6bcbc-111">Temsilci teklifini kaldırır</span><span class="sxs-lookup"><span data-stu-id="6bcbc-111">Removes the offer delegation</span></span>

## <span data-ttu-id="6bcbc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bcbc-112">PARAMETERS</span></span>

### <span data-ttu-id="6bcbc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="6bcbc-113">-Force</span></span>
<span data-ttu-id="6bcbc-114">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="6bcbc-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6bcbc-115">-Name</span></span>
<span data-ttu-id="6bcbc-116">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="6bcbc-117">-OfferName</span><span class="sxs-lookup"><span data-stu-id="6bcbc-117">-OfferName</span></span>
<span data-ttu-id="6bcbc-118">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-118">Name of an offer.</span></span>

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

### <span data-ttu-id="6bcbc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bcbc-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bcbc-120">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6bcbc-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6bcbc-121">-ResourceId</span></span>
<span data-ttu-id="6bcbc-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-122">The resource id.</span></span>

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

### <span data-ttu-id="6bcbc-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="6bcbc-123">-Confirm</span></span>
<span data-ttu-id="6bcbc-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bcbc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bcbc-125">-WhatIf</span></span>
<span data-ttu-id="6bcbc-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bcbc-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bcbc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bcbc-128">CommonParameters</span></span>
<span data-ttu-id="6bcbc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bcbc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bcbc-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bcbc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bcbc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bcbc-131">INPUTS</span></span>

## <span data-ttu-id="6bcbc-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bcbc-132">OUTPUTS</span></span>

## <span data-ttu-id="6bcbc-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bcbc-133">NOTES</span></span>

## <span data-ttu-id="6bcbc-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bcbc-134">RELATED LINKS</span></span>

