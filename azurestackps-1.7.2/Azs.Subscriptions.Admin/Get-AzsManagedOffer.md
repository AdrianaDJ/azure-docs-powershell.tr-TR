---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66d8deb8551dfee98c15fcc5524c993c741bca0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934496"
---
# <span data-ttu-id="3cffc-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="3cffc-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="3cffc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cffc-102">SYNOPSIS</span></span>
<span data-ttu-id="3cffc-103">Teklifler listesini işleç olarak alın.</span><span class="sxs-lookup"><span data-stu-id="3cffc-103">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="3cffc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cffc-104">SYNTAX</span></span>

### <span data-ttu-id="3cffc-105">ListAll (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3cffc-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3cffc-106">Al</span><span class="sxs-lookup"><span data-stu-id="3cffc-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="3cffc-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="3cffc-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3cffc-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="3cffc-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3cffc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cffc-109">DESCRIPTION</span></span>
<span data-ttu-id="3cffc-110">Teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="3cffc-110">Get the list of offers.</span></span>

## <span data-ttu-id="3cffc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cffc-111">EXAMPLES</span></span>

### <span data-ttu-id="3cffc-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3cffc-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="3cffc-113">Teklifler listesini işleç olarak alın.</span><span class="sxs-lookup"><span data-stu-id="3cffc-113">Get the list of offers as the operator.</span></span>

## <span data-ttu-id="3cffc-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cffc-114">PARAMETERS</span></span>

### <span data-ttu-id="3cffc-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="3cffc-115">-Name</span></span>
<span data-ttu-id="3cffc-116">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="3cffc-116">Name of an offer.</span></span>

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

### <span data-ttu-id="3cffc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cffc-117">-ResourceGroupName</span></span>
<span data-ttu-id="3cffc-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="3cffc-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="3cffc-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3cffc-119">-ResourceId</span></span>
<span data-ttu-id="3cffc-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3cffc-120">The resource id.</span></span>

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

### <span data-ttu-id="3cffc-121">-Atla</span><span class="sxs-lookup"><span data-stu-id="3cffc-121">-Skip</span></span>
<span data-ttu-id="3cffc-122">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="3cffc-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3cffc-123">-Üst</span><span class="sxs-lookup"><span data-stu-id="3cffc-123">-Top</span></span>
<span data-ttu-id="3cffc-124">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="3cffc-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3cffc-125">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3cffc-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3cffc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cffc-126">CommonParameters</span></span>
<span data-ttu-id="3cffc-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cffc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cffc-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cffc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cffc-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cffc-129">INPUTS</span></span>

## <span data-ttu-id="3cffc-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cffc-130">OUTPUTS</span></span>

### <span data-ttu-id="3cffc-131">Microsoft. AzureStack. Management. abonelikler. admin. modeller. teklifini</span><span class="sxs-lookup"><span data-stu-id="3cffc-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="3cffc-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cffc-132">NOTES</span></span>

## <span data-ttu-id="3cffc-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cffc-133">RELATED LINKS</span></span>
