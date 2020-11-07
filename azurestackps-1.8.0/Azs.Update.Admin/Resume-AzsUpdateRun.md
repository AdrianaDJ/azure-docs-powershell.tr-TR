---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934552"
---
# <span data-ttu-id="8243c-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="8243c-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="8243c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8243c-102">SYNOPSIS</span></span>
<span data-ttu-id="8243c-103">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="8243c-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="8243c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8243c-104">SYNTAX</span></span>

### <span data-ttu-id="8243c-105">UpdateRuns_Rerun (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8243c-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8243c-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="8243c-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8243c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8243c-107">DESCRIPTION</span></span>
<span data-ttu-id="8243c-108">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="8243c-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="8243c-109">Resumeed güncelleştirme çalıştırmaları son başarısız olan noktada devam eder.</span><span class="sxs-lookup"><span data-stu-id="8243c-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="8243c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8243c-110">EXAMPLES</span></span>

### <span data-ttu-id="8243c-111">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="8243c-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="8243c-112">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="8243c-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="8243c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8243c-113">PARAMETERS</span></span>

### <span data-ttu-id="8243c-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="8243c-114">-Name</span></span>
<span data-ttu-id="8243c-115">Çalışma tanımlayıcısını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="8243c-115">Update run identifier.</span></span>

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

### <span data-ttu-id="8243c-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="8243c-116">-Location</span></span>
<span data-ttu-id="8243c-117">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="8243c-117">The name of the update location.</span></span>

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

### <span data-ttu-id="8243c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8243c-118">-ResourceGroupName</span></span>
<span data-ttu-id="8243c-119">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="8243c-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8243c-120">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="8243c-120">-UpdateName</span></span>
<span data-ttu-id="8243c-121">Güncelleştirmenin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="8243c-121">Display name of the update.</span></span>

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

### <span data-ttu-id="8243c-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="8243c-122">-AsJob</span></span>
<span data-ttu-id="8243c-123">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="8243c-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="8243c-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8243c-124">-ResourceId</span></span>
<span data-ttu-id="8243c-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8243c-125">The resource id.</span></span>

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

### <span data-ttu-id="8243c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8243c-126">-Force</span></span>
<span data-ttu-id="8243c-127">Onay işareti olmadan öğeyi kaldırma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="8243c-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="8243c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8243c-128">-WhatIf</span></span>
<span data-ttu-id="8243c-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8243c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8243c-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8243c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8243c-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8243c-131">-Confirm</span></span>
<span data-ttu-id="8243c-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8243c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8243c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8243c-133">CommonParameters</span></span>
<span data-ttu-id="8243c-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8243c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8243c-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8243c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8243c-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8243c-136">INPUTS</span></span>

## <span data-ttu-id="8243c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8243c-137">OUTPUTS</span></span>

## <span data-ttu-id="8243c-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8243c-138">NOTES</span></span>

## <span data-ttu-id="8243c-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8243c-139">RELATED LINKS</span></span>
