---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4285a7423390f5d9b5384faa63f95c4206840d71
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934860"
---
# <span data-ttu-id="97799-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="97799-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="97799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97799-102">SYNOPSIS</span></span>
<span data-ttu-id="97799-103">Her kaynağın bir hizmet altındaki durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="97799-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="97799-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="97799-104">SYNTAX</span></span>

### <span data-ttu-id="97799-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="97799-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="97799-106">Al</span><span class="sxs-lookup"><span data-stu-id="97799-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> -ResourceRegistrationId <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="97799-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="97799-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="97799-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="97799-108">DESCRIPTION</span></span>
<span data-ttu-id="97799-109">Her kaynağın bir hizmet altındaki durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="97799-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="97799-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="97799-110">EXAMPLES</span></span>

### <span data-ttu-id="97799-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="97799-111">EXAMPLE 1</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="97799-112">Her kaynağın bir hizmet altındaki durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="97799-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="97799-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="97799-113">EXAMPLE 2</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationId $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="97799-114">Bir Microsoft. Fabric. admin için, sistem durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="97799-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="97799-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="97799-115">PARAMETERS</span></span>

### <span data-ttu-id="97799-116">-Serviceregistrationıd</span><span class="sxs-lookup"><span data-stu-id="97799-116">-ServiceRegistrationId</span></span>
<span data-ttu-id="97799-117">Hizmet kayıt kimliği.</span><span class="sxs-lookup"><span data-stu-id="97799-117">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97799-118">-Resourceregistrationıd</span><span class="sxs-lookup"><span data-stu-id="97799-118">-ResourceRegistrationId</span></span>


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

### <span data-ttu-id="97799-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="97799-119">-Location</span></span>
<span data-ttu-id="97799-120">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="97799-120">Name of the region</span></span>

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

### <span data-ttu-id="97799-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97799-121">-ResourceGroupName</span></span>
<span data-ttu-id="97799-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="97799-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="97799-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="97799-123">-ResourceId</span></span>
<span data-ttu-id="97799-124">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="97799-124">The resource id.</span></span>

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

### <span data-ttu-id="97799-125">-Filtre</span><span class="sxs-lookup"><span data-stu-id="97799-125">-Filter</span></span>
<span data-ttu-id="97799-126">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="97799-126">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97799-127">-Üst</span><span class="sxs-lookup"><span data-stu-id="97799-127">-Top</span></span>
<span data-ttu-id="97799-128">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="97799-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="97799-129">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="97799-129">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="97799-130">-Atla</span><span class="sxs-lookup"><span data-stu-id="97799-130">-Skip</span></span>
<span data-ttu-id="97799-131">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="97799-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="97799-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97799-132">CommonParameters</span></span>
<span data-ttu-id="97799-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="97799-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97799-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97799-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97799-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="97799-135">INPUTS</span></span>

## <span data-ttu-id="97799-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="97799-136">OUTPUTS</span></span>

### <span data-ttu-id="97799-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. Resourcesağlık</span><span class="sxs-lookup"><span data-stu-id="97799-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="97799-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="97799-138">NOTES</span></span>

## <span data-ttu-id="97799-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="97799-139">RELATED LINKS</span></span>
