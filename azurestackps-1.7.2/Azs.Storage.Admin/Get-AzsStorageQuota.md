---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e4277ee88af840674d6fc8e4e2d5f614e745ace
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934007"
---
# <span data-ttu-id="13303-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="13303-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="13303-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13303-102">SYNOPSIS</span></span>
<span data-ttu-id="13303-103">Verilen konumda depolama kotaları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="13303-103">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="13303-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="13303-104">SYNTAX</span></span>

### <span data-ttu-id="13303-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="13303-105">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="13303-106">Al</span><span class="sxs-lookup"><span data-stu-id="13303-106">Get</span></span>
```
Get-AzsStorageQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="13303-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="13303-107">ResourceId</span></span>
```
Get-AzsStorageQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="13303-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="13303-108">DESCRIPTION</span></span>
<span data-ttu-id="13303-109">Verilen konumda depolama kotaları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="13303-109">Returns a list of storage quotas at the given location.</span></span>

## <span data-ttu-id="13303-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="13303-110">EXAMPLES</span></span>

### <span data-ttu-id="13303-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="13303-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageQuota
```

<span data-ttu-id="13303-112">Depolama kotaları listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="13303-112">Get the list of storage quotas.</span></span>

### <span data-ttu-id="13303-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="13303-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name "storagequota1"
```

<span data-ttu-id="13303-114">Belirtilen depolama kotasının ayrıntılarını ada göre edinin.</span><span class="sxs-lookup"><span data-stu-id="13303-114">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="13303-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="13303-115">PARAMETERS</span></span>

### <span data-ttu-id="13303-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="13303-116">-Location</span></span>
<span data-ttu-id="13303-117">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="13303-117">Resource location.</span></span>

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

### <span data-ttu-id="13303-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="13303-118">-Name</span></span>
<span data-ttu-id="13303-119">Depolama kotasının adı.</span><span class="sxs-lookup"><span data-stu-id="13303-119">The name of the storage quota.</span></span>

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

### <span data-ttu-id="13303-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="13303-120">-ResourceId</span></span>
<span data-ttu-id="13303-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="13303-121">The resource id.</span></span>

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

### <span data-ttu-id="13303-122">-Atla</span><span class="sxs-lookup"><span data-stu-id="13303-122">-Skip</span></span>
<span data-ttu-id="13303-123">Parametre değerinde belirtilen ilk N öğeyi atlayın.</span><span class="sxs-lookup"><span data-stu-id="13303-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="13303-124">-Üst</span><span class="sxs-lookup"><span data-stu-id="13303-124">-Top</span></span>
<span data-ttu-id="13303-125">Parametre değerinde belirtildiği gibi ilk N öğeyi döndürün.</span><span class="sxs-lookup"><span data-stu-id="13303-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="13303-126">-Skip parametresinden sonra uygulanır.</span><span class="sxs-lookup"><span data-stu-id="13303-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="13303-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13303-127">CommonParameters</span></span>
<span data-ttu-id="13303-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="13303-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13303-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13303-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13303-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="13303-130">INPUTS</span></span>

## <span data-ttu-id="13303-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="13303-131">OUTPUTS</span></span>

### <span data-ttu-id="13303-132">Microsoft. AzureStack. Management. Storage. admin. modeller. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="13303-132">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="13303-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="13303-133">NOTES</span></span>

## <span data-ttu-id="13303-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="13303-134">RELATED LINKS</span></span>
