---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2abc9073b9e7bcbcd4644150ada4c19cd351f660
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934108"
---
# <span data-ttu-id="e54c6-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="e54c6-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="e54c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e54c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e54c6-103">Ölçeklendirme birimi için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e54c6-103">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="e54c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e54c6-104">SYNTAX</span></span>

### <span data-ttu-id="e54c6-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e54c6-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e54c6-106">Al</span><span class="sxs-lookup"><span data-stu-id="e54c6-106">Get</span></span>
```
Get-AzsStorageSubSystem [-Name] <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e54c6-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="e54c6-107">ResourceId</span></span>
```
Get-AzsStorageSubSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="e54c6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e54c6-108">DESCRIPTION</span></span>
<span data-ttu-id="e54c6-109">Ölçeklendirme birimi için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e54c6-109">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="e54c6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e54c6-110">EXAMPLES</span></span>

### <span data-ttu-id="e54c6-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e54c6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster
```

<span data-ttu-id="e54c6-112">Bir ölçek biriminden tüm depolama alt sistemlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="e54c6-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="e54c6-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e54c6-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster -Name S-Cluster.azurestack.local
```

<span data-ttu-id="e54c6-114">Bir ölçeklendirme birimi ve adı verilen bir depolama alt sistemi edinin.</span><span class="sxs-lookup"><span data-stu-id="e54c6-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="e54c6-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e54c6-115">PARAMETERS</span></span>

### <span data-ttu-id="e54c6-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="e54c6-116">-Filter</span></span>
<span data-ttu-id="e54c6-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="e54c6-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="e54c6-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="e54c6-118">-Location</span></span>
<span data-ttu-id="e54c6-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="e54c6-119">Location of the resource.</span></span>

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

### <span data-ttu-id="e54c6-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e54c6-120">-Name</span></span>
<span data-ttu-id="e54c6-121">Depolama alt sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="e54c6-121">Name of the storage subsystem.</span></span>

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

### <span data-ttu-id="e54c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e54c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="e54c6-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e54c6-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e54c6-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e54c6-124">-ResourceId</span></span>
<span data-ttu-id="e54c6-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e54c6-125">The resource id.</span></span>

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

### <span data-ttu-id="e54c6-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e54c6-126">-ScaleUnit</span></span>
<span data-ttu-id="e54c6-127">Ölçek birimi adı.</span><span class="sxs-lookup"><span data-stu-id="e54c6-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="e54c6-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="e54c6-128">-Top</span></span>
<span data-ttu-id="e54c6-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="e54c6-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="e54c6-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e54c6-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="e54c6-131">-Atla</span><span class="sxs-lookup"><span data-stu-id="e54c6-131">-Skip</span></span>
<span data-ttu-id="e54c6-132">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="e54c6-132">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="e54c6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e54c6-133">CommonParameters</span></span>
<span data-ttu-id="e54c6-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e54c6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e54c6-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e54c6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e54c6-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e54c6-136">INPUTS</span></span>

## <span data-ttu-id="e54c6-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e54c6-137">OUTPUTS</span></span>

### <span data-ttu-id="e54c6-138">Microsoft. AzureStack. Management. Fabric. admin. modeller. StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="e54c6-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSubSystem</span></span>
## <span data-ttu-id="e54c6-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e54c6-139">NOTES</span></span>

## <span data-ttu-id="e54c6-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e54c6-140">RELATED LINKS</span></span>
