---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7915A7AC-5A47-4868-B846-2896BCEBFAB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermmetricdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmMetricDefinition.md
ms.openlocfilehash: de839f4b56f4aa1111e130bdf6396875f9aeb185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590484"
---
# <span data-ttu-id="b3c7c-101">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b3c7c-101">Get-AzureRmMetricDefinition</span></span>

## <span data-ttu-id="b3c7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c7c-103">Metrik tanımları alır.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-103">Gets metric definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3c7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3c7c-104">SYNTAX</span></span>

```
Get-AzureRmMetricDefinition [-ResourceId] <String> [-MetricName <String[]>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3c7c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3c7c-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c7c-106">**Get-AzureRmMetricDefinition** cmdlet 'i, metrik tanımları alır.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-106">The **Get-AzureRmMetricDefinition** cmdlet gets metric definitions.</span></span>

## <span data-ttu-id="b3c7c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3c7c-107">EXAMPLES</span></span>

### <span data-ttu-id="b3c7c-108">Örnek 1: kaynağın metrik tanımlarını alma</span><span class="sxs-lookup"><span data-stu-id="b3c7c-108">Example 1: Get metric definitions for a resource</span></span>
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

<span data-ttu-id="b3c7c-109">Bu komut, belirtilen kaynağın ölçüm tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-109">This command gets the metrics definitions for the specified resource.</span></span>

### <span data-ttu-id="b3c7c-110">Örnek 2: ayrıntılı çıktıyla metrik tanımları alma</span><span class="sxs-lookup"><span data-stu-id="b3c7c-110">Example 2: Get metric definitions with detailed output</span></span>
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

<span data-ttu-id="b3c7c-111">Bu komut, website2 için ölçüm tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-111">This command gets the metric definitions for website2.</span></span>
<span data-ttu-id="b3c7c-112">Çıktı</span><span class="sxs-lookup"><span data-stu-id="b3c7c-112">The output is detailed.</span></span>

### <span data-ttu-id="b3c7c-113">Örnek 3: ad ile metrik tanımları alma</span><span class="sxs-lookup"><span data-stu-id="b3c7c-113">Example 3: Get metric definitions by name</span></span>
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

<span data-ttu-id="b3c7c-114">Bu komut, BytesSent ve CpuTime ölçümlerinin tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-114">This command gets definitions for the BytesSent and CpuTime metrics.</span></span>
<span data-ttu-id="b3c7c-115">Çıktı</span><span class="sxs-lookup"><span data-stu-id="b3c7c-115">The output is detailed.</span></span>

## <span data-ttu-id="b3c7c-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3c7c-116">PARAMETERS</span></span>

### <span data-ttu-id="b3c7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c7c-117">-DefaultProfile</span></span>
<span data-ttu-id="b3c7c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3c7c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3c7c-119">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b3c7c-119">-DetailedOutput</span></span>
<span data-ttu-id="b3c7c-120">Bu işlemin ayrıntılı çıktıya dahil olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-120">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="b3c7c-121">Bu parametreyi belirtmezseniz, çıkış özetlenir.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-121">If you do not specify this parameter, the output is summarized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c7c-122">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b3c7c-122">-MetricName</span></span>
<span data-ttu-id="b3c7c-123">Ölçüm adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-123">Specifies an array of names of metrics.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: MetricNames

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c7c-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b3c7c-124">-ResourceId</span></span>
<span data-ttu-id="b3c7c-125">Kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-125">Specifies the resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c7c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c7c-126">CommonParameters</span></span>
<span data-ttu-id="b3c7c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c7c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3c7c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c7c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3c7c-129">INPUTS</span></span>

### <span data-ttu-id="b3c7c-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b3c7c-130">None</span></span>
<span data-ttu-id="b3c7c-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b3c7c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b3c7c-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3c7c-132">OUTPUTS</span></span>

### <span data-ttu-id="b3c7c-133">Microsoft. Azure. Commands. Insights. OutputClasses. PSMetricDefinition []</span><span class="sxs-lookup"><span data-stu-id="b3c7c-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSMetricDefinition[]</span></span>

## <span data-ttu-id="b3c7c-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3c7c-134">NOTES</span></span>

## <span data-ttu-id="b3c7c-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3c7c-135">RELATED LINKS</span></span>

[<span data-ttu-id="b3c7c-136">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="b3c7c-136">Get-AzureRmMetric</span></span>](./Get-AzureRmMetric.md)


