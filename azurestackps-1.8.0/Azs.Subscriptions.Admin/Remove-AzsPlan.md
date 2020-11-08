---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75010b9591b4211f32c5665aa969bae28d69aaea
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934577"
---
# <span data-ttu-id="d9f46-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="d9f46-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="d9f46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9f46-102">SYNOPSIS</span></span>
<span data-ttu-id="d9f46-103">Belirtilen planı kaldırır</span><span class="sxs-lookup"><span data-stu-id="d9f46-103">Removes the specified plan</span></span>

## <span data-ttu-id="d9f46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9f46-104">SYNTAX</span></span>

### <span data-ttu-id="d9f46-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d9f46-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9f46-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d9f46-106">ResourceId</span></span>
```
Remove-AzsPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9f46-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9f46-107">DESCRIPTION</span></span>
<span data-ttu-id="d9f46-108">Belirtilen planı kaldırır</span><span class="sxs-lookup"><span data-stu-id="d9f46-108">Removes the specified plan</span></span>

## <span data-ttu-id="d9f46-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9f46-109">EXAMPLES</span></span>

### <span data-ttu-id="d9f46-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d9f46-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlan -Name plan1 -ResourceGroupName "rg1"
```

<span data-ttu-id="d9f46-111">Belirtilen planı kaldırır</span><span class="sxs-lookup"><span data-stu-id="d9f46-111">Removes the specified plan</span></span>

## <span data-ttu-id="d9f46-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9f46-112">PARAMETERS</span></span>

### <span data-ttu-id="d9f46-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d9f46-113">-Force</span></span>
<span data-ttu-id="d9f46-114">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="d9f46-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="d9f46-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d9f46-115">-Name</span></span>
<span data-ttu-id="d9f46-116">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="d9f46-116">Name of the plan.</span></span>

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

### <span data-ttu-id="d9f46-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9f46-117">-ResourceGroupName</span></span>
<span data-ttu-id="d9f46-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="d9f46-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="d9f46-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d9f46-119">-ResourceId</span></span>
<span data-ttu-id="d9f46-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d9f46-120">The resource id.</span></span>

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

### <span data-ttu-id="d9f46-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9f46-121">-Confirm</span></span>
<span data-ttu-id="d9f46-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9f46-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9f46-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9f46-123">-WhatIf</span></span>
<span data-ttu-id="d9f46-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9f46-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9f46-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9f46-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9f46-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9f46-126">CommonParameters</span></span>
<span data-ttu-id="d9f46-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9f46-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9f46-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9f46-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9f46-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9f46-129">INPUTS</span></span>

## <span data-ttu-id="d9f46-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9f46-130">OUTPUTS</span></span>

## <span data-ttu-id="d9f46-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9f46-131">NOTES</span></span>

## <span data-ttu-id="d9f46-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9f46-132">RELATED LINKS</span></span>
