---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934793"
---
# <span data-ttu-id="c25df-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="c25df-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="c25df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c25df-102">SYNOPSIS</span></span>
<span data-ttu-id="c25df-103">Bir kotayı ada göre silme.</span><span class="sxs-lookup"><span data-stu-id="c25df-103">Delete a quota by name.</span></span>

## <span data-ttu-id="c25df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c25df-104">SYNTAX</span></span>

### <span data-ttu-id="c25df-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c25df-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c25df-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="c25df-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c25df-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c25df-107">DESCRIPTION</span></span>
<span data-ttu-id="c25df-108">Bir kotayı ada göre silme.</span><span class="sxs-lookup"><span data-stu-id="c25df-108">Delete a quota by name.</span></span>

## <span data-ttu-id="c25df-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c25df-109">EXAMPLES</span></span>

### <span data-ttu-id="c25df-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="c25df-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="c25df-111">Ağ kotasını ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c25df-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="c25df-112">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="c25df-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="c25df-113">Kanal kullanarak ağ kotasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c25df-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="c25df-114">ÖRNEK 3</span><span class="sxs-lookup"><span data-stu-id="c25df-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="c25df-115">Ağ kotasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="c25df-115">Remove a network quota.</span></span>

## <span data-ttu-id="c25df-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c25df-116">PARAMETERS</span></span>

### <span data-ttu-id="c25df-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c25df-117">-Name</span></span>
<span data-ttu-id="c25df-118">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="c25df-118">Name of the resource.</span></span>

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

### <span data-ttu-id="c25df-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="c25df-119">-Location</span></span>
<span data-ttu-id="c25df-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="c25df-120">Location of the resource.</span></span>

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

### <span data-ttu-id="c25df-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c25df-121">-ResourceId</span></span>
<span data-ttu-id="c25df-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c25df-122">The resource id.</span></span>

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

### <span data-ttu-id="c25df-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="c25df-123">-AsJob</span></span>
<span data-ttu-id="c25df-124">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="c25df-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="c25df-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c25df-125">-Force</span></span>
<span data-ttu-id="c25df-126">Onayınızı istemeyecektir.</span><span class="sxs-lookup"><span data-stu-id="c25df-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="c25df-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25df-127">-WhatIf</span></span>
<span data-ttu-id="c25df-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c25df-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c25df-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c25df-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25df-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c25df-130">-Confirm</span></span>
<span data-ttu-id="c25df-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c25df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25df-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25df-132">CommonParameters</span></span>
<span data-ttu-id="c25df-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c25df-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25df-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c25df-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25df-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c25df-135">INPUTS</span></span>

## <span data-ttu-id="c25df-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c25df-136">OUTPUTS</span></span>

## <span data-ttu-id="c25df-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c25df-137">NOTES</span></span>

## <span data-ttu-id="c25df-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c25df-138">RELATED LINKS</span></span>
