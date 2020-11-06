---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cab0b994648a414aa164b746a02e3fe1fb848e9c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571301"
---
# <span data-ttu-id="f1f9c-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="f1f9c-101">Get-AzsDrive</span></span>

## <span data-ttu-id="f1f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="f1f9c-103">Verilen kümenin tüm depolama sürücüleri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-103">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="f1f9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1f9c-104">SYNTAX</span></span>

### <span data-ttu-id="f1f9c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1f9c-105">List (Default)</span></span>
```
Get-AzsDrive -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f1f9c-106">Al</span><span class="sxs-lookup"><span data-stu-id="f1f9c-106">Get</span></span>
```
Get-AzsDrive -Name <String> -StorageSubSystem <String> -ScaleUnit <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="f1f9c-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="f1f9c-107">ResourceId</span></span>
```
Get-AzsDrive -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f1f9c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1f9c-108">DESCRIPTION</span></span>
<span data-ttu-id="f1f9c-109">Verilen kümenin tüm depolama sürücüleri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-109">Returns a list of all storage drives for a given cluster.</span></span>

## <span data-ttu-id="f1f9c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1f9c-110">EXAMPLES</span></span>

### <span data-ttu-id="f1f9c-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1f9c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="f1f9c-112">Belirli bir kümenin tüm depolama sürücülerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="f1f9c-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1f9c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDrive -ScaleUnit S-Cluster -StorageSubSystem S-Cluster.azurestack.local -Name a654528c-60bb-18e1-457c-51b7cdb7e14a
```

<span data-ttu-id="f1f9c-114">Belirli bir kümenin adına göre depolama sürücüsüne sahip olun.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="f1f9c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1f9c-115">PARAMETERS</span></span>

### <span data-ttu-id="f1f9c-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="f1f9c-116">-Filter</span></span>
<span data-ttu-id="f1f9c-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="f1f9c-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="f1f9c-118">-Location</span></span>
<span data-ttu-id="f1f9c-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="f1f9c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1f9c-120">-Name</span></span>
<span data-ttu-id="f1f9c-121">Depolama sürücüsünün adı.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-121">Name of the storage drive.</span></span>

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

### <span data-ttu-id="f1f9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1f9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1f9c-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f1f9c-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f1f9c-124">-ResourceId</span></span>
<span data-ttu-id="f1f9c-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-125">The resource id.</span></span>

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

### <span data-ttu-id="f1f9c-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="f1f9c-126">-ScaleUnit</span></span>
<span data-ttu-id="f1f9c-127">Ölçek birimi adı.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="f1f9c-128">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="f1f9c-128">-StorageSubSystem</span></span>
<span data-ttu-id="f1f9c-129">Sürücünün bulunduğu depolama alt sistemi.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-129">Storage subsystem in which the drive is located.</span></span>

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

### <span data-ttu-id="f1f9c-130">-Üst</span><span class="sxs-lookup"><span data-stu-id="f1f9c-130">-Top</span></span>
<span data-ttu-id="f1f9c-131">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f1f9c-132">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f1f9c-133">-Atla</span><span class="sxs-lookup"><span data-stu-id="f1f9c-133">-Skip</span></span>
<span data-ttu-id="f1f9c-134">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-134">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f1f9c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1f9c-135">CommonParameters</span></span>
<span data-ttu-id="f1f9c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1f9c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1f9c-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1f9c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1f9c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1f9c-138">INPUTS</span></span>

## <span data-ttu-id="f1f9c-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1f9c-139">OUTPUTS</span></span>

### <span data-ttu-id="f1f9c-140">Microsoft. AzureStack. Management. Fabric. admin. modeller. Drive</span><span class="sxs-lookup"><span data-stu-id="f1f9c-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Drive</span></span>
## <span data-ttu-id="f1f9c-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1f9c-141">NOTES</span></span>

## <span data-ttu-id="f1f9c-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1f9c-142">RELATED LINKS</span></span>
