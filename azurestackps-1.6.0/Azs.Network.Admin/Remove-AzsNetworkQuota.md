---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572242"
---
# <span data-ttu-id="deeea-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="deeea-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="deeea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="deeea-102">SYNOPSIS</span></span>
<span data-ttu-id="deeea-103">Bir kotayı ada göre silme.</span><span class="sxs-lookup"><span data-stu-id="deeea-103">Delete a quota by name.</span></span>

## <span data-ttu-id="deeea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="deeea-104">SYNTAX</span></span>

### <span data-ttu-id="deeea-105">Sil (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="deeea-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="deeea-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="deeea-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deeea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="deeea-107">DESCRIPTION</span></span>
<span data-ttu-id="deeea-108">Bir kotayı ada göre silme.</span><span class="sxs-lookup"><span data-stu-id="deeea-108">Delete a quota by name.</span></span>

## <span data-ttu-id="deeea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="deeea-109">EXAMPLES</span></span>

### <span data-ttu-id="deeea-110">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="deeea-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="deeea-111">Ağ kotasını ada göre kaldırma.</span><span class="sxs-lookup"><span data-stu-id="deeea-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="deeea-112">--------------------------ÖRNEK 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="deeea-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="deeea-113">Kanal kullanarak ağ kotasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="deeea-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="deeea-114">--------------------------ÖRNEK 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="deeea-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="deeea-115">Ağ kotasını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="deeea-115">Remove a network quota.</span></span>

## <span data-ttu-id="deeea-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="deeea-116">PARAMETERS</span></span>

### <span data-ttu-id="deeea-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="deeea-117">-AsJob</span></span>
<span data-ttu-id="deeea-118">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="deeea-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="deeea-119">-Force</span><span class="sxs-lookup"><span data-stu-id="deeea-119">-Force</span></span>
<span data-ttu-id="deeea-120">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="deeea-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="deeea-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="deeea-121">-Location</span></span>
<span data-ttu-id="deeea-122">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="deeea-122">Location of the resource.</span></span>

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

### <span data-ttu-id="deeea-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="deeea-123">-Name</span></span>
<span data-ttu-id="deeea-124">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="deeea-124">Name of the resource.</span></span>

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

### <span data-ttu-id="deeea-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="deeea-125">-ResourceId</span></span>
<span data-ttu-id="deeea-126">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="deeea-126">The resource id.</span></span>

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

### <span data-ttu-id="deeea-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="deeea-127">-Confirm</span></span>
<span data-ttu-id="deeea-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="deeea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deeea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deeea-129">-WhatIf</span></span>
<span data-ttu-id="deeea-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="deeea-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deeea-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="deeea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deeea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deeea-132">CommonParameters</span></span>
<span data-ttu-id="deeea-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="deeea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deeea-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deeea-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deeea-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="deeea-135">INPUTS</span></span>

## <span data-ttu-id="deeea-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="deeea-136">OUTPUTS</span></span>

## <span data-ttu-id="deeea-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="deeea-137">NOTES</span></span>

## <span data-ttu-id="deeea-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="deeea-138">RELATED LINKS</span></span>

