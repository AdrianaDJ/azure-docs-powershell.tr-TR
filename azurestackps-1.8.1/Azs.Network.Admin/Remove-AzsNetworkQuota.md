---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935083"
---
# <span data-ttu-id="6aadb-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="6aadb-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="6aadb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aadb-102">SYNOPSIS</span></span>
<span data-ttu-id="6aadb-103">Bir kotayı ada göre silme.</span><span class="sxs-lookup"><span data-stu-id="6aadb-103">Delete a quota by name.</span></span>

## <span data-ttu-id="6aadb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6aadb-104">SYNTAX</span></span>

### <span data-ttu-id="6aadb-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6aadb-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6aadb-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="6aadb-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aadb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6aadb-107">DESCRIPTION</span></span>
<span data-ttu-id="6aadb-108">Bir kotayı ada göre silme.</span><span class="sxs-lookup"><span data-stu-id="6aadb-108">Delete a quota by name.</span></span>

## <span data-ttu-id="6aadb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6aadb-109">EXAMPLES</span></span>

### <span data-ttu-id="6aadb-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="6aadb-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="6aadb-111">Ağ kotasını ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6aadb-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="6aadb-112">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="6aadb-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="6aadb-113">Kanal kullanarak ağ kotasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6aadb-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="6aadb-114">ÖRNEK 3</span><span class="sxs-lookup"><span data-stu-id="6aadb-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="6aadb-115">Ağ kotasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6aadb-115">Remove a network quota.</span></span>

## <span data-ttu-id="6aadb-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6aadb-116">PARAMETERS</span></span>

### <span data-ttu-id="6aadb-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6aadb-117">-Name</span></span>
<span data-ttu-id="6aadb-118">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="6aadb-118">Name of the resource.</span></span>

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

### <span data-ttu-id="6aadb-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="6aadb-119">-Location</span></span>
<span data-ttu-id="6aadb-120">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="6aadb-120">Location of the resource.</span></span>

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

### <span data-ttu-id="6aadb-121">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6aadb-121">-ResourceId</span></span>
<span data-ttu-id="6aadb-122">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6aadb-122">The resource id.</span></span>

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

### <span data-ttu-id="6aadb-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="6aadb-123">-AsJob</span></span>
<span data-ttu-id="6aadb-124">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="6aadb-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="6aadb-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6aadb-125">-Force</span></span>
<span data-ttu-id="6aadb-126">Onayınızı istemeyecektir.</span><span class="sxs-lookup"><span data-stu-id="6aadb-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="6aadb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aadb-127">-WhatIf</span></span>
<span data-ttu-id="6aadb-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6aadb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aadb-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6aadb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aadb-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="6aadb-130">-Confirm</span></span>
<span data-ttu-id="6aadb-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6aadb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aadb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aadb-132">CommonParameters</span></span>
<span data-ttu-id="6aadb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6aadb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aadb-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aadb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aadb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6aadb-135">INPUTS</span></span>

## <span data-ttu-id="6aadb-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6aadb-136">OUTPUTS</span></span>

## <span data-ttu-id="6aadb-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6aadb-137">NOTES</span></span>

## <span data-ttu-id="6aadb-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6aadb-138">RELATED LINKS</span></span>
