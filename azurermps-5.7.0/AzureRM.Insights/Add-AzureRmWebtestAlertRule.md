---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589773"
---
# <span data-ttu-id="d820a-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d820a-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="d820a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d820a-102">SYNOPSIS</span></span>
<span data-ttu-id="d820a-103">Bir WebTest uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d820a-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d820a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d820a-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d820a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d820a-105">DESCRIPTION</span></span>
<span data-ttu-id="d820a-106">**Add-AzureRmWebtestAlertRule** cmdlet 'i, metrik, olay veya WebTest türünden bir uyarı kuralı ekler veya bu kuralı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d820a-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="d820a-107">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="d820a-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="d820a-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="d820a-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d820a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d820a-109">EXAMPLES</span></span>

### <span data-ttu-id="d820a-110">Örnek 1: WebTest uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="d820a-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="d820a-111">Bu komut bir WebTest uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d820a-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="d820a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d820a-112">PARAMETERS</span></span>

### <span data-ttu-id="d820a-113">-Eylem</span><span class="sxs-lookup"><span data-stu-id="d820a-113">-Action</span></span>
<span data-ttu-id="d820a-114">Virgülle ayrılmış bir eylem listesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d820a-115">-DefaultProfile</span></span>
<span data-ttu-id="d820a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d820a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d820a-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="d820a-117">-Description</span></span>
<span data-ttu-id="d820a-118">Kuralın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-118">Specifies a description of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="d820a-119">-DisableRule</span></span>
<span data-ttu-id="d820a-120">Kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="d820a-120">Disables the rule.</span></span>
<span data-ttu-id="d820a-121">Bu parametreyi belirtmezseniz, kural etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d820a-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="d820a-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="d820a-122">-FailedLocationCount</span></span>
<span data-ttu-id="d820a-123">WebTest kuralları için başarısız olan konum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="d820a-124">Bu, diğer kural türlerinde eşik ile benzerdir.</span><span class="sxs-lookup"><span data-stu-id="d820a-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="d820a-125">-Location</span></span>
<span data-ttu-id="d820a-126">Kuralın tanımlandığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="d820a-127">-MetricName</span></span>
<span data-ttu-id="d820a-128">Ölçümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-128">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="d820a-129">-MetricNamespace</span></span>
<span data-ttu-id="d820a-130">Kural için ölçü ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-130">Specifies the metric namespace for rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="d820a-131">-Name</span></span>
<span data-ttu-id="d820a-132">Kuralın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-132">Specifies the name of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d820a-133">-ResourceGroupName</span></span>
<span data-ttu-id="d820a-134">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-134">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="d820a-135">-TargetResourceUri</span></span>
<span data-ttu-id="d820a-136">WebTest 'in kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="d820a-137">-WindowSize</span></span>
<span data-ttu-id="d820a-138">Kuralın verilerinin hesaplanması için zaman penceresi boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d820a-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d820a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d820a-139">CommonParameters</span></span>
<span data-ttu-id="d820a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d820a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d820a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d820a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d820a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d820a-142">INPUTS</span></span>

### <span data-ttu-id="d820a-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d820a-143">None</span></span>
<span data-ttu-id="d820a-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d820a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d820a-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d820a-145">OUTPUTS</span></span>

### <span data-ttu-id="d820a-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d820a-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="d820a-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d820a-147">NOTES</span></span>

## <span data-ttu-id="d820a-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d820a-148">RELATED LINKS</span></span>

[<span data-ttu-id="d820a-149">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="d820a-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="d820a-150">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d820a-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="d820a-151">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="d820a-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="d820a-152">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="d820a-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


