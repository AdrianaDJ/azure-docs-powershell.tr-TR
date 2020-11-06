---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594675"
---
# <span data-ttu-id="089ca-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="089ca-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="089ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="089ca-102">SYNOPSIS</span></span>
<span data-ttu-id="089ca-103">Bir WebTest uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="089ca-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="089ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="089ca-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="089ca-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="089ca-105">DESCRIPTION</span></span>
<span data-ttu-id="089ca-106">**Add-AzureRmWebtestAlertRule** cmdlet 'i, metrik, olay veya WebTest türünden bir uyarı kuralı ekler veya bu kuralı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="089ca-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="089ca-107">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="089ca-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="089ca-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="089ca-108">EXAMPLES</span></span>

### <span data-ttu-id="089ca-109">Örnek 1: WebTest uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="089ca-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="089ca-110">Bu komut bir WebTest uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="089ca-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="089ca-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="089ca-111">PARAMETERS</span></span>

### <span data-ttu-id="089ca-112">-Eylemler</span><span class="sxs-lookup"><span data-stu-id="089ca-112">-Actions</span></span>
<span data-ttu-id="089ca-113">Virgülle ayrılmış bir eylem listesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-113">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="089ca-114">-Description</span></span>
<span data-ttu-id="089ca-115">Kuralın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="089ca-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="089ca-116">-DisableRule</span></span>
<span data-ttu-id="089ca-117">Kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="089ca-117">Disables the rule.</span></span>
<span data-ttu-id="089ca-118">Bu parametreyi belirtmezseniz, kural etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="089ca-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="089ca-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="089ca-119">-FailedLocationCount</span></span>
<span data-ttu-id="089ca-120">WebTest kuralları için başarısız olan konum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="089ca-121">Bu, diğer kural türlerinde eşik ile benzerdir.</span><span class="sxs-lookup"><span data-stu-id="089ca-121">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="089ca-122">-Location</span></span>
<span data-ttu-id="089ca-123">Kuralın tanımlandığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-123">Specifies the location where the rule is defined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-124">-MetricName</span><span class="sxs-lookup"><span data-stu-id="089ca-124">-MetricName</span></span>
<span data-ttu-id="089ca-125">Ölçümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-125">Specifies the name of the metric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="089ca-126">-MetricNamespace</span></span>
<span data-ttu-id="089ca-127">Kural için ölçü ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="089ca-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="089ca-128">-Name</span></span>
<span data-ttu-id="089ca-129">Kuralın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-129">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="089ca-130">-ResourceGroup</span></span>
<span data-ttu-id="089ca-131">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-131">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="089ca-132">-TargetResourceUri</span></span>
<span data-ttu-id="089ca-133">WebTest 'in kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-133">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-134">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="089ca-134">-WindowSize</span></span>
<span data-ttu-id="089ca-135">Kuralın verilerinin hesaplanması için zaman penceresi boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="089ca-135">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="089ca-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089ca-136">-DefaultProfile</span></span>
<span data-ttu-id="089ca-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="089ca-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="089ca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089ca-138">CommonParameters</span></span>
<span data-ttu-id="089ca-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="089ca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089ca-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="089ca-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089ca-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="089ca-141">INPUTS</span></span>

## <span data-ttu-id="089ca-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="089ca-142">OUTPUTS</span></span>

### <span data-ttu-id="089ca-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="089ca-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="089ca-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="089ca-144">NOTES</span></span>

## <span data-ttu-id="089ca-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="089ca-145">RELATED LINKS</span></span>

[<span data-ttu-id="089ca-146">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="089ca-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="089ca-147">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="089ca-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="089ca-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="089ca-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="089ca-149">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="089ca-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


