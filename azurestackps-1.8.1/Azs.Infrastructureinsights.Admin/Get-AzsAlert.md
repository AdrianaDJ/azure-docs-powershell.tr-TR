---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935105"
---
# <span data-ttu-id="3a820-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="3a820-101">Get-AzsAlert</span></span>

## <span data-ttu-id="3a820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a820-102">SYNOPSIS</span></span>
<span data-ttu-id="3a820-103">Belirli bir konumdaki tüm uyarıların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a820-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="3a820-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a820-104">SYNTAX</span></span>

### <span data-ttu-id="3a820-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a820-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3a820-106">Al</span><span class="sxs-lookup"><span data-stu-id="3a820-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="3a820-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="3a820-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="3a820-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a820-108">DESCRIPTION</span></span>
<span data-ttu-id="3a820-109">Belirli bir konumdaki tüm uyarıların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a820-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="3a820-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a820-110">EXAMPLES</span></span>

### <span data-ttu-id="3a820-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="3a820-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="3a820-112">Ada göre bir uyarı alın.</span><span class="sxs-lookup"><span data-stu-id="3a820-112">Get an alert by Name.</span></span>

### <span data-ttu-id="3a820-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="3a820-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="3a820-114">Tüm etkin uyarıları alın ve hata ve unvanlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="3a820-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="3a820-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a820-115">PARAMETERS</span></span>

### <span data-ttu-id="3a820-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a820-116">-Name</span></span>
<span data-ttu-id="3a820-117">Uyarı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="3a820-117">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a820-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="3a820-118">-Location</span></span>
<span data-ttu-id="3a820-119">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="3a820-119">Name of the location.</span></span>

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

### <span data-ttu-id="3a820-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a820-120">-ResourceGroupName</span></span>
<span data-ttu-id="3a820-121">Uyarının kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3a820-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="3a820-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a820-122">-ResourceId</span></span>
<span data-ttu-id="3a820-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3a820-123">The resource id.</span></span>

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

### <span data-ttu-id="3a820-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="3a820-124">-Filter</span></span>
<span data-ttu-id="3a820-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="3a820-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="3a820-126">-Üst</span><span class="sxs-lookup"><span data-stu-id="3a820-126">-Top</span></span>
<span data-ttu-id="3a820-127">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="3a820-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="3a820-128">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="3a820-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="3a820-129">-Atla</span><span class="sxs-lookup"><span data-stu-id="3a820-129">-Skip</span></span>
<span data-ttu-id="3a820-130">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="3a820-130">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="3a820-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a820-131">CommonParameters</span></span>
<span data-ttu-id="3a820-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a820-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a820-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a820-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a820-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a820-134">INPUTS</span></span>

## <span data-ttu-id="3a820-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a820-135">OUTPUTS</span></span>

### <span data-ttu-id="3a820-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. Alert</span><span class="sxs-lookup"><span data-stu-id="3a820-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="3a820-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a820-137">NOTES</span></span>

## <span data-ttu-id="3a820-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a820-138">RELATED LINKS</span></span>
