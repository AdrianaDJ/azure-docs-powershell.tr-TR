---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 752bd7f183bf5a5bdad7950e6567024cbe5b8dec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935103"
---
# <span data-ttu-id="2f78b-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="2f78b-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="2f78b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f78b-102">SYNOPSIS</span></span>
<span data-ttu-id="2f78b-103">Her hizmetin durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f78b-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="2f78b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f78b-104">SYNTAX</span></span>

### <span data-ttu-id="2f78b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f78b-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2f78b-106">Al</span><span class="sxs-lookup"><span data-stu-id="2f78b-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2f78b-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="2f78b-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2f78b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f78b-108">DESCRIPTION</span></span>
<span data-ttu-id="2f78b-109">Her hizmetin durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f78b-109">Returns a list of each service's health.</span></span> <span data-ttu-id="2f78b-110">AlertSummary özelliği, uyarı/hata sayıları hakkında ayrıntılar içerir.</span><span class="sxs-lookup"><span data-stu-id="2f78b-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="2f78b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f78b-111">EXAMPLES</span></span>

### <span data-ttu-id="2f78b-112">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="2f78b-112">EXAMPLE 1</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="2f78b-113">Her hizmetin durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f78b-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="2f78b-114">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="2f78b-114">EXAMPLE 2</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="2f78b-115">Hizmetin durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f78b-115">Returns a service's health.</span></span>

## <span data-ttu-id="2f78b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f78b-116">PARAMETERS</span></span>

### <span data-ttu-id="2f78b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2f78b-117">-Name</span></span>
<span data-ttu-id="2f78b-118">Hizmet durumu adı.</span><span class="sxs-lookup"><span data-stu-id="2f78b-118">Service Health name.</span></span>

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

### <span data-ttu-id="2f78b-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="2f78b-119">-Location</span></span>
<span data-ttu-id="2f78b-120">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="2f78b-120">Name of the region</span></span>

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

### <span data-ttu-id="2f78b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f78b-121">-ResourceGroupName</span></span>
<span data-ttu-id="2f78b-122">Kaynak grubunun adı, isteğe bağlı.</span><span class="sxs-lookup"><span data-stu-id="2f78b-122">Name of the resource group, optional.</span></span>

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

### <span data-ttu-id="2f78b-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2f78b-123">-ResourceId</span></span>
<span data-ttu-id="2f78b-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2f78b-124">The resource id.</span></span>

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

### <span data-ttu-id="2f78b-125">-Filtre</span><span class="sxs-lookup"><span data-stu-id="2f78b-125">-Filter</span></span>
<span data-ttu-id="2f78b-126">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="2f78b-126">OData filter parameter.</span></span>

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

### <span data-ttu-id="2f78b-127">-Atla</span><span class="sxs-lookup"><span data-stu-id="2f78b-127">-Skip</span></span>
<span data-ttu-id="2f78b-128">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="2f78b-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2f78b-129">-Üst</span><span class="sxs-lookup"><span data-stu-id="2f78b-129">-Top</span></span>
<span data-ttu-id="2f78b-130">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="2f78b-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2f78b-131">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="2f78b-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2f78b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f78b-132">CommonParameters</span></span>
<span data-ttu-id="2f78b-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f78b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f78b-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f78b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f78b-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f78b-135">INPUTS</span></span>

## <span data-ttu-id="2f78b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f78b-136">OUTPUTS</span></span>

### <span data-ttu-id="2f78b-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="2f78b-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="2f78b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f78b-138">NOTES</span></span>

## <span data-ttu-id="2f78b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f78b-139">RELATED LINKS</span></span>
