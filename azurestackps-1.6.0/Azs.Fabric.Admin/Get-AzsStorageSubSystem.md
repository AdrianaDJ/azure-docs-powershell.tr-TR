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
ms.locfileid: "93571562"
---
# <span data-ttu-id="0dc4c-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="0dc4c-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="0dc4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc4c-103">Ölçeklendirme birimi için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-103">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="0dc4c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0dc4c-104">SYNTAX</span></span>

### <span data-ttu-id="0dc4c-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0dc4c-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0dc4c-106">Al</span><span class="sxs-lookup"><span data-stu-id="0dc4c-106">Get</span></span>
```
Get-AzsStorageSubSystem [-Name] <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0dc4c-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="0dc4c-107">ResourceId</span></span>
```
Get-AzsStorageSubSystem -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="0dc4c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0dc4c-108">DESCRIPTION</span></span>
<span data-ttu-id="0dc4c-109">Ölçeklendirme birimi için tüm depolama alt sistemlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-109">Returns a list of all storage subsystems for a scale unit.</span></span>

## <span data-ttu-id="0dc4c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0dc4c-110">EXAMPLES</span></span>

### <span data-ttu-id="0dc4c-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0dc4c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster
```

<span data-ttu-id="0dc4c-112">Bir ölçek biriminden tüm depolama alt sistemlerini edinin.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="0dc4c-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0dc4c-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit S-Cluster -Name S-Cluster.azurestack.local
```

<span data-ttu-id="0dc4c-114">Bir ölçeklendirme birimi ve adı verilen bir depolama alt sistemi edinin.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="0dc4c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0dc4c-115">PARAMETERS</span></span>

### <span data-ttu-id="0dc4c-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="0dc4c-116">-Filter</span></span>
<span data-ttu-id="0dc4c-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="0dc4c-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="0dc4c-118">-Location</span></span>
<span data-ttu-id="0dc4c-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0dc4c-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0dc4c-120">-Name</span></span>
<span data-ttu-id="0dc4c-121">Depolama alt sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-121">Name of the storage subsystem.</span></span>

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

### <span data-ttu-id="0dc4c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc4c-122">-ResourceGroupName</span></span>
<span data-ttu-id="0dc4c-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0dc4c-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0dc4c-124">-ResourceId</span></span>
<span data-ttu-id="0dc4c-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-125">The resource id.</span></span>

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

### <span data-ttu-id="0dc4c-126">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="0dc4c-126">-ScaleUnit</span></span>
<span data-ttu-id="0dc4c-127">Ölçek birimi adı.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-127">Name of the scale unit.</span></span>

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

### <span data-ttu-id="0dc4c-128">-Üst</span><span class="sxs-lookup"><span data-stu-id="0dc4c-128">-Top</span></span>
<span data-ttu-id="0dc4c-129">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0dc4c-130">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0dc4c-131">-Atla</span><span class="sxs-lookup"><span data-stu-id="0dc4c-131">-Skip</span></span>
<span data-ttu-id="0dc4c-132">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-132">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0dc4c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc4c-133">CommonParameters</span></span>
<span data-ttu-id="0dc4c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0dc4c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc4c-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc4c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc4c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0dc4c-136">INPUTS</span></span>

## <span data-ttu-id="0dc4c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0dc4c-137">OUTPUTS</span></span>

### <span data-ttu-id="0dc4c-138">Microsoft. AzureStack. Management. Fabric. admin. modeller. StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="0dc4c-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StorageSubSystem</span></span>
## <span data-ttu-id="0dc4c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0dc4c-139">NOTES</span></span>

## <span data-ttu-id="0dc4c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0dc4c-140">RELATED LINKS</span></span>
