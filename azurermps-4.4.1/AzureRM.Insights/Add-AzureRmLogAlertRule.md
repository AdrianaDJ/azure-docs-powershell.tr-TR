---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594680"
---
# <span data-ttu-id="a01d4-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="a01d4-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="a01d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a01d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a01d4-103">Günlük uyarısı kuralı ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a01d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a01d4-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a01d4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a01d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a01d4-106">**Add-AzureRmLogAlertRule** cmdlet 'i, bir olay uyarısı kuralı ekler veya değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="a01d4-107">Ek kural bir kaynak grubuyla ilişkilendirilir ve bir adı vardır.</span><span class="sxs-lookup"><span data-stu-id="a01d4-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="a01d4-108">Önceki sürümlerde duyurulmuş gibi: **Add-AzureRMLogAlertRule cmdlet 'i gelecekteki sürümlerde onaylanmaz.**</span><span class="sxs-lookup"><span data-stu-id="a01d4-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="a01d4-109">1 ' inci 1 ' den sonra 2017 bu cmdlet 'i kullanarak bu işlev etkinlik günlüğü uyarılarını geçti.</span><span class="sxs-lookup"><span data-stu-id="a01d4-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="a01d4-110">**_https://aka.ms/migratemealerts_** Daha fazla bilgi için lütfen bkz.</span><span class="sxs-lookup"><span data-stu-id="a01d4-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="a01d4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a01d4-111">EXAMPLES</span></span>

### <span data-ttu-id="a01d4-112">Örnek 1: günlük uyarısı kuralı ekleme</span><span class="sxs-lookup"><span data-stu-id="a01d4-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="a01d4-113">Bu komut, olaya dayalı bir uyarı kuralı ekler veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="a01d4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a01d4-114">PARAMETERS</span></span>

### <span data-ttu-id="a01d4-115">-Eylemler</span><span class="sxs-lookup"><span data-stu-id="a01d4-115">-Actions</span></span>
<span data-ttu-id="a01d4-116">Virgülle ayrılmış bir eylem listesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-116">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="a01d4-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="a01d4-117">-Description</span></span>
<span data-ttu-id="a01d4-118">Kuralın açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="a01d4-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="a01d4-119">-DisableRule</span></span>
<span data-ttu-id="a01d4-120">Kuralı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="a01d4-120">Disables a rule.</span></span>
<span data-ttu-id="a01d4-121">Bu parametreyi belirtmezseniz, kural etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="a01d4-122">Düzey</span><span class="sxs-lookup"><span data-stu-id="a01d4-122">-Level</span></span>
<span data-ttu-id="a01d4-123">Kuralın izlenme olayının düzeyini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="a01d4-124">Bu parametreyi yalnızca olay tabanlı kurallar için belirtin.</span><span class="sxs-lookup"><span data-stu-id="a01d4-124">Specify this parameter only for event-based rules.</span></span>

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

### <span data-ttu-id="a01d4-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="a01d4-125">-Location</span></span>
<span data-ttu-id="a01d4-126">Kuralın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="a01d4-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="a01d4-127">-Name</span></span>
<span data-ttu-id="a01d4-128">Kuralın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="a01d4-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="a01d4-129">-OperationName</span></span>
<span data-ttu-id="a01d4-130">İşlemin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="a01d4-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a01d4-131">-ResourceGroup</span></span>
<span data-ttu-id="a01d4-132">Kuralın kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="a01d4-133">-Durum</span><span class="sxs-lookup"><span data-stu-id="a01d4-133">-Status</span></span>
<span data-ttu-id="a01d4-134">Durumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-134">Specifies the status.</span></span>

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

### <span data-ttu-id="a01d4-135">-Alt durum</span><span class="sxs-lookup"><span data-stu-id="a01d4-135">-SubStatus</span></span>
<span data-ttu-id="a01d4-136">Alt durumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-136">Specifies the substatus.</span></span>

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

### <span data-ttu-id="a01d4-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a01d4-137">-TargetResourceGroup</span></span>
<span data-ttu-id="a01d4-138">Kuralın izlenme kaynağının kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="a01d4-139">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="a01d4-139">-TargetResourceId</span></span>
<span data-ttu-id="a01d4-140">Kuralın izlenme kaynağının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-140">Specifies the ID of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="a01d4-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a01d4-141">-TargetResourceProvider</span></span>
<span data-ttu-id="a01d4-142">Kuralın izlenme kaynağının kaynak sağlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a01d4-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="a01d4-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a01d4-143">-DefaultProfile</span></span>
<span data-ttu-id="a01d4-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a01d4-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a01d4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01d4-145">CommonParameters</span></span>
<span data-ttu-id="a01d4-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a01d4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01d4-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01d4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01d4-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a01d4-148">INPUTS</span></span>

## <span data-ttu-id="a01d4-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a01d4-149">OUTPUTS</span></span>

### <span data-ttu-id="a01d4-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a01d4-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="a01d4-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a01d4-151">NOTES</span></span>

## <span data-ttu-id="a01d4-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a01d4-152">RELATED LINKS</span></span>

[<span data-ttu-id="a01d4-153">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a01d4-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="a01d4-154">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a01d4-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="a01d4-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="a01d4-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="a01d4-156">Yeni-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="a01d4-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="a01d4-157">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="a01d4-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


