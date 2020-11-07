---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935137"
---
# <span data-ttu-id="4f906-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="4f906-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="4f906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f906-102">SYNOPSIS</span></span>
<span data-ttu-id="4f906-103">Teklifler listesini yönetici olarak alın.</span><span class="sxs-lookup"><span data-stu-id="4f906-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="4f906-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f906-104">SYNTAX</span></span>

### <span data-ttu-id="4f906-105">ListAll (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f906-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4f906-106">Al</span><span class="sxs-lookup"><span data-stu-id="4f906-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="4f906-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="4f906-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4f906-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="4f906-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4f906-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f906-109">DESCRIPTION</span></span>
<span data-ttu-id="4f906-110">Teklifler listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="4f906-110">Get the list of offers.</span></span>

## <span data-ttu-id="4f906-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f906-111">EXAMPLES</span></span>

### <span data-ttu-id="4f906-112">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4f906-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="4f906-113">Teklifler listesini yönetici olarak alın.</span><span class="sxs-lookup"><span data-stu-id="4f906-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="4f906-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f906-114">PARAMETERS</span></span>

### <span data-ttu-id="4f906-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f906-115">-Name</span></span>
<span data-ttu-id="4f906-116">Teklifin adı.</span><span class="sxs-lookup"><span data-stu-id="4f906-116">Name of an offer.</span></span>

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

### <span data-ttu-id="4f906-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f906-117">-ResourceGroupName</span></span>
<span data-ttu-id="4f906-118">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4f906-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4f906-119">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4f906-119">-ResourceId</span></span>
<span data-ttu-id="4f906-120">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4f906-120">The resource id.</span></span>

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

### <span data-ttu-id="4f906-121">-Atla</span><span class="sxs-lookup"><span data-stu-id="4f906-121">-Skip</span></span>
<span data-ttu-id="4f906-122">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="4f906-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4f906-123">-Üst</span><span class="sxs-lookup"><span data-stu-id="4f906-123">-Top</span></span>
<span data-ttu-id="4f906-124">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="4f906-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4f906-125">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="4f906-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4f906-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f906-126">CommonParameters</span></span>
<span data-ttu-id="4f906-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f906-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f906-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f906-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f906-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f906-129">INPUTS</span></span>

## <span data-ttu-id="4f906-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f906-130">OUTPUTS</span></span>

### <span data-ttu-id="4f906-131">Microsoft. AzureStack. Management. abonelikler. admin. modeller. teklifini</span><span class="sxs-lookup"><span data-stu-id="4f906-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="4f906-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f906-132">NOTES</span></span>

## <span data-ttu-id="4f906-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f906-133">RELATED LINKS</span></span>

