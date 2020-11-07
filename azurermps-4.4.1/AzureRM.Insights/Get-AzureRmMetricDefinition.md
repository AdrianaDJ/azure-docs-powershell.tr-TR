---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: 4cb978b33b6bcb68d400f33fb2da06747ce9b763
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763729"
---
# <span data-ttu-id="e93a1-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="e93a1-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="e93a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e93a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e93a1-103">Metrik tanımları alır.</span><span class="sxs-lookup"><span data-stu-id="e93a1-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e93a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e93a1-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricNames <String[]>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e93a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e93a1-105">DESCRIPTION</span></span>
<span data-ttu-id="e93a1-106">**Get-AzureRmMetricDefinition** cmdlet 'i, metrik tanımları alır.</span><span class="sxs-lookup"><span data-stu-id="e93a1-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="e93a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e93a1-107">EXAMPLES</span></span>

### <span data-ttu-id="e93a1-108">Örnek 1: kaynağın metrik tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="e93a1-108">Example 1: Get metric definitions for a resource</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2"
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

<span data-ttu-id="e93a1-109">Bu komut, belirtilen kaynağın ölçüm tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e93a1-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="e93a1-110">Örnek 2: ayrıntılı çıktıyla metrik tanımları alma</span><span class="sxs-lookup"><span data-stu-id="e93a1-110">Example 2: Get metric definitions with detailed output</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput
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

<span data-ttu-id="e93a1-111">Bu komut, website2 için ölçüm tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e93a1-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="e93a1-112">Çıktı</span><span class="sxs-lookup"><span data-stu-id="e93a1-112">The output is detailed.</span></span>

### <span data-ttu-id="e93a1-113">Örnek 3: ad ile metrik tanımları alma</span><span class="sxs-lookup"><span data-stu-id="e93a1-113">Example 3: Get metric definitions by name</span></span>
```
PS C:\>Get-AzureRmMetricDefinition -ResourceId "/subscriptions/d33fb0c7-69d3-40be-e35b-4f0deba70fff/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/website2" -DetailedOutput -MetricNames "BytesSent,CpuTime"
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

<span data-ttu-id="e93a1-114">Bu komut, BytesSent ve CpuTime ölçümlerinin tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e93a1-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="e93a1-115">Çıktı</span><span class="sxs-lookup"><span data-stu-id="e93a1-115">The output is detailed.</span></span>

## <span data-ttu-id="e93a1-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e93a1-116">PARAMETERS</span></span>

### <span data-ttu-id="e93a1-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="e93a1-117">-DetailedOutput</span></span>
<span data-ttu-id="e93a1-118">Bu işlemin ayrıntılı çıktıya dahil olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e93a1-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="e93a1-119">Bu parametreyi belirtmezseniz, çıkış özetlenir.</span><span class="sxs-lookup"><span data-stu-id="e93a1-119">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93a1-120">-Metrik adları</span><span class="sxs-lookup"><span data-stu-id="e93a1-120">-MetricNames</span></span>
<span data-ttu-id="e93a1-121">Ölçüm adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93a1-121">Specifies an array of names of metrics.</span></span>

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

### <span data-ttu-id="e93a1-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e93a1-122">-ResourceId</span></span>
<span data-ttu-id="e93a1-123">Kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e93a1-123">Specifies the resource ID.</span></span>

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

### <span data-ttu-id="e93a1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93a1-124">-DefaultProfile</span></span>
<span data-ttu-id="e93a1-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e93a1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93a1-126">CommonParameters</span></span>
<span data-ttu-id="e93a1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e93a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93a1-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e93a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93a1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e93a1-129">INPUTS</span></span>

## <span data-ttu-id="e93a1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e93a1-130">OUTPUTS</span></span>

### <span data-ttu-id="e93a1-131">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition []</span><span class="sxs-lookup"><span data-stu-id="e93a1-131">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="e93a1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e93a1-132">NOTES</span></span>

## <span data-ttu-id="e93a1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e93a1-133">RELATED LINKS</span></span>

[<span data-ttu-id="e93a1-134">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="e93a1-134">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


