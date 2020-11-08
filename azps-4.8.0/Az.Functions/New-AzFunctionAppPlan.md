---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267703"
---
# <span data-ttu-id="a1b71-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a1b71-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a1b71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1b71-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b71-103">Function App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1b71-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="a1b71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1b71-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1b71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1b71-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b71-106">Function App Service planı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a1b71-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="a1b71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1b71-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b71-108">Örnek 1: Batı Avrupa 'da bir Windows Premium App planı oluşturma</span><span class="sxs-lookup"><span data-stu-id="a1b71-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="a1b71-109">Bu komut, Batı Avrupa 'da bir Windows Premium App planı oluşturur ve en fazla 10 örneği</span><span class="sxs-lookup"><span data-stu-id="a1b71-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="a1b71-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1b71-110">PARAMETERS</span></span>

### <span data-ttu-id="a1b71-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="a1b71-111">-AsJob</span></span>
<span data-ttu-id="a1b71-112">Komutu iş olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a1b71-112">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b71-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-114">-Konum</span><span class="sxs-lookup"><span data-stu-id="a1b71-114">-Location</span></span>
<span data-ttu-id="a1b71-115">Tüketim planının konumu.</span><span class="sxs-lookup"><span data-stu-id="a1b71-115">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a1b71-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="a1b71-117">App Service planı için en fazla çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="a1b71-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a1b71-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="a1b71-119">App Service planı için en az çalışan sayısı.</span><span class="sxs-lookup"><span data-stu-id="a1b71-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1b71-120">-Name</span></span>
<span data-ttu-id="a1b71-121">App Service planının adı.</span><span class="sxs-lookup"><span data-stu-id="a1b71-121">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a1b71-122">-NoWait</span></span>
<span data-ttu-id="a1b71-123">Komutu zaman uyumsuz olarak çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="a1b71-123">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b71-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1b71-125">Kaynağın ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a1b71-125">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="a1b71-126">-Sku</span></span>
<span data-ttu-id="a1b71-127">Plan SKU 'su.</span><span class="sxs-lookup"><span data-stu-id="a1b71-127">The plan sku.</span></span>
<span data-ttu-id="a1b71-128">Geçerli girdiler: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="a1b71-128">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a1b71-129">-SubscriptionId</span></span>
<span data-ttu-id="a1b71-130">Azure aboneliği KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a1b71-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a1b71-131">-Tag</span></span>
<span data-ttu-id="a1b71-132">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="a1b71-132">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="a1b71-133">-WorkerType</span></span>
<span data-ttu-id="a1b71-134">Planın çalışan türü.</span><span class="sxs-lookup"><span data-stu-id="a1b71-134">The worker type for the plan.</span></span>
<span data-ttu-id="a1b71-135">Geçerli girdiler: Windows veya Linux.</span><span class="sxs-lookup"><span data-stu-id="a1b71-135">Valid inputs are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1b71-136">-Confirm</span></span>
<span data-ttu-id="a1b71-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1b71-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1b71-138">-WhatIf</span></span>
<span data-ttu-id="a1b71-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1b71-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1b71-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1b71-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1b71-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b71-141">CommonParameters</span></span>
<span data-ttu-id="a1b71-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1b71-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b71-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a1b71-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b71-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1b71-144">INPUTS</span></span>

## <span data-ttu-id="a1b71-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1b71-145">OUTPUTS</span></span>

### <span data-ttu-id="a1b71-146">Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ıappserviceplan</span><span class="sxs-lookup"><span data-stu-id="a1b71-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a1b71-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1b71-147">NOTES</span></span>

<span data-ttu-id="a1b71-148">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a1b71-148">ALIASES</span></span>

## <span data-ttu-id="a1b71-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1b71-149">RELATED LINKS</span></span>

