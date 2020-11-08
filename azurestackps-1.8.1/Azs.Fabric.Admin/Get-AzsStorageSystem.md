---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934952"
---
# <span data-ttu-id="eefd4-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="eefd4-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="eefd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefd4-102">SYNOPSIS</span></span>
<span data-ttu-id="eefd4-103">Bir konum için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="eefd4-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="eefd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eefd4-104">SYNTAX</span></span>

### <span data-ttu-id="eefd4-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eefd4-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="eefd4-106">Al</span><span class="sxs-lookup"><span data-stu-id="eefd4-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="eefd4-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="eefd4-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="eefd4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eefd4-108">DESCRIPTION</span></span>
<span data-ttu-id="eefd4-109">Bir konum için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="eefd4-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="eefd4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eefd4-110">EXAMPLES</span></span>

### <span data-ttu-id="eefd4-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="eefd4-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="eefd4-112">Tüm depolama alt sistemlerini bir konumdan alın.</span><span class="sxs-lookup"><span data-stu-id="eefd4-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="eefd4-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="eefd4-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="eefd4-114">Bir konum ve ad verilen bir depolama alt sistemine sahip olun.</span><span class="sxs-lookup"><span data-stu-id="eefd4-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="eefd4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eefd4-115">PARAMETERS</span></span>

### <span data-ttu-id="eefd4-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="eefd4-116">-Name</span></span>
<span data-ttu-id="eefd4-117">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="eefd4-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="eefd4-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="eefd4-118">-Location</span></span>
<span data-ttu-id="eefd4-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="eefd4-119">Location of the resource.</span></span>

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

### <span data-ttu-id="eefd4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefd4-120">-ResourceGroupName</span></span>
<span data-ttu-id="eefd4-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="eefd4-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="eefd4-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eefd4-122">-ResourceId</span></span>
<span data-ttu-id="eefd4-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="eefd4-123">The resource id.</span></span>

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

### <span data-ttu-id="eefd4-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="eefd4-124">-Filter</span></span>
<span data-ttu-id="eefd4-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="eefd4-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="eefd4-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="eefd4-126">-Skip</span></span>
<span data-ttu-id="eefd4-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="eefd4-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="eefd4-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="eefd4-128">-Top</span></span>
<span data-ttu-id="eefd4-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="eefd4-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="eefd4-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="eefd4-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="eefd4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefd4-131">CommonParameters</span></span>
<span data-ttu-id="eefd4-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eefd4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefd4-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eefd4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefd4-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eefd4-134">INPUTS</span></span>

## <span data-ttu-id="eefd4-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eefd4-135">OUTPUTS</span></span>

### <span data-ttu-id="eefd4-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="eefd4-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="eefd4-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eefd4-137">NOTES</span></span>

## <span data-ttu-id="eefd4-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eefd4-138">RELATED LINKS</span></span>