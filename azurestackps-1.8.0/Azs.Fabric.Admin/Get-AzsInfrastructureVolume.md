---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: deaefa8e98e27572fb3faa9443c296e5a15accb0
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934633"
---
# <span data-ttu-id="ce500-101">Get-AzsInfrastructureVolume</span><span class="sxs-lookup"><span data-stu-id="ce500-101">Get-AzsInfrastructureVolume</span></span>

## <span data-ttu-id="ce500-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce500-102">SYNOPSIS</span></span>
<span data-ttu-id="ce500-103">Bir konumdaki tüm depolama birimlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce500-103">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="ce500-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce500-104">SYNTAX</span></span>

### <span data-ttu-id="ce500-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ce500-105">List (Default)</span></span>
```
Get-AzsInfrastructureVolume -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ce500-106">Al</span><span class="sxs-lookup"><span data-stu-id="ce500-106">Get</span></span>
```
Get-AzsInfrastructureVolume -Name <String> -StoragePool <String> -StorageSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ce500-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="ce500-107">ResourceId</span></span>
```
Get-AzsInfrastructureVolume -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ce500-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce500-108">DESCRIPTION</span></span>
<span data-ttu-id="ce500-109">Bir konumdaki tüm depolama birimlerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ce500-109">Returns a list of all storage volumes at a location.</span></span>

## <span data-ttu-id="ce500-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce500-110">EXAMPLES</span></span>

### <span data-ttu-id="ce500-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="ce500-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="ce500-112">Belirli bir yerdeki tüm depolama birimlerinin listesini alma.</span><span class="sxs-lookup"><span data-stu-id="ce500-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="ce500-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="ce500-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureVolume -StoragePool SU1_Pool -StorageSystem S-Cluster.azurestack.local -Name a42d219b
```

<span data-ttu-id="ce500-114">Belirli bir konumda ada göre bir depolama birimi alın.</span><span class="sxs-lookup"><span data-stu-id="ce500-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="ce500-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce500-115">PARAMETERS</span></span>

### <span data-ttu-id="ce500-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce500-116">-Name</span></span>
<span data-ttu-id="ce500-117">Depolama biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="ce500-117">Name of the storage volume.</span></span>

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

### <span data-ttu-id="ce500-118">-StoragePool</span><span class="sxs-lookup"><span data-stu-id="ce500-118">-StoragePool</span></span>
<span data-ttu-id="ce500-119">Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="ce500-119">Storage pool name.</span></span>

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

### <span data-ttu-id="ce500-120">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="ce500-120">-StorageSystem</span></span>
<span data-ttu-id="ce500-121">Depolama sistemi kaynağının temsili.</span><span class="sxs-lookup"><span data-stu-id="ce500-121">Representation of a storage system resource.</span></span>

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

### <span data-ttu-id="ce500-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="ce500-122">-Location</span></span>
<span data-ttu-id="ce500-123">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="ce500-123">Location of the resource.</span></span>

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

### <span data-ttu-id="ce500-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce500-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce500-125">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="ce500-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="ce500-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ce500-126">-ResourceId</span></span>
<span data-ttu-id="ce500-127">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="ce500-127">The resource id.</span></span>

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

### <span data-ttu-id="ce500-128">-Filtre</span><span class="sxs-lookup"><span data-stu-id="ce500-128">-Filter</span></span>
<span data-ttu-id="ce500-129">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="ce500-129">OData filter parameter.</span></span>

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

### <span data-ttu-id="ce500-130">-Atla</span><span class="sxs-lookup"><span data-stu-id="ce500-130">-Skip</span></span>
<span data-ttu-id="ce500-131">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="ce500-131">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ce500-132">-Üst</span><span class="sxs-lookup"><span data-stu-id="ce500-132">-Top</span></span>
<span data-ttu-id="ce500-133">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="ce500-133">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ce500-134">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ce500-134">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ce500-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce500-135">CommonParameters</span></span>
<span data-ttu-id="ce500-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce500-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce500-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce500-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce500-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce500-138">INPUTS</span></span>

## <span data-ttu-id="ce500-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce500-139">OUTPUTS</span></span>

### <span data-ttu-id="ce500-140">Microsoft. AzureStack. Management. Fabric. admin. modeller. Volume</span><span class="sxs-lookup"><span data-stu-id="ce500-140">Microsoft.AzureStack.Management.Fabric.Admin.Models.Volume</span></span>

## <span data-ttu-id="ce500-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce500-141">NOTES</span></span>

## <span data-ttu-id="ce500-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce500-142">RELATED LINKS</span></span>
