---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935027"
---
# <span data-ttu-id="120a1-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="120a1-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="120a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="120a1-102">SYNOPSIS</span></span>
<span data-ttu-id="120a1-103">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="120a1-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="120a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="120a1-104">SYNTAX</span></span>

### <span data-ttu-id="120a1-105">UpdateRuns_Rerun (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="120a1-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="120a1-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="120a1-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="120a1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="120a1-107">DESCRIPTION</span></span>
<span data-ttu-id="120a1-108">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="120a1-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="120a1-109">Resumeed güncelleştirme çalıştırmaları son başarısız olan noktada devam eder.</span><span class="sxs-lookup"><span data-stu-id="120a1-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="120a1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="120a1-110">EXAMPLES</span></span>

### <span data-ttu-id="120a1-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="120a1-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="120a1-112">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="120a1-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="120a1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="120a1-113">PARAMETERS</span></span>

### <span data-ttu-id="120a1-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="120a1-114">-Name</span></span>
<span data-ttu-id="120a1-115">Çalışma tanımlayıcısını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="120a1-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a1-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="120a1-116">-Location</span></span>
<span data-ttu-id="120a1-117">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="120a1-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="120a1-118">-ResourceGroupName</span></span>
<span data-ttu-id="120a1-119">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="120a1-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a1-120">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="120a1-120">-UpdateName</span></span>
<span data-ttu-id="120a1-121">Güncelleştirmenin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="120a1-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="120a1-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="120a1-122">-AsJob</span></span>
<span data-ttu-id="120a1-123">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="120a1-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="120a1-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="120a1-124">-ResourceId</span></span>
<span data-ttu-id="120a1-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="120a1-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="120a1-126">-Force</span><span class="sxs-lookup"><span data-stu-id="120a1-126">-Force</span></span>
<span data-ttu-id="120a1-127">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="120a1-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="120a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="120a1-128">-WhatIf</span></span>
<span data-ttu-id="120a1-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="120a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="120a1-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="120a1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="120a1-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="120a1-131">-Confirm</span></span>
<span data-ttu-id="120a1-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="120a1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="120a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="120a1-133">CommonParameters</span></span>
<span data-ttu-id="120a1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="120a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="120a1-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="120a1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="120a1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="120a1-136">INPUTS</span></span>

## <span data-ttu-id="120a1-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="120a1-137">OUTPUTS</span></span>

## <span data-ttu-id="120a1-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="120a1-138">NOTES</span></span>

## <span data-ttu-id="120a1-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="120a1-139">RELATED LINKS</span></span>