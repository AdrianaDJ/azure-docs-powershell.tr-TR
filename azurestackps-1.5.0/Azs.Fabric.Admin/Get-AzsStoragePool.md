---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25243539ef01a7476b6b0befb2d5cb29595001ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571774"
---
# <span data-ttu-id="c7532-101">Get-AzsStoragePool</span><span class="sxs-lookup"><span data-stu-id="c7532-101">Get-AzsStoragePool</span></span>

## <span data-ttu-id="c7532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7532-102">SYNOPSIS</span></span>
<span data-ttu-id="c7532-103">Bir konum için tüm depolama havuzları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c7532-103">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="c7532-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7532-104">SYNTAX</span></span>

### <span data-ttu-id="c7532-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7532-105">List (Default)</span></span>
```
Get-AzsStoragePool -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c7532-106">Al</span><span class="sxs-lookup"><span data-stu-id="c7532-106">Get</span></span>
```
Get-AzsStoragePool -Name <String> -StorageSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7532-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="c7532-107">ResourceId</span></span>
```
Get-AzsStoragePool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c7532-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7532-108">DESCRIPTION</span></span>
<span data-ttu-id="c7532-109">Bir konum için tüm depolama havuzları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c7532-109">Returns a list of all storage pools for a location.</span></span>

## <span data-ttu-id="c7532-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7532-110">EXAMPLES</span></span>

### <span data-ttu-id="c7532-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c7532-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local
```

<span data-ttu-id="c7532-112">Tüm depolama havuzlarını belirli bir konumda alma.</span><span class="sxs-lookup"><span data-stu-id="c7532-112">Get all storage pools at a given location.</span></span>

### <span data-ttu-id="c7532-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c7532-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStoragePool -StorageSubSystem S-Cluster.azurestack.local -Name "SU1_Pool"
```

<span data-ttu-id="c7532-114">Bir depolama havuzu adı verilen bir konumda depolama havuzları alma.</span><span class="sxs-lookup"><span data-stu-id="c7532-114">Get a storage pools at a given location given a storage pool name.</span></span>

## <span data-ttu-id="c7532-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7532-115">PARAMETERS</span></span>

### <span data-ttu-id="c7532-116">-Filtre</span><span class="sxs-lookup"><span data-stu-id="c7532-116">-Filter</span></span>
<span data-ttu-id="c7532-117">OData filtre parametresi.</span><span class="sxs-lookup"><span data-stu-id="c7532-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c7532-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="c7532-118">-Location</span></span>
<span data-ttu-id="c7532-119">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c7532-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c7532-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7532-120">-Name</span></span>
<span data-ttu-id="c7532-121">Depolama havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="c7532-121">Storage pool name.</span></span>

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

### <span data-ttu-id="c7532-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7532-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7532-123">Kaynak sağlayıcının kaydedildiği kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="c7532-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c7532-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c7532-124">-ResourceId</span></span>
<span data-ttu-id="c7532-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c7532-125">The resource id.</span></span>

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

### <span data-ttu-id="c7532-126">-Atla</span><span class="sxs-lookup"><span data-stu-id="c7532-126">-Skip</span></span>
<span data-ttu-id="c7532-127">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="c7532-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c7532-128">-StorageSystem</span><span class="sxs-lookup"><span data-stu-id="c7532-128">-StorageSystem</span></span>
<span data-ttu-id="c7532-129">Depolama havuzunun bulunduğu depolama sistemi.</span><span class="sxs-lookup"><span data-stu-id="c7532-129">Storage system in which the storage pool is located.</span></span>

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

### <span data-ttu-id="c7532-130">-Üst</span><span class="sxs-lookup"><span data-stu-id="c7532-130">-Top</span></span>
<span data-ttu-id="c7532-131">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="c7532-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c7532-132">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c7532-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c7532-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7532-133">CommonParameters</span></span>
<span data-ttu-id="c7532-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7532-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7532-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7532-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7532-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7532-136">INPUTS</span></span>

## <span data-ttu-id="c7532-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7532-137">OUTPUTS</span></span>

### <span data-ttu-id="c7532-138">Microsoft. AzureStack. Management. Fabric. admin. modeller. StoragePool</span><span class="sxs-lookup"><span data-stu-id="c7532-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.StoragePool</span></span>

## <span data-ttu-id="c7532-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7532-139">NOTES</span></span>

## <span data-ttu-id="c7532-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7532-140">RELATED LINKS</span></span>

