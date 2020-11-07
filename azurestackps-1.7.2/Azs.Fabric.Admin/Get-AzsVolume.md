---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67835cc0ae5191f50aefb79f76148752c68508bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934107"
---
# <span data-ttu-id="c5191-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="c5191-101">Get-AzsVolume</span></span>

## <span data-ttu-id="c5191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5191-102">SYNOPSIS</span></span>
<span data-ttu-id="c5191-103">Bir konumdaki tüm depolama birimlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c5191-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="c5191-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5191-104">SYNTAX</span></span>

### <span data-ttu-id="c5191-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5191-105">List (Default)</span></span>
```
Get-AzsVolume -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c5191-106">Al</span><span class="sxs-lookup"><span data-stu-id="c5191-106">Get</span></span>
```
Get-AzsVolume -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c5191-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="c5191-107">ResourceId</span></span>
```
Get-AzsVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c5191-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5191-108">DESCRIPTION</span></span>
<span data-ttu-id="c5191-109">Bir konumdaki tüm depolama birimlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c5191-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="c5191-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5191-110">EXAMPLES</span></span>

### <span data-ttu-id="c5191-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c5191-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="c5191-112">Belirli bir yerdeki tüm depolama birimlerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="c5191-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="c5191-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c5191-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsVolume -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="c5191-114">Belirli bir konumda ada göre bir depolama birimi alın.</span><span class="sxs-lookup"><span data-stu-id="c5191-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="c5191-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5191-115">PARAMETERS</span></span>

### <span data-ttu-id="c5191-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="c5191-116">-Filter</span></span>
<span data-ttu-id="c5191-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="c5191-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c5191-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="c5191-118">-Location</span></span>
<span data-ttu-id="c5191-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c5191-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c5191-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5191-120">-Name</span></span>
<span data-ttu-id="c5191-121">Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="c5191-121">Name of the storage volume.</span></span>

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

### <span data-ttu-id="c5191-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5191-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5191-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c5191-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c5191-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c5191-124">-ResourceId</span></span>
<span data-ttu-id="c5191-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c5191-125">The resource id.</span></span>

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

### <span data-ttu-id="c5191-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c5191-126">-ScaleUnit</span></span>
<span data-ttu-id="c5191-127">Ölçek birimi adı.</span><span class="sxs-lookup"><span data-stu-id="c5191-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="c5191-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="c5191-128">-StorageSubSystem</span></span>
<span data-ttu-id="c5191-129">Birimin bulunduğu depolama alt sistemi.</span><span class="sxs-lookup"><span data-stu-id="c5191-129">Storage subsystem in which the volume is located.</span></span>

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

### <span data-ttu-id="c5191-130">-Üst</span><span class="sxs-lookup"><span data-stu-id="c5191-130">-Top</span></span>
<span data-ttu-id="c5191-131">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="c5191-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c5191-132">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c5191-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c5191-133">-Atla</span><span class="sxs-lookup"><span data-stu-id="c5191-133">-Skip</span></span>
<span data-ttu-id="c5191-134">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="c5191-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c5191-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5191-135">CommonParameters</span></span>
<span data-ttu-id="c5191-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5191-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5191-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5191-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5191-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5191-138">INPUTS</span></span>

## <span data-ttu-id="c5191-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5191-139">OUTPUTS</span></span>

### <span data-ttu-id="c5191-140">Microsoft. AzureStack. Management. Fabric. admin. modeller. Volume</span><span class="sxs-lookup"><span data-stu-id="c5191-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>
## <span data-ttu-id="c5191-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5191-141">NOTES</span></span>

## <span data-ttu-id="c5191-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5191-142">RELATED LINKS</span></span>
