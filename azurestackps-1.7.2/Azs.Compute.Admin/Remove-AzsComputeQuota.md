---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b3fb659c1d11df734bdc95f554e4c100060e185
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934509"
---
# <span data-ttu-id="72130-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="72130-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="72130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72130-102">SYNOPSIS</span></span>
<span data-ttu-id="72130-103">Belirtilen işlem kotasını siler.</span><span class="sxs-lookup"><span data-stu-id="72130-103">Deletes specified compute quota.</span></span>

## <span data-ttu-id="72130-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72130-104">SYNTAX</span></span>

### <span data-ttu-id="72130-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="72130-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72130-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="72130-106">ResourceId</span></span>
```
Remove-AzsComputeQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72130-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72130-107">DESCRIPTION</span></span>
<span data-ttu-id="72130-108">Var olan kotayı silme.</span><span class="sxs-lookup"><span data-stu-id="72130-108">Delete an existing quota.</span></span>

## <span data-ttu-id="72130-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72130-109">EXAMPLES</span></span>

### <span data-ttu-id="72130-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="72130-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsComputeQuota -Name ComputeQuota
```

<span data-ttu-id="72130-111">Tüm parametreler verilen bir hesaplama kotasını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="72130-111">Remove a compute quota given all the parameters.</span></span>

## <span data-ttu-id="72130-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72130-112">PARAMETERS</span></span>

### <span data-ttu-id="72130-113">-Force</span><span class="sxs-lookup"><span data-stu-id="72130-113">-Force</span></span>
<span data-ttu-id="72130-114">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="72130-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="72130-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="72130-115">-Location</span></span>
<span data-ttu-id="72130-116">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="72130-116">Location of the resource.</span></span> <span data-ttu-id="72130-117">Verilmezse, varsayılan olarak kullanım aboneliğine bağlı olan konum.</span><span class="sxs-lookup"><span data-stu-id="72130-117">If not given we default to the location bound to the tenat's subscription.</span></span>

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

### <span data-ttu-id="72130-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="72130-118">-Name</span></span>
<span data-ttu-id="72130-119">Kotanın adı.</span><span class="sxs-lookup"><span data-stu-id="72130-119">Name of the quota.</span></span>

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

### <span data-ttu-id="72130-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="72130-120">-ResourceId</span></span>
<span data-ttu-id="72130-121">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="72130-121">The resource id.</span></span>

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

### <span data-ttu-id="72130-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="72130-122">-Confirm</span></span>
<span data-ttu-id="72130-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72130-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72130-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72130-124">-WhatIf</span></span>
<span data-ttu-id="72130-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72130-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72130-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72130-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72130-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72130-127">CommonParameters</span></span>
<span data-ttu-id="72130-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72130-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72130-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72130-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72130-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72130-130">INPUTS</span></span>

## <span data-ttu-id="72130-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72130-131">OUTPUTS</span></span>

## <span data-ttu-id="72130-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72130-132">NOTES</span></span>

## <span data-ttu-id="72130-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72130-133">RELATED LINKS</span></span>
