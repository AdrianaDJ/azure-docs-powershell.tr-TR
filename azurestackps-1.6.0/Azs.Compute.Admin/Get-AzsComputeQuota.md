---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 30a1bc70b4e704d8dadf864dedf7173476909cf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571346"
---
# <span data-ttu-id="88f34-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="88f34-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="88f34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88f34-102">SYNOPSIS</span></span>
<span data-ttu-id="88f34-103">İşlem nesnelerinin kota sınırlarını belirten kotalar döndürür.</span><span class="sxs-lookup"><span data-stu-id="88f34-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="88f34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88f34-104">SYNTAX</span></span>

### <span data-ttu-id="88f34-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88f34-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="88f34-106">Al</span><span class="sxs-lookup"><span data-stu-id="88f34-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="88f34-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="88f34-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="88f34-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="88f34-108">DESCRIPTION</span></span>
<span data-ttu-id="88f34-109">Var olan kotaların listesini alma.</span><span class="sxs-lookup"><span data-stu-id="88f34-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="88f34-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88f34-110">EXAMPLES</span></span>

### <span data-ttu-id="88f34-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="88f34-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="88f34-112">Tüm işlem kotalarını belirtilen konumda edinin.</span><span class="sxs-lookup"><span data-stu-id="88f34-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="88f34-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="88f34-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="88f34-114">Belirli bir işlem kotası edinin.</span><span class="sxs-lookup"><span data-stu-id="88f34-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="88f34-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88f34-115">PARAMETERS</span></span>

### <span data-ttu-id="88f34-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="88f34-116">-Location</span></span>
<span data-ttu-id="88f34-117">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="88f34-117">Location of the resource.</span></span>

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

### <span data-ttu-id="88f34-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="88f34-118">-Name</span></span>
<span data-ttu-id="88f34-119">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="88f34-119">Name of the quota.</span></span>

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

### <span data-ttu-id="88f34-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="88f34-120">-ResourceId</span></span>
<span data-ttu-id="88f34-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="88f34-121">The resource id.</span></span>

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

### <span data-ttu-id="88f34-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f34-122">CommonParameters</span></span>
<span data-ttu-id="88f34-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88f34-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f34-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88f34-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f34-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88f34-125">INPUTS</span></span>

## <span data-ttu-id="88f34-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88f34-126">OUTPUTS</span></span>

### <span data-ttu-id="88f34-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="88f34-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="88f34-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88f34-128">NOTES</span></span>

## <span data-ttu-id="88f34-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88f34-129">RELATED LINKS</span></span>

