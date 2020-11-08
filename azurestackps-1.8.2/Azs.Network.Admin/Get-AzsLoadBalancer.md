---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b280b9e99fa91c53371d2eff38d42003873951bb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106951"
---
# <span data-ttu-id="91485-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="91485-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="91485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91485-102">SYNOPSIS</span></span>
<span data-ttu-id="91485-103">Tüm yük dengeleyicileri listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="91485-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="91485-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91485-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [[-Filter] <String>] [[-OrderBy] <String>] [[-Skip] <Int32>] [[-Top] <Int32>]
 [[-InlineCount] <String>] [<CommonParameters>]
```

## <span data-ttu-id="91485-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91485-105">DESCRIPTION</span></span>
<span data-ttu-id="91485-106">Tüm yük dengeleyicileri listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="91485-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="91485-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91485-107">EXAMPLES</span></span>

### <span data-ttu-id="91485-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="91485-108">EXAMPLE 1</span></span>
```
Get-AzsLoadBalancer
```

<span data-ttu-id="91485-109">Tüm yük dengeleyicileri listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="91485-109">Get a list of all load balancers.</span></span>

## <span data-ttu-id="91485-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91485-110">PARAMETERS</span></span>

### <span data-ttu-id="91485-111">-Filtre</span><span class="sxs-lookup"><span data-stu-id="91485-111">-Filter</span></span>
<span data-ttu-id="91485-112">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="91485-112">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91485-113">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="91485-113">-OrderBy</span></span>
<span data-ttu-id="91485-114">OData orderBy parametresi.</span><span class="sxs-lookup"><span data-stu-id="91485-114">OData orderBy parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91485-115">-Atla</span><span class="sxs-lookup"><span data-stu-id="91485-115">-Skip</span></span>
<span data-ttu-id="91485-116">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="91485-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91485-117">-Üst</span><span class="sxs-lookup"><span data-stu-id="91485-117">-Top</span></span>
<span data-ttu-id="91485-118">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="91485-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="91485-119">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="91485-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91485-120">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="91485-120">-InlineCount</span></span>
<span data-ttu-id="91485-121">OData satır içi sayısı parametresi.</span><span class="sxs-lookup"><span data-stu-id="91485-121">OData inline count parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91485-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91485-122">CommonParameters</span></span>
<span data-ttu-id="91485-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91485-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91485-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91485-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91485-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91485-125">INPUTS</span></span>

## <span data-ttu-id="91485-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91485-126">OUTPUTS</span></span>

### <span data-ttu-id="91485-127">Microsoft. AzureStack. Management. Network. admin. modeller. LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="91485-127">Microsoft.AzureStack.Management.Network.Admin.Models.LoadBalancer</span></span>

## <span data-ttu-id="91485-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91485-128">NOTES</span></span>

## <span data-ttu-id="91485-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91485-129">RELATED LINKS</span></span>
