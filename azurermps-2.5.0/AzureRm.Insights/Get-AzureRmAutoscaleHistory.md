---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalehistory
schema: 2.0.0
ms.openlocfilehash: c149cf0d44bfe5fdeee953d36a7ea8244587ba36
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938880"
---
# <span data-ttu-id="e017f-101">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="e017f-101">Get-AzureRmAutoscaleHistory</span></span>

## <span data-ttu-id="e017f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e017f-102">SYNOPSIS</span></span>
<span data-ttu-id="e017f-103">Otomatik ölçeklendirme geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="e017f-103">Gets the Autoscale history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e017f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e017f-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Status <String>] [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e017f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e017f-105">DESCRIPTION</span></span>
<span data-ttu-id="e017f-106">**Get-AzureRmAutoscaleHistory** cmdlet 'ı otomatik ölçeklendirme ayarıyla ilgili olayların geçmişini alır.</span><span class="sxs-lookup"><span data-stu-id="e017f-106">The **Get-AzureRmAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="e017f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e017f-107">EXAMPLES</span></span>

### <span data-ttu-id="e017f-108">Örnek 1: abonelikle ilişkilendirilmiş tüm etkinlikleri alma</span><span class="sxs-lookup"><span data-stu-id="e017f-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="e017f-109">Bu komut, geçerli abonelikle ilişkili otomatik ölçeklendirme ile ilgili etkinlikleri alır.</span><span class="sxs-lookup"><span data-stu-id="e017f-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="e017f-110">Örnek 2: belirli bir kaynak için GetAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="e017f-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="e017f-111">Bu komut, kaynağın KIMLIĞI (Aslýnda, ResourceUri) tarafından tanımlanan belirli bir kaynakla ilişkili, otomatik ölçeklendirme ile ilgili tüm etkinlikleri alır.</span><span class="sxs-lookup"><span data-stu-id="e017f-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="e017f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e017f-112">PARAMETERS</span></span>

### <span data-ttu-id="e017f-113">Arayan</span><span class="sxs-lookup"><span data-stu-id="e017f-113">-Caller</span></span>
<span data-ttu-id="e017f-114">Arayan belirtir.</span><span class="sxs-lookup"><span data-stu-id="e017f-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="e017f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e017f-115">-DefaultProfile</span></span>
<span data-ttu-id="e017f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e017f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e017f-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="e017f-117">-DetailedOutput</span></span>
<span data-ttu-id="e017f-118">Bu işlemin ayrıntılı çıktıya dahil olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e017f-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="e017f-119">Bu parametreyi belirtmezseniz, çıkış özetlenir.</span><span class="sxs-lookup"><span data-stu-id="e017f-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="e017f-120">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="e017f-120">-EndTime</span></span>
<span data-ttu-id="e017f-121">Yerel saatte sorgunun bitiş saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e017f-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="e017f-122">Varsayılan geçerli saat.</span><span class="sxs-lookup"><span data-stu-id="e017f-122">The default is the current time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e017f-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e017f-123">-ResourceId</span></span>
<span data-ttu-id="e017f-124">Otomatik ölçeklendirme ayarının ilişkilendirildiği kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e017f-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="e017f-125">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="e017f-125">-StartTime</span></span>
<span data-ttu-id="e017f-126">Sorgunun başlangıç saatini yerel saatte belirtir.</span><span class="sxs-lookup"><span data-stu-id="e017f-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="e017f-127">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e017f-127">This parameter is optional.</span></span>
<span data-ttu-id="e017f-128">Varsayılan, geçerli yerel saatin bir saattir.</span><span class="sxs-lookup"><span data-stu-id="e017f-128">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e017f-129">-Durum</span><span class="sxs-lookup"><span data-stu-id="e017f-129">-Status</span></span>
<span data-ttu-id="e017f-130">Duruma göre filtreleme belirtir.</span><span class="sxs-lookup"><span data-stu-id="e017f-130">Specifies a filter by status.</span></span>
<span data-ttu-id="e017f-131">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e017f-131">This parameter is optional.</span></span>
<span data-ttu-id="e017f-132">Hata, boş bir dizedir (filtre yok)</span><span class="sxs-lookup"><span data-stu-id="e017f-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="e017f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e017f-133">CommonParameters</span></span>
<span data-ttu-id="e017f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e017f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e017f-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e017f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e017f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e017f-136">INPUTS</span></span>

### <span data-ttu-id="e017f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e017f-137">System.String</span></span>

### <span data-ttu-id="e017f-138">System. Nullable ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e017f-138">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e017f-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e017f-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e017f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e017f-140">OUTPUTS</span></span>

### <span data-ttu-id="e017f-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData</span><span class="sxs-lookup"><span data-stu-id="e017f-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="e017f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e017f-142">NOTES</span></span>

## <span data-ttu-id="e017f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e017f-143">RELATED LINKS</span></span>

[<span data-ttu-id="e017f-144">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e017f-144">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="e017f-145">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e017f-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="e017f-146">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e017f-146">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


