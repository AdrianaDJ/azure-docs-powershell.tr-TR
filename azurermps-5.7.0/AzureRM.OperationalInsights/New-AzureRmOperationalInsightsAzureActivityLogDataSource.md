---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 6b3009a37a314b70d258f597823f8da062970450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588137"
---
# <span data-ttu-id="fec80-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="fec80-101">New-AzureRmOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="fec80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec80-102">SYNOPSIS</span></span>
<span data-ttu-id="fec80-103">Verilen abonelikten Azure etkinlik günlüğü Collect.</span><span class="sxs-lookup"><span data-stu-id="fec80-103">Collect Azure Activity log from given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fec80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fec80-104">SYNTAX</span></span>

### <span data-ttu-id="fec80-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fec80-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fec80-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="fec80-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fec80-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fec80-107">DESCRIPTION</span></span>
<span data-ttu-id="fec80-108">Günlük çözümlemelerini verilen abonelikten Azure etkinlik günlüğünü toplamasını etkinleştirme New-AzureRmOperationalInsightsAzureActivityLogDataSource.</span><span class="sxs-lookup"><span data-stu-id="fec80-108">The New-AzureRmOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="fec80-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fec80-109">EXAMPLES</span></span>

### <span data-ttu-id="fec80-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fec80-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="fec80-111">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="fec80-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="fec80-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fec80-112">PARAMETERS</span></span>

### <span data-ttu-id="fec80-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="fec80-113">-BackfillStartTime</span></span>
<span data-ttu-id="fec80-114">Günlükleri bir hafta önce doldurmayı tercih edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fec80-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec80-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec80-115">-DefaultProfile</span></span>
<span data-ttu-id="fec80-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fec80-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec80-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fec80-117">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec80-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fec80-118">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec80-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fec80-119">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec80-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="fec80-120">-SubscriptionId</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec80-121">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="fec80-121">-Workspace</span></span>
```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fec80-122">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="fec80-122">-WorkspaceName</span></span>
```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec80-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="fec80-123">-Confirm</span></span>
<span data-ttu-id="fec80-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fec80-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec80-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec80-125">-WhatIf</span></span>
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

### <span data-ttu-id="fec80-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec80-126">CommonParameters</span></span>
<span data-ttu-id="fec80-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fec80-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec80-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec80-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec80-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fec80-129">INPUTS</span></span>

### <span data-ttu-id="fec80-130">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="fec80-130">PSWorkspace</span></span>
<span data-ttu-id="fec80-131">Parametre ' çalışma alanı ', ardışık düzenin ' PSWorkspace ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="fec80-131">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="fec80-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fec80-132">OUTPUTS</span></span>

### <span data-ttu-id="fec80-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDAtakaynağı</span><span class="sxs-lookup"><span data-stu-id="fec80-133">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="fec80-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fec80-134">NOTES</span></span>

## <span data-ttu-id="fec80-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fec80-135">RELATED LINKS</span></span>

