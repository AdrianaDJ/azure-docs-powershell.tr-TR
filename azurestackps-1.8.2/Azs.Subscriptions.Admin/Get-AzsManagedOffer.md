---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106826"
---
# <span data-ttu-id="35909-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="35909-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="35909-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35909-102">SYNOPSIS</span></span>
<span data-ttu-id="35909-103">Teklifler listesini yönetici olarak alın.</span><span class="sxs-lookup"><span data-stu-id="35909-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="35909-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="35909-104">SYNTAX</span></span>

### <span data-ttu-id="35909-105">ListAll (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="35909-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="35909-106">Al</span><span class="sxs-lookup"><span data-stu-id="35909-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="35909-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="35909-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="35909-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="35909-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="35909-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="35909-109">DESCRIPTION</span></span>
<span data-ttu-id="35909-110">Teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="35909-110">Get the list of offers.</span></span>

## <span data-ttu-id="35909-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="35909-111">EXAMPLES</span></span>

### <span data-ttu-id="35909-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="35909-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="35909-113">Teklifler listesini yönetici olarak alın.</span><span class="sxs-lookup"><span data-stu-id="35909-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="35909-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="35909-114">PARAMETERS</span></span>

### <span data-ttu-id="35909-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="35909-115">-Name</span></span>
<span data-ttu-id="35909-116">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="35909-116">Name of an offer.</span></span>

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

### <span data-ttu-id="35909-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35909-117">-ResourceGroupName</span></span>
<span data-ttu-id="35909-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="35909-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="35909-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="35909-119">-ResourceId</span></span>
<span data-ttu-id="35909-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="35909-120">The resource id.</span></span>

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

### <span data-ttu-id="35909-121">-Atla</span><span class="sxs-lookup"><span data-stu-id="35909-121">-Skip</span></span>
<span data-ttu-id="35909-122">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="35909-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="35909-123">-Üst</span><span class="sxs-lookup"><span data-stu-id="35909-123">-Top</span></span>
<span data-ttu-id="35909-124">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="35909-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="35909-125">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="35909-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="35909-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35909-126">CommonParameters</span></span>
<span data-ttu-id="35909-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="35909-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35909-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35909-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35909-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="35909-129">INPUTS</span></span>

## <span data-ttu-id="35909-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="35909-130">OUTPUTS</span></span>

### <span data-ttu-id="35909-131">Microsoft. AzureStack. Management. abonelikler. admin. modeller. teklifini</span><span class="sxs-lookup"><span data-stu-id="35909-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="35909-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="35909-132">NOTES</span></span>

## <span data-ttu-id="35909-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="35909-133">RELATED LINKS</span></span>

