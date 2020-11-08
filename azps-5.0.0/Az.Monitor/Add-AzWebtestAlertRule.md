---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzWebtestAlertRule.md
ms.openlocfilehash: 043bb0e0b3c5fac61407eaca3d20c82ebe483037
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280056"
---
# <span data-ttu-id="1ecf2-101">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="1ecf2-101">Add-AzWebtestAlertRule</span></span>

## <span data-ttu-id="1ecf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ecf2-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecf2-103">Bir WebTest uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-103">Adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="1ecf2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ecf2-104">SYNTAX</span></span>

```
Add-AzWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ecf2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ecf2-105">DESCRIPTION</span></span>
<span data-ttu-id="1ecf2-106">**Add-AzWebtestAlertRule** cmdlet 'i, metrik, olay veya WebTest türünden bir uyarı kuralı ekler veya bu kuralı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-106">The **Add-AzWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="1ecf2-107">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="1ecf2-108">Bu cmdlet, ShouldProcess desenini uygular Yani, kaynağı oluşturmadan, değiştirmeden veya kaldırmadan önce kullanıcıdan onay isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="1ecf2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ecf2-109">EXAMPLES</span></span>

### <span data-ttu-id="1ecf2-110">Örnek 1: WebTest uyarı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="1ecf2-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="1ecf2-111">Bu komut bir WebTest uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="1ecf2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ecf2-112">PARAMETERS</span></span>

### <span data-ttu-id="1ecf2-113">-Eylem</span><span class="sxs-lookup"><span data-stu-id="1ecf2-113">-Action</span></span>
<span data-ttu-id="1ecf2-114">Virgülle ayrılmış bir eylem listesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-114">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="1ecf2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecf2-115">-DefaultProfile</span></span>
<span data-ttu-id="1ecf2-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1ecf2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ecf2-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="1ecf2-117">-Description</span></span>
<span data-ttu-id="1ecf2-118">Kuralın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="1ecf2-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="1ecf2-119">-DisableRule</span></span>
<span data-ttu-id="1ecf2-120">Kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-120">Disables the rule.</span></span>
<span data-ttu-id="1ecf2-121">Bu parametreyi belirtmezseniz, kural etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="1ecf2-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="1ecf2-122">-FailedLocationCount</span></span>
<span data-ttu-id="1ecf2-123">WebTest kuralları için başarısız olan konum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="1ecf2-124">Bu, diğer kural türlerinde eşik ile benzerdir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-124">This is similar to the threshold in the other types of rules.</span></span>

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

### <span data-ttu-id="1ecf2-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="1ecf2-125">-Location</span></span>
<span data-ttu-id="1ecf2-126">Kuralın tanımlandığı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-126">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="1ecf2-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="1ecf2-127">-MetricName</span></span>
<span data-ttu-id="1ecf2-128">Ölçümün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-128">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="1ecf2-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="1ecf2-129">-MetricNamespace</span></span>
<span data-ttu-id="1ecf2-130">Kural için ölçü ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-130">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="1ecf2-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ecf2-131">-Name</span></span>
<span data-ttu-id="1ecf2-132">Kuralın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-132">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="1ecf2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ecf2-133">-ResourceGroupName</span></span>
<span data-ttu-id="1ecf2-134">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-134">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ecf2-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="1ecf2-135">-TargetResourceUri</span></span>
<span data-ttu-id="1ecf2-136">WebTest 'in kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-136">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="1ecf2-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="1ecf2-137">-WindowSize</span></span>
<span data-ttu-id="1ecf2-138">Kuralın verilerinin hesaplanması için zaman penceresi boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-138">Specifies the time window size for the rule to compute its data.</span></span>

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

### <span data-ttu-id="1ecf2-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ecf2-139">-Confirm</span></span>
<span data-ttu-id="1ecf2-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ecf2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ecf2-141">-WhatIf</span></span>
<span data-ttu-id="1ecf2-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ecf2-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ecf2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecf2-144">CommonParameters</span></span>
<span data-ttu-id="1ecf2-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecf2-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1ecf2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecf2-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ecf2-147">INPUTS</span></span>

### <span data-ttu-id="1ecf2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="1ecf2-148">System.String</span></span>

### <span data-ttu-id="1ecf2-149">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="1ecf2-149">System.TimeSpan</span></span>

### <span data-ttu-id="1ecf2-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1ecf2-150">System.Int32</span></span>

### <span data-ttu-id="1ecf2-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ecf2-151">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1ecf2-152">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Management. Monitor. Management. modeller. RuleAction, Microsoft. Azure. PowerShell. cmdlet. Monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1ecf2-152">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1ecf2-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ecf2-153">OUTPUTS</span></span>

### <span data-ttu-id="1ecf2-154">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1ecf2-154">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="1ecf2-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ecf2-155">NOTES</span></span>

## <span data-ttu-id="1ecf2-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ecf2-156">RELATED LINKS</span></span>

[<span data-ttu-id="1ecf2-157">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="1ecf2-157">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="1ecf2-158">Add-Azmetrik ıalertrule</span><span class="sxs-lookup"><span data-stu-id="1ecf2-158">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="1ecf2-159">Get-Azalera</span><span class="sxs-lookup"><span data-stu-id="1ecf2-159">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="1ecf2-160">Yeni-Azalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="1ecf2-160">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


