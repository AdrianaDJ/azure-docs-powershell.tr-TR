---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 689dbeef5dd51b525ae5858129c448ba52faab43
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760370"
---
# <span data-ttu-id="d608b-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d608b-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d608b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d608b-102">SYNOPSIS</span></span>
<span data-ttu-id="d608b-103">Uygulama ağ geçidi için WAF yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d608b-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="d608b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d608b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d608b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d608b-105">DESCRIPTION</span></span>
<span data-ttu-id="d608b-106">**Yeni-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'ı bir Azure uygulama ağ geçidi için Web uygulaması güvenlik duvarı (WAF) yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d608b-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="d608b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d608b-107">EXAMPLES</span></span>

### <span data-ttu-id="d608b-108">Örnek 1: uygulama ağ geçidi için Web uygulaması güvenlik duvarı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d608b-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="d608b-109">İlk komut, Rule 942130 ile "REQUEST-942-APPLICATION-SALDÝRÝ-SQLI" adlı kural grubu için yeni bir devre dışı kural grubu yapılandırması oluşturur ve 942140 kuralı devre dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="d608b-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="d608b-110">İkinci komut, "REQUEST-921-PROTOCOL-SALDÝRÝ" adlı bir kural grubu için başka bir devre dışı bırakılmış kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d608b-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="d608b-111">Kural özel olarak geçirilir ve kural grubundaki tüm kurallar devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="d608b-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="d608b-112">Son komut, $disabledRuleGroup 1 ve $disabledRuleGroup 2 ' de yapılandırıldığı şekilde güvenlik duvarı kuralları devre dışı bırakılmış bir WAF yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d608b-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="d608b-113">Yeni WAF yapılandırması $firewallConfig değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="d608b-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="d608b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d608b-114">PARAMETERS</span></span>

### <span data-ttu-id="d608b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d608b-115">-DefaultProfile</span></span>
<span data-ttu-id="d608b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d608b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d608b-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="d608b-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="d608b-118">Devre dışı bırakılan kural grupları.</span><span class="sxs-lookup"><span data-stu-id="d608b-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="d608b-119">Özellikli</span><span class="sxs-lookup"><span data-stu-id="d608b-119">-Enabled</span></span>
<span data-ttu-id="d608b-120">WAF özelliğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d608b-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="d608b-121">-Dışlama</span><span class="sxs-lookup"><span data-stu-id="d608b-121">-Exclusion</span></span>
<span data-ttu-id="d608b-122">Dışlama Listeleri.</span><span class="sxs-lookup"><span data-stu-id="d608b-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="d608b-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="d608b-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="d608b-124">MB cinsinden dosya karşıya yükleme sınırı.</span><span class="sxs-lookup"><span data-stu-id="d608b-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="d608b-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="d608b-125">-FirewallMode</span></span>
<span data-ttu-id="d608b-126">Web uygulaması güvenlik duvarı modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d608b-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="d608b-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d608b-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d608b-128">İti</span><span class="sxs-lookup"><span data-stu-id="d608b-128">Detection</span></span>
- <span data-ttu-id="d608b-129">Önleme</span><span class="sxs-lookup"><span data-stu-id="d608b-129">Prevention</span></span>

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

### <span data-ttu-id="d608b-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="d608b-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="d608b-131">KB cinsinden en büyük istek gövdesi boyutu.</span><span class="sxs-lookup"><span data-stu-id="d608b-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="d608b-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="d608b-132">-RequestBodyCheck</span></span>
<span data-ttu-id="d608b-133">İstek gövdesinin işaretli olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="d608b-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="d608b-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="d608b-134">-RuleSetType</span></span>
<span data-ttu-id="d608b-135">Web uygulaması güvenlik duvarı kuralı kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="d608b-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="d608b-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d608b-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="d608b-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="d608b-137">OWASP</span></span>

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

### <span data-ttu-id="d608b-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="d608b-138">-RuleSetVersion</span></span>
<span data-ttu-id="d608b-139">Kural kümesi türünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="d608b-139">The version of the rule set type.</span></span>
<span data-ttu-id="d608b-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d608b-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="d608b-141">3,0</span><span class="sxs-lookup"><span data-stu-id="d608b-141">3.0</span></span>
- <span data-ttu-id="d608b-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="d608b-142">2.2.9</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d608b-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="d608b-143">-Confirm</span></span>
<span data-ttu-id="d608b-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d608b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d608b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d608b-145">-WhatIf</span></span>
<span data-ttu-id="d608b-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d608b-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d608b-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d608b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d608b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d608b-148">CommonParameters</span></span>
<span data-ttu-id="d608b-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d608b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d608b-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d608b-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d608b-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d608b-151">INPUTS</span></span>

### <span data-ttu-id="d608b-152">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d608b-152">None</span></span>

## <span data-ttu-id="d608b-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d608b-153">OUTPUTS</span></span>

### <span data-ttu-id="d608b-154">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d608b-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d608b-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d608b-155">NOTES</span></span>

## <span data-ttu-id="d608b-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d608b-156">RELATED LINKS</span></span>

[<span data-ttu-id="d608b-157">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d608b-157">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="d608b-158">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d608b-158">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


