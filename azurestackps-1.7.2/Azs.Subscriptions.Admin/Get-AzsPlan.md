---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75fef110a1266ca34bef645f39a879dda4aeeda4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934520"
---
# <span data-ttu-id="487aa-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="487aa-101">Get-AzsPlan</span></span>

## <span data-ttu-id="487aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="487aa-102">SYNOPSIS</span></span>
<span data-ttu-id="487aa-103">Tüm abonelikler genelinde tüm planları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="487aa-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="487aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="487aa-104">SYNTAX</span></span>

### <span data-ttu-id="487aa-105">ListAll (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="487aa-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="487aa-106">Al</span><span class="sxs-lookup"><span data-stu-id="487aa-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="487aa-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="487aa-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="487aa-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="487aa-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="487aa-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="487aa-109">DESCRIPTION</span></span>
<span data-ttu-id="487aa-110">Tüm abonelikler genelinde tüm planları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="487aa-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="487aa-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="487aa-111">EXAMPLES</span></span>

### <span data-ttu-id="487aa-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="487aa-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="487aa-113">Bu aboneliklerin altında bir</span><span class="sxs-lookup"><span data-stu-id="487aa-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="487aa-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="487aa-114">PARAMETERS</span></span>

### <span data-ttu-id="487aa-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="487aa-115">-Name</span></span>
<span data-ttu-id="487aa-116">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="487aa-116">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="487aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="487aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="487aa-118">Kaynağın altında bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="487aa-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="487aa-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="487aa-119">-ResourceId</span></span>
<span data-ttu-id="487aa-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="487aa-120">The resource id.</span></span>

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

### <span data-ttu-id="487aa-121">-Atla</span><span class="sxs-lookup"><span data-stu-id="487aa-121">-Skip</span></span>
<span data-ttu-id="487aa-122">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="487aa-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="487aa-123">-Üst</span><span class="sxs-lookup"><span data-stu-id="487aa-123">-Top</span></span>
<span data-ttu-id="487aa-124">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="487aa-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="487aa-125">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="487aa-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="487aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="487aa-126">CommonParameters</span></span>
<span data-ttu-id="487aa-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="487aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="487aa-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="487aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="487aa-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="487aa-129">INPUTS</span></span>

## <span data-ttu-id="487aa-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="487aa-130">OUTPUTS</span></span>

### <span data-ttu-id="487aa-131">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan</span><span class="sxs-lookup"><span data-stu-id="487aa-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="487aa-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="487aa-132">NOTES</span></span>

## <span data-ttu-id="487aa-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="487aa-133">RELATED LINKS</span></span>

