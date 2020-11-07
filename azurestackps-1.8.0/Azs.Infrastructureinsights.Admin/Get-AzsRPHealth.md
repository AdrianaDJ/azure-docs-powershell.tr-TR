---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934699"
---
# <span data-ttu-id="d3384-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="d3384-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="d3384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3384-102">SYNOPSIS</span></span>
<span data-ttu-id="d3384-103">Her hizmetin durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3384-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="d3384-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3384-104">SYNTAX</span></span>

### <span data-ttu-id="d3384-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3384-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="d3384-106">Al</span><span class="sxs-lookup"><span data-stu-id="d3384-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="d3384-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d3384-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d3384-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3384-108">DESCRIPTION</span></span>
<span data-ttu-id="d3384-109">Her hizmetin durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3384-109">Returns a list of each service's health.</span></span> <span data-ttu-id="d3384-110">AlertSummary özelliği, uyarı/hata sayıları hakkında ayrıntılar içerir.</span><span class="sxs-lookup"><span data-stu-id="d3384-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="d3384-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3384-111">EXAMPLES</span></span>

### <span data-ttu-id="d3384-112">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="d3384-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="d3384-113">Her hizmetin durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3384-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="d3384-114">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="d3384-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="d3384-115">Hizmetin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="d3384-115">Returns a service's health.</span></span>

## <span data-ttu-id="d3384-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3384-116">PARAMETERS</span></span>

### <span data-ttu-id="d3384-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3384-117">-Name</span></span>
<span data-ttu-id="d3384-118">Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="d3384-118">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3384-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="d3384-119">-Location</span></span>
<span data-ttu-id="d3384-120">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="d3384-120">Name of the region</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3384-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3384-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3384-122">Kaynak grubunun adı, isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="d3384-122">Name of the resource group, optional.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3384-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3384-123">-ResourceId</span></span>
<span data-ttu-id="d3384-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d3384-124">The resource id.</span></span>

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

### <span data-ttu-id="d3384-125">-Filtre</span><span class="sxs-lookup"><span data-stu-id="d3384-125">-Filter</span></span>
<span data-ttu-id="d3384-126">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="d3384-126">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3384-127">-Atla</span><span class="sxs-lookup"><span data-stu-id="d3384-127">-Skip</span></span>
<span data-ttu-id="d3384-128">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="d3384-128">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3384-129">-Üst</span><span class="sxs-lookup"><span data-stu-id="d3384-129">-Top</span></span>
<span data-ttu-id="d3384-130">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="d3384-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="d3384-131">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d3384-131">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3384-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3384-132">CommonParameters</span></span>
<span data-ttu-id="d3384-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3384-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3384-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3384-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3384-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3384-135">INPUTS</span></span>

## <span data-ttu-id="d3384-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3384-136">OUTPUTS</span></span>

### <span data-ttu-id="d3384-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="d3384-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="d3384-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3384-138">NOTES</span></span>

## <span data-ttu-id="d3384-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3384-139">RELATED LINKS</span></span>
