---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ebc1ebae40d6d1726ee6c23def6f82ff1efc8517
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935002"
---
# <span data-ttu-id="d80c3-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d80c3-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="d80c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d80c3-102">SYNOPSIS</span></span>
<span data-ttu-id="d80c3-103">Belirtilen işlem kotasını siler.</span><span class="sxs-lookup"><span data-stu-id="d80c3-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="d80c3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d80c3-104">SYNTAX</span></span>

### <span data-ttu-id="d80c3-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d80c3-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80c3-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="d80c3-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d80c3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d80c3-107">DESCRIPTION</span></span>
<span data-ttu-id="d80c3-108">Var olan kotayı silme.</span><span class="sxs-lookup"><span data-stu-id="d80c3-108">Delete an existing quota.</span></span>

## <span data-ttu-id="d80c3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d80c3-109">EXAMPLES</span></span>

### <span data-ttu-id="d80c3-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d80c3-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="d80c3-111">Tüm parametreler verilen bir hesaplama kotasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d80c3-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="d80c3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d80c3-112">PARAMETERS</span></span>

### <span data-ttu-id="d80c3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d80c3-113">-Force</span></span>
<span data-ttu-id="d80c3-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="d80c3-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c3-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="d80c3-115">-Location</span></span>
<span data-ttu-id="d80c3-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="d80c3-116">Location of the resource.</span></span> <span data-ttu-id="d80c3-117">Verilmezse, varsayılan olarak kullanım aboneliğine bağlı olan konum.</span><span class="sxs-lookup"><span data-stu-id="d80c3-117">If not given we default to the location bound to the tenat's subscription.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d80c3-118">-Name</span></span>
<span data-ttu-id="d80c3-119">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="d80c3-119">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c3-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d80c3-120">-ResourceId</span></span>
<span data-ttu-id="d80c3-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d80c3-121">The resource id.</span></span>

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

### <span data-ttu-id="d80c3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d80c3-122">-Confirm</span></span>
<span data-ttu-id="d80c3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d80c3-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80c3-124">-WhatIf</span></span>
<span data-ttu-id="d80c3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d80c3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d80c3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d80c3-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80c3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80c3-127">CommonParameters</span></span>
<span data-ttu-id="d80c3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d80c3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80c3-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d80c3-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80c3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d80c3-130">INPUTS</span></span>

## <span data-ttu-id="d80c3-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d80c3-131">OUTPUTS</span></span>

## <span data-ttu-id="d80c3-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d80c3-132">NOTES</span></span>

## <span data-ttu-id="d80c3-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d80c3-133">RELATED LINKS</span></span>
