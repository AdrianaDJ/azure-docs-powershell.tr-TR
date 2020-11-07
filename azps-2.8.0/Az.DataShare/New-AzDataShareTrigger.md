---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: f7342ec33e712407987da28b232670d56bdcab66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752176"
---
# <span data-ttu-id="df9c9-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="df9c9-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="df9c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="df9c9-103">Paylaşım aboneliği için tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df9c9-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="df9c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df9c9-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="df9c9-106">**New-AzDataShareTrigger** cmdlet 'i, Azure veri paylaşımı hesabı altında belirtilen yinelenme aralığı ve eşitleme süresi için paylaşım aboneliği için bir tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df9c9-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="df9c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df9c9-107">EXAMPLES</span></span>

### <span data-ttu-id="df9c9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="df9c9-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="df9c9-109">Bu komut, paylaşım aboneliği Adsshar, 9 ' un günlük yinelenme aralığına sahip Share aboneliği için yeni bir tetik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="df9c9-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="df9c9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df9c9-110">PARAMETERS</span></span>

### <span data-ttu-id="df9c9-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="df9c9-111">-AccountName</span></span>
<span data-ttu-id="df9c9-112">Azure veri paylaşımı hesap adı</span><span class="sxs-lookup"><span data-stu-id="df9c9-112">Azure data share account name</span></span>

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

### <span data-ttu-id="df9c9-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="df9c9-113">-AsJob</span></span>
<span data-ttu-id="df9c9-114">{{Fill Iş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="df9c9-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="df9c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9c9-115">-DefaultProfile</span></span>
<span data-ttu-id="df9c9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df9c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df9c9-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="df9c9-117">-Name</span></span>
<span data-ttu-id="df9c9-118">Azure veri paylaşımı tetik adı</span><span class="sxs-lookup"><span data-stu-id="df9c9-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="df9c9-119">-Recurrenceınterval</span><span class="sxs-lookup"><span data-stu-id="df9c9-119">-RecurrenceInterval</span></span>
<span data-ttu-id="df9c9-120">Tetikleyicinin yineleme aralığı (gün veya saat)</span><span class="sxs-lookup"><span data-stu-id="df9c9-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="df9c9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9c9-121">-ResourceGroupName</span></span>
<span data-ttu-id="df9c9-122">Azure veri paylaşımı hesabının kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="df9c9-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="df9c9-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="df9c9-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="df9c9-124">Azure veri paylaşımı abonelik adı</span><span class="sxs-lookup"><span data-stu-id="df9c9-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9c9-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="df9c9-125">-SynchronizationTime</span></span>
<span data-ttu-id="df9c9-126">Tetik için zamanlanmış eşitlemenin başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="df9c9-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9c9-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="df9c9-127">-Confirm</span></span>
<span data-ttu-id="df9c9-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df9c9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9c9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9c9-129">-WhatIf</span></span>
<span data-ttu-id="df9c9-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df9c9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9c9-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df9c9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9c9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9c9-132">CommonParameters</span></span>
<span data-ttu-id="df9c9-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df9c9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9c9-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df9c9-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9c9-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df9c9-135">INPUTS</span></span>

### <span data-ttu-id="df9c9-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="df9c9-136">None</span></span>

## <span data-ttu-id="df9c9-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df9c9-137">OUTPUTS</span></span>

### <span data-ttu-id="df9c9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDAtapaylaşıdavetiyesi</span><span class="sxs-lookup"><span data-stu-id="df9c9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="df9c9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df9c9-139">NOTES</span></span>

## <span data-ttu-id="df9c9-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df9c9-140">RELATED LINKS</span></span>
