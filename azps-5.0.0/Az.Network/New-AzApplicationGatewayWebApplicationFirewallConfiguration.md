---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324637"
---
# <span data-ttu-id="e1222-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1222-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e1222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1222-102">SYNOPSIS</span></span>
<span data-ttu-id="e1222-103">Uygulama ağ geçidi için WAF yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1222-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="e1222-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e1222-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1222-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e1222-105">DESCRIPTION</span></span>
<span data-ttu-id="e1222-106">**Yeni-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'ı bir Azure uygulama ağ geçidi için Web uygulaması güvenlik duvarı (WAF) yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1222-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="e1222-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e1222-107">EXAMPLES</span></span>

### <span data-ttu-id="e1222-108">Örnek 1: uygulama ağ geçidi için Web uygulaması güvenlik duvarı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="e1222-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="e1222-109">İlk komut, Rule 942130 ile "REQUEST-942-APPLICATION-SALDÝRÝ-SQLI" adlı kural grubu için yeni bir devre dışı kural grubu yapılandırması oluşturur ve 942140 kuralı devre dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="e1222-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="e1222-110">İkinci komut, "REQUEST-921-PROTOCOL-SALDÝRÝ" adlı bir kural grubu için başka bir devre dışı bırakılmış kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1222-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="e1222-111">Kural özel olarak geçirilir ve kural grubundaki tüm kurallar devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="e1222-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="e1222-112">Son komut, $disabledRuleGroup 1 ve $disabledRuleGroup 2 ' de yapılandırıldığı şekilde güvenlik duvarı kuralları devre dışı bırakılmış bir WAF yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e1222-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="e1222-113">Yeni WAF yapılandırması $firewallConfig değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="e1222-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="e1222-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e1222-114">PARAMETERS</span></span>

### <span data-ttu-id="e1222-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1222-115">-DefaultProfile</span></span>
<span data-ttu-id="e1222-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e1222-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1222-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="e1222-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="e1222-118">Devre dışı bırakılan kural grupları.</span><span class="sxs-lookup"><span data-stu-id="e1222-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-119">Özellikli</span><span class="sxs-lookup"><span data-stu-id="e1222-119">-Enabled</span></span>
<span data-ttu-id="e1222-120">WAF özelliğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1222-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-121">-Dışlama</span><span class="sxs-lookup"><span data-stu-id="e1222-121">-Exclusion</span></span>
<span data-ttu-id="e1222-122">Dışlama Listeleri.</span><span class="sxs-lookup"><span data-stu-id="e1222-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="e1222-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="e1222-124">MB cinsinden dosya karşıya yükleme sınırı.</span><span class="sxs-lookup"><span data-stu-id="e1222-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="e1222-125">-FirewallMode</span></span>
<span data-ttu-id="e1222-126">Web uygulaması güvenlik duvarı modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e1222-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="e1222-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e1222-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e1222-128">İti</span><span class="sxs-lookup"><span data-stu-id="e1222-128">Detection</span></span>
- <span data-ttu-id="e1222-129">Önleme</span><span class="sxs-lookup"><span data-stu-id="e1222-129">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="e1222-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="e1222-131">KB cinsinden en büyük istek gövdesi boyutu.</span><span class="sxs-lookup"><span data-stu-id="e1222-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="e1222-132">-RequestBodyCheck</span></span>
<span data-ttu-id="e1222-133">İstek gövdesinin işaretli olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="e1222-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="e1222-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="e1222-134">-RuleSetType</span></span>
<span data-ttu-id="e1222-135">Web uygulaması güvenlik duvarı kuralı kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="e1222-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="e1222-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="e1222-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="e1222-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="e1222-137">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="e1222-138">-RuleSetVersion</span></span>
<span data-ttu-id="e1222-139">Kural kümesi türünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="e1222-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="e1222-140">-Confirm</span></span>
<span data-ttu-id="e1222-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e1222-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1222-142">-WhatIf</span></span>
<span data-ttu-id="e1222-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e1222-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1222-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e1222-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1222-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1222-145">CommonParameters</span></span>
<span data-ttu-id="e1222-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e1222-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1222-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1222-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1222-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e1222-148">INPUTS</span></span>

### <span data-ttu-id="e1222-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e1222-149">None</span></span>

## <span data-ttu-id="e1222-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e1222-150">OUTPUTS</span></span>

### <span data-ttu-id="e1222-151">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1222-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e1222-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e1222-152">NOTES</span></span>

## <span data-ttu-id="e1222-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e1222-153">RELATED LINKS</span></span>

[<span data-ttu-id="e1222-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1222-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="e1222-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1222-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


