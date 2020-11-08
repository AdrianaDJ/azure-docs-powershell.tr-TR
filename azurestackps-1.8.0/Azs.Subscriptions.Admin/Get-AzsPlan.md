---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934597"
---
# <span data-ttu-id="a6231-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="a6231-101">Get-AzsPlan</span></span>

## <span data-ttu-id="a6231-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6231-102">SYNOPSIS</span></span>
<span data-ttu-id="a6231-103">Tüm abonelikler genelinde tüm planları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="a6231-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="a6231-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6231-104">SYNTAX</span></span>

### <span data-ttu-id="a6231-105">ListAll (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6231-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a6231-106">Al</span><span class="sxs-lookup"><span data-stu-id="a6231-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="a6231-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="a6231-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="a6231-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="a6231-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="a6231-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6231-109">DESCRIPTION</span></span>
<span data-ttu-id="a6231-110">Tüm abonelikler genelinde tüm planları listeleyin.</span><span class="sxs-lookup"><span data-stu-id="a6231-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="a6231-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6231-111">EXAMPLES</span></span>

### <span data-ttu-id="a6231-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="a6231-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="a6231-113">Bu aboneliklerin altında bir</span><span class="sxs-lookup"><span data-stu-id="a6231-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="a6231-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6231-114">PARAMETERS</span></span>

### <span data-ttu-id="a6231-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6231-115">-Name</span></span>
<span data-ttu-id="a6231-116">Planın adı.</span><span class="sxs-lookup"><span data-stu-id="a6231-116">Name of the plan.</span></span>

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

### <span data-ttu-id="a6231-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6231-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6231-118">Kaynağın altında bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6231-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a6231-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a6231-119">-ResourceId</span></span>
<span data-ttu-id="a6231-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="a6231-120">The resource id.</span></span>

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

### <span data-ttu-id="a6231-121">-Atla</span><span class="sxs-lookup"><span data-stu-id="a6231-121">-Skip</span></span>
<span data-ttu-id="a6231-122">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="a6231-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="a6231-123">-Üst</span><span class="sxs-lookup"><span data-stu-id="a6231-123">-Top</span></span>
<span data-ttu-id="a6231-124">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="a6231-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="a6231-125">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a6231-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="a6231-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6231-126">CommonParameters</span></span>
<span data-ttu-id="a6231-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6231-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6231-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6231-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6231-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6231-129">INPUTS</span></span>

## <span data-ttu-id="a6231-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6231-130">OUTPUTS</span></span>

### <span data-ttu-id="a6231-131">Microsoft. AzureStack. Management. abonelikler. admin. modeller. plan</span><span class="sxs-lookup"><span data-stu-id="a6231-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="a6231-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6231-132">NOTES</span></span>

## <span data-ttu-id="a6231-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6231-133">RELATED LINKS</span></span>
