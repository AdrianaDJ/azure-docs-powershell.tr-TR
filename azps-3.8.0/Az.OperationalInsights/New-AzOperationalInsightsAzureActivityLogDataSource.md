---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6dc016e717e89ad60e066be1c1d86e5871309d9e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096115"
---
# <span data-ttu-id="b146e-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="b146e-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="b146e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b146e-102">SYNOPSIS</span></span>
<span data-ttu-id="b146e-103">Verilen abonelikten Azure etkinlik günlüğü Collect.</span><span class="sxs-lookup"><span data-stu-id="b146e-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="b146e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b146e-104">SYNTAX</span></span>

### <span data-ttu-id="b146e-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b146e-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b146e-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="b146e-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b146e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b146e-107">DESCRIPTION</span></span>
<span data-ttu-id="b146e-108">Günlük çözümlemelerini verilen abonelikten Azure etkinlik günlüğünü toplamasını etkinleştirme New-AzOperationalInsightsAzureActivityLogDataSource.</span><span class="sxs-lookup"><span data-stu-id="b146e-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="b146e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b146e-109">EXAMPLES</span></span>

### <span data-ttu-id="b146e-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b146e-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b146e-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="b146e-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="b146e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b146e-112">PARAMETERS</span></span>

### <span data-ttu-id="b146e-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="b146e-113">-BackfillStartTime</span></span>
<span data-ttu-id="b146e-114">Günlükleri bir hafta önce doldurmayı tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b146e-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b146e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b146e-115">-DefaultProfile</span></span>
<span data-ttu-id="b146e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b146e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b146e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b146e-117">-Force</span></span>
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

### <span data-ttu-id="b146e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b146e-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b146e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b146e-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b146e-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b146e-120">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b146e-121">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="b146e-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b146e-122">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="b146e-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b146e-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="b146e-123">-Confirm</span></span>
<span data-ttu-id="b146e-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b146e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b146e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b146e-125">-WhatIf</span></span>
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

### <span data-ttu-id="b146e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b146e-126">CommonParameters</span></span>
<span data-ttu-id="b146e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b146e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b146e-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b146e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b146e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b146e-129">INPUTS</span></span>

### <span data-ttu-id="b146e-130">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b146e-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b146e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b146e-131">System.String</span></span>

### <span data-ttu-id="b146e-132">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b146e-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="b146e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b146e-133">OUTPUTS</span></span>

### <span data-ttu-id="b146e-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="b146e-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b146e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b146e-135">NOTES</span></span>

## <span data-ttu-id="b146e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b146e-136">RELATED LINKS</span></span>