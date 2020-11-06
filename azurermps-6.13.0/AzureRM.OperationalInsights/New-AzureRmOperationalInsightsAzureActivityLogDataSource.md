---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 654663e9fdc44270266aa2872b7deb939be93e83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589407"
---
# <span data-ttu-id="59fde-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="59fde-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="59fde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59fde-102">SYNOPSIS</span></span>
<span data-ttu-id="59fde-103">Verilen abonelikten Azure etkinlik günlüğü Collect.</span><span class="sxs-lookup"><span data-stu-id="59fde-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59fde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59fde-104">SYNTAX</span></span>

### <span data-ttu-id="59fde-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59fde-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59fde-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="59fde-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59fde-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="59fde-107">DESCRIPTION</span></span>
<span data-ttu-id="59fde-108">Günlük çözümlemelerini verilen abonelikten Azure etkinlik günlüğünü toplamasını etkinleştirme New-AzureRmOperationalInsightsAzureActivityLogDataSource.</span><span class="sxs-lookup"><span data-stu-id="59fde-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="59fde-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59fde-109">EXAMPLES</span></span>

### <span data-ttu-id="59fde-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="59fde-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="59fde-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="59fde-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="59fde-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59fde-112">PARAMETERS</span></span>

### <span data-ttu-id="59fde-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="59fde-113">-BackfillStartTime</span></span>
<span data-ttu-id="59fde-114">Günlükleri bir hafta önce doldurmayı tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="59fde-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="59fde-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fde-115">-DefaultProfile</span></span>
<span data-ttu-id="59fde-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="59fde-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59fde-117">-Force</span><span class="sxs-lookup"><span data-stu-id="59fde-117">-Force</span></span>
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

### <span data-ttu-id="59fde-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="59fde-118">-Name</span></span>
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

### <span data-ttu-id="59fde-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59fde-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="59fde-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="59fde-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="59fde-121">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="59fde-121">-Workspace</span></span>
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

### <span data-ttu-id="59fde-122">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="59fde-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="59fde-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="59fde-123">-Confirm</span></span>
<span data-ttu-id="59fde-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59fde-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59fde-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59fde-125">-WhatIf</span></span>
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

### <span data-ttu-id="59fde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fde-126">CommonParameters</span></span>
<span data-ttu-id="59fde-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59fde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fde-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59fde-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fde-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59fde-129">INPUTS</span></span>

### <span data-ttu-id="59fde-130">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="59fde-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="59fde-131">Parametreler: çalışma alanı (ByValue)</span><span class="sxs-lookup"><span data-stu-id="59fde-131">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="59fde-132">System. String</span><span class="sxs-lookup"><span data-stu-id="59fde-132">System.String</span></span>

### <span data-ttu-id="59fde-133">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59fde-133">System.DateTimeOffset</span></span>

## <span data-ttu-id="59fde-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59fde-134">OUTPUTS</span></span>

### <span data-ttu-id="59fde-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="59fde-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="59fde-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59fde-136">NOTES</span></span>

## <span data-ttu-id="59fde-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59fde-137">RELATED LINKS</span></span>
