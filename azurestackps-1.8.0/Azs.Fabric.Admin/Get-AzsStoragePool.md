---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcc4dbfdd4634c53835c588947a77c4c2e773af4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934615"
---
# <span data-ttu-id="34356-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="34356-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="34356-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34356-102">SYNOPSIS</span></span>
<span data-ttu-id="34356-103">Bir konum için tüm depolama havuzları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="34356-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="34356-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34356-104">SYNTAX</span></span>

### <span data-ttu-id="34356-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34356-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="34356-106">Al</span><span class="sxs-lookup"><span data-stu-id="34356-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="34356-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="34356-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="34356-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34356-108">DESCRIPTION</span></span>
<span data-ttu-id="34356-109">Bir konum için tüm depolama havuzları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="34356-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="34356-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34356-110">EXAMPLES</span></span>

### <span data-ttu-id="34356-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="34356-111">EXAMPLE 1</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local
```

<span data-ttu-id="34356-112">Tüm depolama havuzlarını belirli bir konumda alma.</span><span class="sxs-lookup"><span data-stu-id="34356-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="34356-113">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="34356-113">EXAMPLE 2</span></span>
```
Get-AzsStoragePool -StorageSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="34356-114">Bir depolama havuzu adı verilen bir konumda depolama havuzları alma.</span><span class="sxs-lookup"><span data-stu-id="34356-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="34356-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34356-115">PARAMETERS</span></span>

### <span data-ttu-id="34356-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="34356-116">-Name</span></span>
<span data-ttu-id="34356-117">Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="34356-117">Storage pool name.</span></span>

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

### <span data-ttu-id="34356-118">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="34356-118">-StorageSystem</span></span>
<span data-ttu-id="34356-119">Depolama alt sisteminin adı.</span><span class="sxs-lookup"><span data-stu-id="34356-119">Name of the Storage Sub System.</span></span>

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

### <span data-ttu-id="34356-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="34356-120">-Location</span></span>
<span data-ttu-id="34356-121">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="34356-121">Location of the resource.</span></span>

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

### <span data-ttu-id="34356-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34356-122">-ResourceGroupName</span></span>
<span data-ttu-id="34356-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="34356-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="34356-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="34356-124">-ResourceId</span></span>
<span data-ttu-id="34356-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="34356-125">The resource id.</span></span>

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

### <span data-ttu-id="34356-126">-Filtre</span><span class="sxs-lookup"><span data-stu-id="34356-126">-Filter</span></span>
<span data-ttu-id="34356-127">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="34356-127">OData filter parameter.</span></span>

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

### <span data-ttu-id="34356-128">-Atla</span><span class="sxs-lookup"><span data-stu-id="34356-128">-Skip</span></span>
<span data-ttu-id="34356-129">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="34356-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="34356-130">-Üst</span><span class="sxs-lookup"><span data-stu-id="34356-130">-Top</span></span>
<span data-ttu-id="34356-131">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="34356-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="34356-132">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="34356-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="34356-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34356-133">CommonParameters</span></span>
<span data-ttu-id="34356-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34356-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34356-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34356-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34356-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34356-136">INPUTS</span></span>

## <span data-ttu-id="34356-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34356-137">OUTPUTS</span></span>

### <span data-ttu-id="34356-138">Microsoft. AzureStack. Management. Fabric. admin. modeller. StoragePool</span><span class="sxs-lookup"><span data-stu-id="34356-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="34356-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34356-139">NOTES</span></span>

## <span data-ttu-id="34356-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34356-140">RELATED LINKS</span></span>
