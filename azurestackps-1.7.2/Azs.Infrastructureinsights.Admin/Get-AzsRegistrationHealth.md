---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d73e2db2f09ba504e9c6adbf15a0bbc2629452ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934500"
---
# <span data-ttu-id="0719b-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="0719b-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="0719b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0719b-102">SYNOPSIS</span></span>
<span data-ttu-id="0719b-103">Her kaynağın bir hizmet altındaki durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0719b-103">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="0719b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0719b-104">SYNTAX</span></span>

### <span data-ttu-id="0719b-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0719b-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0719b-106">Al</span><span class="sxs-lookup"><span data-stu-id="0719b-106">Get</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName <String> -Name <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="0719b-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="0719b-107">ResourceId</span></span>
```
Get-AzsRegistrationHealth -ResourceId <String> [-Filter <String>] [<CommonParameters>]
```

## <span data-ttu-id="0719b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0719b-108">DESCRIPTION</span></span>
<span data-ttu-id="0719b-109">Her kaynağın bir hizmet altındaki durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0719b-109">Returns a list of each resource's health under a service.</span></span>

## <span data-ttu-id="0719b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0719b-110">EXAMPLES</span></span>

### <span data-ttu-id="0719b-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0719b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="0719b-112">Her kaynağın bir hizmet altındaki durumunun listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0719b-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="0719b-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0719b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="0719b-114">Bir Microsoft. Fabric. admin için, sistem durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="0719b-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="0719b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0719b-115">PARAMETERS</span></span>

### <span data-ttu-id="0719b-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="0719b-116">-Filter</span></span>
<span data-ttu-id="0719b-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="0719b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="0719b-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="0719b-118">-Location</span></span>
<span data-ttu-id="0719b-119">Bölgenin adı</span><span class="sxs-lookup"><span data-stu-id="0719b-119">Name of the region</span></span>

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

### <span data-ttu-id="0719b-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0719b-120">-Name</span></span>
<span data-ttu-id="0719b-121">Kaynak kayıt kimliğine karşılık gelen sağlık nesnesinin kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="0719b-121">The resource name of the health object which corresponds to the resource registration id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0719b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0719b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0719b-123">Kaynağın bulunduğu kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="0719b-123">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="0719b-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0719b-124">-ResourceId</span></span>
<span data-ttu-id="0719b-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0719b-125">The resource id.</span></span>

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

### <span data-ttu-id="0719b-126">-ServiceRegistrationName</span><span class="sxs-lookup"><span data-stu-id="0719b-126">-ServiceRegistrationName</span></span>
<span data-ttu-id="0719b-127">Hizmet kayıt kimliği.</span><span class="sxs-lookup"><span data-stu-id="0719b-127">Service registration id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ServiceRegistrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0719b-128">-Atla</span><span class="sxs-lookup"><span data-stu-id="0719b-128">-Skip</span></span>
<span data-ttu-id="0719b-129">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="0719b-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0719b-130">-Üst</span><span class="sxs-lookup"><span data-stu-id="0719b-130">-Top</span></span>
<span data-ttu-id="0719b-131">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="0719b-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0719b-132">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="0719b-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0719b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0719b-133">CommonParameters</span></span>
<span data-ttu-id="0719b-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0719b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0719b-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0719b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0719b-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0719b-136">INPUTS</span></span>

## <span data-ttu-id="0719b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0719b-137">OUTPUTS</span></span>

### <span data-ttu-id="0719b-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. modeller. Resourcesağlık</span><span class="sxs-lookup"><span data-stu-id="0719b-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ResourceHealth</span></span>

## <span data-ttu-id="0719b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0719b-139">NOTES</span></span>

## <span data-ttu-id="0719b-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0719b-140">RELATED LINKS</span></span>
