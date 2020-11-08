---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzMetricDefinition.md
ms.openlocfilehash: 9ca873736ad86eaac17dd2795ad61716197ceaba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109001"
---
# <span data-ttu-id="4f727-101">Get-AzMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="4f727-101">Get-AzMetricDefinition</span></span>

## <span data-ttu-id="4f727-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f727-102">SYNOPSIS</span></span>
<span data-ttu-id="4f727-103">Metrik tanımları alır.</span><span class="sxs-lookup"><span data-stu-id="4f727-103">Gets metric definitions.</span></span>

## <span data-ttu-id="4f727-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f727-104">SYNTAX</span></span>

```
Get-AzMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-MetricNamespace <String>]
 [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f727-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f727-105">DESCRIPTION</span></span>
<span data-ttu-id="4f727-106">**Get-AzMetricDefinition** cmdlet 'i, metrik tanımları alır.</span><span class="sxs-lookup"><span data-stu-id="4f727-106">The **Get-AzMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="4f727-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f727-107">EXAMPLES</span></span>

### <span data-ttu-id="4f727-108">Örnek 1: kaynağın metrik tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="4f727-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
Name                   : CpuTime
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Seconds
Name                   : Requests
Dimensions             : {}
MetricAvailabilities   : {Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability, 
                         Microsoft.Azure.Insights.Models.MetricAvailability}
PrimaryAggregationType : Total
Properties             : {}
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="4f727-109">Bu komut, belirtilen kaynağın ölçüm tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f727-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="4f727-110">Örnek 2: ayrıntılı çıktıyla metrik tanımları alma</span><span class="sxs-lookup"><span data-stu-id="4f727-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : Requests
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Count
```

<span data-ttu-id="4f727-111">Bu komut, website2 için ölçüm tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f727-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="4f727-112">Çıktı</span><span class="sxs-lookup"><span data-stu-id="4f727-112">The output is detailed.</span></span>

### <span data-ttu-id="4f727-113">Örnek 3: ad ile metrik tanımları alma</span><span class="sxs-lookup"><span data-stu-id="4f727-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricName "BytesSent,CpuTime"
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : CpuTime
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Seconds
Dimensions             : 
MetricAvailabilities   : 
                             Location  : 
                             Retention : 2.00:00:00
                             Values    : 00:01:00
                             Location  : 
                             Retention : 30.00:00:00
                             Values    : 01:00:00
                             Location  : 
                             Retention : 90.00:00:00
                             Values    : 1.00:00:00
Name                   : BytesSent
Properties             : 
PrimaryAggregationType : Total
ResourceUri            : 
Unit                   : Bytes
```

<span data-ttu-id="4f727-114">Bu komut, BytesSent ve CpuTime ölçümlerinin tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4f727-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="4f727-115">Çıktı</span><span class="sxs-lookup"><span data-stu-id="4f727-115">The output is detailed.</span></span>

## <span data-ttu-id="4f727-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f727-116">PARAMETERS</span></span>

### <span data-ttu-id="4f727-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f727-117">-DefaultProfile</span></span>
<span data-ttu-id="4f727-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4f727-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f727-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="4f727-119">-DetailedOutput</span></span>
<span data-ttu-id="4f727-120">Bu işlemin ayrıntılı çıktıya dahil olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f727-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="4f727-121">Bu parametreyi belirtmezseniz, çıkış özetlenir.</span><span class="sxs-lookup"><span data-stu-id="4f727-121">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="4f727-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="4f727-122">-MetricName</span></span>
<span data-ttu-id="4f727-123">Ölçüm adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f727-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f727-124">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="4f727-124">-MetricNamespace</span></span>
<span data-ttu-id="4f727-125">Ölçüm tanımlarının sorgu olarak kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f727-125">Specifies the metric namespace to query metric definitions for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f727-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4f727-126">-ResourceId</span></span>
<span data-ttu-id="4f727-127">Kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4f727-127">Specifies the resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f727-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f727-128">CommonParameters</span></span>
<span data-ttu-id="4f727-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4f727-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f727-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4f727-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f727-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f727-131">INPUTS</span></span>

### <span data-ttu-id="4f727-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4f727-132">System.String</span></span>

### <span data-ttu-id="4f727-133">System. String []</span><span class="sxs-lookup"><span data-stu-id="4f727-133">System.String[]</span></span>

## <span data-ttu-id="4f727-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f727-134">OUTPUTS</span></span>

### <span data-ttu-id="4f727-135">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="4f727-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition</span></span>

## <span data-ttu-id="4f727-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f727-136">NOTES</span></span>

<span data-ttu-id="4f727-137">Desteklenen ölçümler hakkında daha fazla bilgiyi şu adreste bulabilirsiniz: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span><span class="sxs-lookup"><span data-stu-id="4f727-137">More information about the supported metrics may be found at: https://docs.microsoft.com/en-us/azure/azure-monitor/platform/metrics-supported</span></span>

## <span data-ttu-id="4f727-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f727-138">RELATED LINKS</span></span>

<span data-ttu-id="4f727-139">[Get-Azmetrik](./Get-AzMetric.md) 
 [New-Azmetrik Icfilter](./New-AzMetricFilter.md)</span><span class="sxs-lookup"><span data-stu-id="4f727-139">[Get-AzMetric](./Get-AzMetric.md)
[New-AzMetricFilter](./New-AzMetricFilter.md)</span></span>


