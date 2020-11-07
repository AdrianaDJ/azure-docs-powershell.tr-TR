---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19c8f8fce7c3711c5002f9588900e6bdf8efcbb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934315"
---
# <span data-ttu-id="bf6d4-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="bf6d4-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="bf6d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf6d4-102">SYNOPSIS</span></span>
<span data-ttu-id="bf6d4-103">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="bf6d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf6d4-104">SYNTAX</span></span>

### <span data-ttu-id="bf6d4-105">UpdateRuns_Rerun (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf6d4-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf6d4-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="bf6d4-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf6d4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf6d4-107">DESCRIPTION</span></span>
<span data-ttu-id="bf6d4-108">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="bf6d4-109">Resumeed güncelleştirme çalıştırmaları son başarısız olan noktada devam eder.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="bf6d4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf6d4-110">EXAMPLES</span></span>

### <span data-ttu-id="bf6d4-111">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf6d4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="bf6d4-112">Daha önce başlatılan bir güncelleştirme çalıştırmasını devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="bf6d4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf6d4-113">PARAMETERS</span></span>

### <span data-ttu-id="bf6d4-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="bf6d4-114">-AsJob</span></span>
<span data-ttu-id="bf6d4-115">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bf6d4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bf6d4-116">-Force</span></span>
<span data-ttu-id="bf6d4-117">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bf6d4-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="bf6d4-118">-Location</span></span>
<span data-ttu-id="bf6d4-119">Güncelleştirme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-119">The name of the update location.</span></span>

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

### <span data-ttu-id="bf6d4-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf6d4-120">-Name</span></span>
<span data-ttu-id="bf6d4-121">Çalışma tanımlayıcısını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-121">Update run identifier.</span></span>

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

### <span data-ttu-id="bf6d4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf6d4-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf6d4-123">Kaynağın altında bulunduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="bf6d4-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bf6d4-124">-ResourceId</span></span>
<span data-ttu-id="bf6d4-125">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-125">The resource id.</span></span>

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

### <span data-ttu-id="bf6d4-126">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="bf6d4-126">-UpdateName</span></span>
<span data-ttu-id="bf6d4-127">Güncelleştirmenin görünen adı.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-127">Display name of the update.</span></span>

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

### <span data-ttu-id="bf6d4-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf6d4-128">-Confirm</span></span>
<span data-ttu-id="bf6d4-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf6d4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf6d4-130">-WhatIf</span></span>
<span data-ttu-id="bf6d4-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf6d4-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf6d4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf6d4-133">CommonParameters</span></span>
<span data-ttu-id="bf6d4-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf6d4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf6d4-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf6d4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf6d4-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf6d4-136">INPUTS</span></span>

## <span data-ttu-id="bf6d4-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf6d4-137">OUTPUTS</span></span>

## <span data-ttu-id="bf6d4-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf6d4-138">NOTES</span></span>

## <span data-ttu-id="bf6d4-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf6d4-139">RELATED LINKS</span></span>

