---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3760ecd9c0bc9fd62e49ee8163dfe24ae190985e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934612"
---
# <span data-ttu-id="aac0f-101">Get-AzsStorageSystem</span><span class="sxs-lookup"><span data-stu-id="aac0f-101">Get-AzsStorageSystem</span></span>

## <span data-ttu-id="aac0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac0f-102">SYNOPSIS</span></span>
<span data-ttu-id="aac0f-103">Bir konum için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="aac0f-103">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="aac0f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aac0f-104">SYNTAX</span></span>

### <span data-ttu-id="aac0f-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aac0f-105">List (Default)</span></span>
```
Get-AzsStorageSystem [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="aac0f-106">Al</span><span class="sxs-lookup"><span data-stu-id="aac0f-106">Get</span></span>
```
Get-AzsStorageSystem [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="aac0f-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="aac0f-107">ResourceId</span></span>
```
Get-AzsStorageSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="aac0f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aac0f-108">DESCRIPTION</span></span>
<span data-ttu-id="aac0f-109">Bir konum için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="aac0f-109">Returns a list of all storage subsystems for a location.</span></span>

## <span data-ttu-id="aac0f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aac0f-110">EXAMPLES</span></span>

### <span data-ttu-id="aac0f-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="aac0f-111">EXAMPLE 1</span></span>
```
Get-AzsStorageSystem
```

<span data-ttu-id="aac0f-112">Tüm depolama alt sistemlerini bir konumdan alın.</span><span class="sxs-lookup"><span data-stu-id="aac0f-112">Get all storage subsystems from a location.</span></span>

### <span data-ttu-id="aac0f-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="aac0f-113">EXAMPLE 2</span></span>
```
Get-AzsStorageSystem -Name S-Cluster.azurestack.local
```

<span data-ttu-id="aac0f-114">Bir konum ve ad verilen bir depolama alt sistemine sahip olun.</span><span class="sxs-lookup"><span data-stu-id="aac0f-114">Get a storage subsystem given a location and name.</span></span>

## <span data-ttu-id="aac0f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aac0f-115">PARAMETERS</span></span>

### <span data-ttu-id="aac0f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="aac0f-116">-Name</span></span>
<span data-ttu-id="aac0f-117">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="aac0f-117">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="aac0f-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="aac0f-118">-Location</span></span>
<span data-ttu-id="aac0f-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="aac0f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="aac0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="aac0f-121">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="aac0f-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="aac0f-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="aac0f-122">-ResourceId</span></span>
<span data-ttu-id="aac0f-123">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="aac0f-123">The resource id.</span></span>

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

### <span data-ttu-id="aac0f-124">-Filtre</span><span class="sxs-lookup"><span data-stu-id="aac0f-124">-Filter</span></span>
<span data-ttu-id="aac0f-125">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="aac0f-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="aac0f-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="aac0f-126">-Skip</span></span>
<span data-ttu-id="aac0f-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="aac0f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="aac0f-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="aac0f-128">-Top</span></span>
<span data-ttu-id="aac0f-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="aac0f-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="aac0f-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="aac0f-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="aac0f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac0f-131">CommonParameters</span></span>
<span data-ttu-id="aac0f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aac0f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac0f-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac0f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac0f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aac0f-134">INPUTS</span></span>

## <span data-ttu-id="aac0f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aac0f-135">OUTPUTS</span></span>

### <span data-ttu-id="aac0f-136">Microsoft. AzureStack. Management. Fabric. admin. modeller. StorageSystem</span><span class="sxs-lookup"><span data-stu-id="aac0f-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSystem</span></span>

## <span data-ttu-id="aac0f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aac0f-137">NOTES</span></span>

## <span data-ttu-id="aac0f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aac0f-138">RELATED LINKS</span></span>
