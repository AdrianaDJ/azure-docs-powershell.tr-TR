---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 362eb6a8d688aab2276fa1166f65474dab488952
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761742"
---
# <span data-ttu-id="477c8-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="477c8-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="477c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="477c8-102">SYNOPSIS</span></span>
<span data-ttu-id="477c8-103">Bir konum için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="477c8-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="477c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="477c8-104">SYNTAX</span></span>

### <span data-ttu-id="477c8-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="477c8-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="477c8-106">Al</span><span class="sxs-lookup"><span data-stu-id="477c8-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="477c8-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="477c8-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="477c8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="477c8-108">DESCRIPTION</span></span>
<span data-ttu-id="477c8-109">Bir konum için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="477c8-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="477c8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="477c8-110">EXAMPLES</span></span>

### <span data-ttu-id="477c8-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="477c8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="477c8-112">Tüm depolama alt sistemlerini bir konumdan alın.</span><span class="sxs-lookup"><span data-stu-id="477c8-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="477c8-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="477c8-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="477c8-114">Bir konum ve ad verilen bir depolama alt sistemine sahip olun.</span><span class="sxs-lookup"><span data-stu-id="477c8-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="477c8-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="477c8-115">PARAMETERS</span></span>

### <span data-ttu-id="477c8-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="477c8-116">-Filter</span></span>
<span data-ttu-id="477c8-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="477c8-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="477c8-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="477c8-118">-Location</span></span>
<span data-ttu-id="477c8-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="477c8-119">Location of the resource.</span></span>

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

### <span data-ttu-id="477c8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="477c8-120">-Name</span></span>
<span data-ttu-id="477c8-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="477c8-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="477c8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477c8-122">-ResourceGroupName</span></span>
<span data-ttu-id="477c8-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="477c8-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="477c8-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="477c8-124">-ResourceId</span></span>
<span data-ttu-id="477c8-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="477c8-125">The resource id.</span></span>

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

### <span data-ttu-id="477c8-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="477c8-126">-Skip</span></span>
<span data-ttu-id="477c8-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="477c8-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="477c8-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="477c8-128">-Top</span></span>
<span data-ttu-id="477c8-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="477c8-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="477c8-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="477c8-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="477c8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477c8-131">CommonParameters</span></span>
<span data-ttu-id="477c8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="477c8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477c8-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477c8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477c8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="477c8-134">INPUTS</span></span>

## <span data-ttu-id="477c8-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="477c8-135">OUTPUTS</span></span>

### <span data-ttu-id="477c8-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="477c8-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="477c8-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="477c8-137">NOTES</span></span>

## <span data-ttu-id="477c8-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="477c8-138">RELATED LINKS</span></span>

