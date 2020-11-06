---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8fbec7ec2f8bcfc0d7595658f84866cf449d3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571710"
---
# <span data-ttu-id="00c0c-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="00c0c-101">Get-AzsAlert</span></span>

## <span data-ttu-id="00c0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="00c0c-103">Belirli bir konumdaki tüm uyarıların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="00c0c-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="00c0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00c0c-104">SYNTAX</span></span>

### <span data-ttu-id="00c0c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00c0c-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="00c0c-106">Al</span><span class="sxs-lookup"><span data-stu-id="00c0c-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="00c0c-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="00c0c-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="00c0c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="00c0c-108">DESCRIPTION</span></span>
<span data-ttu-id="00c0c-109">Belirli bir konumdaki tüm uyarıların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="00c0c-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="00c0c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00c0c-110">EXAMPLES</span></span>

### <span data-ttu-id="00c0c-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="00c0c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="00c0c-112">Ada göre bir uyarı alın.</span><span class="sxs-lookup"><span data-stu-id="00c0c-112">Get an alert by Name.</span></span>

### <span data-ttu-id="00c0c-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="00c0c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="00c0c-114">Tüm etkin uyarıları alın ve hata ve unvanlarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="00c0c-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="00c0c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00c0c-115">PARAMETERS</span></span>

### <span data-ttu-id="00c0c-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="00c0c-116">-Filter</span></span>
<span data-ttu-id="00c0c-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="00c0c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="00c0c-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="00c0c-118">-Location</span></span>
<span data-ttu-id="00c0c-119">Konumun adı.</span><span class="sxs-lookup"><span data-stu-id="00c0c-119">Name of the location.</span></span>

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

### <span data-ttu-id="00c0c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="00c0c-120">-Name</span></span>
<span data-ttu-id="00c0c-121">Uyarı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="00c0c-121">The alert identifier.</span></span>

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

### <span data-ttu-id="00c0c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00c0c-122">-ResourceGroupName</span></span>
<span data-ttu-id="00c0c-123">Kaynağın bulunduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="00c0c-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="00c0c-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="00c0c-124">-ResourceId</span></span>
<span data-ttu-id="00c0c-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="00c0c-125">The resource id.</span></span>

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

### <span data-ttu-id="00c0c-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="00c0c-126">-Skip</span></span>
<span data-ttu-id="00c0c-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="00c0c-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="00c0c-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="00c0c-128">-Top</span></span>
<span data-ttu-id="00c0c-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="00c0c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="00c0c-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="00c0c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="00c0c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c0c-131">CommonParameters</span></span>
<span data-ttu-id="00c0c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00c0c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c0c-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00c0c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c0c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00c0c-134">INPUTS</span></span>

## <span data-ttu-id="00c0c-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00c0c-135">OUTPUTS</span></span>

### <span data-ttu-id="00c0c-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. Alert</span><span class="sxs-lookup"><span data-stu-id="00c0c-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="00c0c-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00c0c-137">NOTES</span></span>

## <span data-ttu-id="00c0c-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00c0c-138">RELATED LINKS</span></span>

