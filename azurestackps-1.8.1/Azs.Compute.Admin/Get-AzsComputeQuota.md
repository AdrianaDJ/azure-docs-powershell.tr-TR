---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 819cdc45e75c15c38c9ae28c583ac3c73e54f4ac
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935118"
---
# <span data-ttu-id="63a7e-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="63a7e-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="63a7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="63a7e-103">İşlem nesnelerinin kota sınırlarını belirten kotalar döndürür.</span><span class="sxs-lookup"><span data-stu-id="63a7e-103">Returns quotas specifying the quota limits for compute objects.</span></span>

## <span data-ttu-id="63a7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63a7e-104">SYNTAX</span></span>

### <span data-ttu-id="63a7e-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63a7e-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="63a7e-106">Al</span><span class="sxs-lookup"><span data-stu-id="63a7e-106">Get</span></span>
```
Get-AzsComputeQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="63a7e-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="63a7e-107">ResourceId</span></span>
```
Get-AzsComputeQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="63a7e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63a7e-108">DESCRIPTION</span></span>
<span data-ttu-id="63a7e-109">Var olan kotaların listesini alma.</span><span class="sxs-lookup"><span data-stu-id="63a7e-109">Get a list of existing quotas.</span></span>

## <span data-ttu-id="63a7e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63a7e-110">EXAMPLES</span></span>

### <span data-ttu-id="63a7e-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="63a7e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsComputeQuota -Location 'local'
```

<span data-ttu-id="63a7e-112">Tüm işlem kotalarını belirtilen konumda edinin.</span><span class="sxs-lookup"><span data-stu-id="63a7e-112">Get all compute quotas at the specified location.</span></span>

### <span data-ttu-id="63a7e-113">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="63a7e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsComputeQuota 'Default Quota'
```

<span data-ttu-id="63a7e-114">Belirli bir işlem kotası edinin.</span><span class="sxs-lookup"><span data-stu-id="63a7e-114">Get a specific compute quota.</span></span>

## <span data-ttu-id="63a7e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63a7e-115">PARAMETERS</span></span>

### <span data-ttu-id="63a7e-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="63a7e-116">-Location</span></span>
<span data-ttu-id="63a7e-117">{{Dolgu konumu açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="63a7e-117">{{Fill Location Description}}</span></span>

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

### <span data-ttu-id="63a7e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="63a7e-118">-Name</span></span>
<span data-ttu-id="63a7e-119">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="63a7e-119">Name of the quota.</span></span>

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

### <span data-ttu-id="63a7e-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="63a7e-120">-ResourceId</span></span>
<span data-ttu-id="63a7e-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="63a7e-121">The resource id.</span></span>

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

### <span data-ttu-id="63a7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63a7e-122">CommonParameters</span></span>
<span data-ttu-id="63a7e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63a7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63a7e-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63a7e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63a7e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63a7e-125">INPUTS</span></span>

## <span data-ttu-id="63a7e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63a7e-126">OUTPUTS</span></span>

### <span data-ttu-id="63a7e-127">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="63a7e-127">ComputeQuotaObject</span></span>

## <span data-ttu-id="63a7e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63a7e-128">NOTES</span></span>

## <span data-ttu-id="63a7e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63a7e-129">RELATED LINKS</span></span>

