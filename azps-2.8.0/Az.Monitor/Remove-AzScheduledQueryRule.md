---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ebbbe7376499ba1fd72a207754bd7ea74c2d7c3a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932156"
---
# <span data-ttu-id="83f72-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="83f72-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="83f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83f72-102">SYNOPSIS</span></span>
<span data-ttu-id="83f72-103">Günlük uyarısı kuralını kaldırır</span><span class="sxs-lookup"><span data-stu-id="83f72-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="83f72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83f72-104">SYNTAX</span></span>

### <span data-ttu-id="83f72-105">ByRuleName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83f72-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f72-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83f72-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f72-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="83f72-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f72-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="83f72-108">DESCRIPTION</span></span>
<span data-ttu-id="83f72-109">Günlük uyarısı kuralını kaldırır</span><span class="sxs-lookup"><span data-stu-id="83f72-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="83f72-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83f72-110">EXAMPLES</span></span>

### <span data-ttu-id="83f72-111">Örnek 1-kural adına göre kaldır</span><span class="sxs-lookup"><span data-stu-id="83f72-111">Example 1 - Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="83f72-112">Örnek 2-giriş nesnesine göre kaldır</span><span class="sxs-lookup"><span data-stu-id="83f72-112">Example 2 - Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="83f72-113">Örnek 3-kaynak kimliğiyle kaldır</span><span class="sxs-lookup"><span data-stu-id="83f72-113">Example 3 - Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="83f72-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83f72-114">PARAMETERS</span></span>

### <span data-ttu-id="83f72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f72-115">-DefaultProfile</span></span>
<span data-ttu-id="83f72-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83f72-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f72-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83f72-117">-InputObject</span></span>
<span data-ttu-id="83f72-118">Zamanlanmış sorgu kuralı kaynağı</span><span class="sxs-lookup"><span data-stu-id="83f72-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83f72-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="83f72-119">-Name</span></span>
<span data-ttu-id="83f72-120">Uyarı adı</span><span class="sxs-lookup"><span data-stu-id="83f72-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f72-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="83f72-121">-PassThru</span></span>
<span data-ttu-id="83f72-122">Başarı veya başarısızlığı belirten bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="83f72-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="83f72-123">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="83f72-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="83f72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f72-124">-ResourceGroupName</span></span>
<span data-ttu-id="83f72-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="83f72-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f72-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="83f72-126">-ResourceId</span></span>
<span data-ttu-id="83f72-127">Kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="83f72-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f72-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="83f72-128">-Confirm</span></span>
<span data-ttu-id="83f72-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83f72-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f72-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f72-130">-WhatIf</span></span>
<span data-ttu-id="83f72-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83f72-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f72-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83f72-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f72-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f72-133">CommonParameters</span></span>
<span data-ttu-id="83f72-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83f72-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f72-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="83f72-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f72-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83f72-136">INPUTS</span></span>

### <span data-ttu-id="83f72-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="83f72-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="83f72-138">System. String</span><span class="sxs-lookup"><span data-stu-id="83f72-138">System.String</span></span>

## <span data-ttu-id="83f72-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83f72-139">OUTPUTS</span></span>

### <span data-ttu-id="83f72-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83f72-140">System.Boolean</span></span>

## <span data-ttu-id="83f72-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83f72-141">NOTES</span></span>

## <span data-ttu-id="83f72-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83f72-142">RELATED LINKS</span></span>
