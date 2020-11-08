---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/measure-azalertstatistic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Measure-AzAlertStatistic.md
ms.openlocfilehash: 96b83f6792babed9fed7c39cad44aec0ea0f26ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109278"
---
# <span data-ttu-id="e02e3-101">Measure-AzAlertStatistic</span><span class="sxs-lookup"><span data-stu-id="e02e3-101">Measure-AzAlertStatistic</span></span>

## <span data-ttu-id="e02e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e02e3-102">SYNOPSIS</span></span>
<span data-ttu-id="e02e3-103">Uyarı Özeti bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="e02e3-103">Gets Alert Summary Information</span></span>

## <span data-ttu-id="e02e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e02e3-104">SYNTAX</span></span>

### <span data-ttu-id="e02e3-105">Summarytargetresourceıdfilter</span><span class="sxs-lookup"><span data-stu-id="e02e3-105">SummaryTargetResourceIdFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceId <String>] [-MonitorService <String>]
 [-MonitorCondition <String>] [-Severity <String>] [-State <String>] [-AlertRuleId <String>]
 [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02e3-106">SummaryFilter</span><span class="sxs-lookup"><span data-stu-id="e02e3-106">SummaryFilter</span></span>
```
Measure-AzAlertStatistic -GroupBy <String> [-TargetResourceType <String>] [-TargetResourceGroup <String>]
 [-MonitorService <String>] [-MonitorCondition <String>] [-Severity <String>] [-State <String>]
 [-AlertRuleId <String>] [-TimeRange <String>] [-CustomTimeRange <String>] [-IncludeSmartGroupsCount <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e02e3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e02e3-107">DESCRIPTION</span></span>
<span data-ttu-id="e02e3-108">**Measure-Azalertistatistiğini** cmdlet, uyarı Özeti ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e02e3-108">**Measure-AzAlertStatistic** cmdlet gets alert summary details.</span></span>

## <span data-ttu-id="e02e3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e02e3-109">EXAMPLES</span></span>

### <span data-ttu-id="e02e3-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e02e3-110">Example 1</span></span>
```powershell
PS C:\> Measure-AzAlertStatistic -GroupBy "severity,alertstate" -State "Active"
```

<span data-ttu-id="e02e3-111">Durumları, etkin duruma göre filtrelenmiş önem derecesine ve duruma göre gruplandırılmış olarak gruplandırılmış uyarılar.</span><span class="sxs-lookup"><span data-stu-id="e02e3-111">Summarize alerts count grouped by severity and state filtered by Active state.</span></span>

## <span data-ttu-id="e02e3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e02e3-112">PARAMETERS</span></span>

### <span data-ttu-id="e02e3-113">-Alertruleıd</span><span class="sxs-lookup"><span data-stu-id="e02e3-113">-AlertRuleId</span></span>
<span data-ttu-id="e02e3-114">Uyarı kuralı kimliği</span><span class="sxs-lookup"><span data-stu-id="e02e3-114">Filter on Alert Rule Id</span></span>

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

### <span data-ttu-id="e02e3-115">-CustomTimeRange</span><span class="sxs-lookup"><span data-stu-id="e02e3-115">-CustomTimeRange</span></span>
<span data-ttu-id="e02e3-116">Desteklenen biçim- \<start-time\> / \<end-time\> saat, ISO-8601 biçimindedir</span><span class="sxs-lookup"><span data-stu-id="e02e3-116">Supported format - \<start-time\>/\<end-time\> where time is in ISO-8601 format</span></span>

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

### <span data-ttu-id="e02e3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02e3-117">-DefaultProfile</span></span>
<span data-ttu-id="e02e3-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e02e3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02e3-119">-GroupBy</span><span class="sxs-lookup"><span data-stu-id="e02e3-119">-GroupBy</span></span>
<span data-ttu-id="e02e3-120">Özelliğe göre özetleme</span><span class="sxs-lookup"><span data-stu-id="e02e3-120">Summarize by property</span></span>

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

### <span data-ttu-id="e02e3-121">-Includesmartgroupscount</span><span class="sxs-lookup"><span data-stu-id="e02e3-121">-IncludeSmartGroupsCount</span></span>
<span data-ttu-id="e02e3-122">SmartGroups sayısını içer</span><span class="sxs-lookup"><span data-stu-id="e02e3-122">Include SmartGroups Count</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02e3-123">-MonitorCondition</span><span class="sxs-lookup"><span data-stu-id="e02e3-123">-MonitorCondition</span></span>
<span data-ttu-id="e02e3-124">Monitörde filtre koşulu</span><span class="sxs-lookup"><span data-stu-id="e02e3-124">Filter on Monitor Condition</span></span>

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

### <span data-ttu-id="e02e3-125">-MonitorService</span><span class="sxs-lookup"><span data-stu-id="e02e3-125">-MonitorService</span></span>
<span data-ttu-id="e02e3-126">Monitorın hizmetine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="e02e3-126">Filter on Moniter Service</span></span>

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

### <span data-ttu-id="e02e3-127">-Önem derecesi</span><span class="sxs-lookup"><span data-stu-id="e02e3-127">-Severity</span></span>
<span data-ttu-id="e02e3-128">Uyarının önem derecesine filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="e02e3-128">Filter on Severity of alert</span></span>

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

### <span data-ttu-id="e02e3-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="e02e3-129">-State</span></span>
<span data-ttu-id="e02e3-130">Uyarının durumuna filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="e02e3-130">Filter on State of alert</span></span>

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

### <span data-ttu-id="e02e3-131">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e02e3-131">-TargetResourceGroup</span></span>
<span data-ttu-id="e02e3-132">Uyarının hedef kaynağının kaynak grubu adına filtre uygulama.</span><span class="sxs-lookup"><span data-stu-id="e02e3-132">Filter on Resource group name of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02e3-133">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="e02e3-133">-TargetResourceId</span></span>
<span data-ttu-id="e02e3-134">Uyarının hedef kaynağının kaynak kimliği 'ne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="e02e3-134">Filter on Resource Id of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryTargetResourceIdFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02e3-135">-TargetResourceType</span><span class="sxs-lookup"><span data-stu-id="e02e3-135">-TargetResourceType</span></span>
<span data-ttu-id="e02e3-136">Hedef uyarının kaynak türüne filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="e02e3-136">Filter on Resource type of the target resource of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SummaryFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02e3-137">-TimeRange</span><span class="sxs-lookup"><span data-stu-id="e02e3-137">-TimeRange</span></span>
<span data-ttu-id="e02e3-138">Desteklenen zaman aralığı değerleri-1h, 1G, 7d, 30D (varsayılan olarak 1G)</span><span class="sxs-lookup"><span data-stu-id="e02e3-138">Supported time range values - 1h, 1d, 7d, 30d (Default is 1d)</span></span>

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

### <span data-ttu-id="e02e3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02e3-139">CommonParameters</span></span>
<span data-ttu-id="e02e3-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e02e3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02e3-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e02e3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02e3-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e02e3-142">INPUTS</span></span>

### <span data-ttu-id="e02e3-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e02e3-143">None</span></span>

## <span data-ttu-id="e02e3-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e02e3-144">OUTPUTS</span></span>

### <span data-ttu-id="e02e3-145">Microsoft. Azure. Commands. AlertsManagement. Outputmodel. Psalcertssummary</span><span class="sxs-lookup"><span data-stu-id="e02e3-145">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertsSummary</span></span>

## <span data-ttu-id="e02e3-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e02e3-146">NOTES</span></span>

## <span data-ttu-id="e02e3-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e02e3-147">RELATED LINKS</span></span>
