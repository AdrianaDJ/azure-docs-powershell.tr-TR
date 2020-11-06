---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 281a4a0d935d73777f7fdd693f3d32982b2da47a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589966"
---
# <span data-ttu-id="49098-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="49098-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="49098-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49098-102">SYNOPSIS</span></span>
<span data-ttu-id="49098-103">Uygulama ağ geçidi için WAF yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49098-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49098-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49098-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49098-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="49098-105">DESCRIPTION</span></span>
<span data-ttu-id="49098-106">**New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'ı bir Azure Application Gateway için Web uygulaması güvenlik duvarı (WAF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49098-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="49098-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49098-107">EXAMPLES</span></span>

### <span data-ttu-id="49098-108">Örnek 1: uygulama ağ geçidi için Web uygulaması güvenlik duvarı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="49098-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="49098-109">İlk komut, Rule 942130 ile "REQUEST-942-APPLICATION-SALDÝRÝ-SQLI" adlı kural grubu için yeni bir devre dışı kural grubu yapılandırması oluşturur ve 942140 kuralı devre dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="49098-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="49098-110">İkinci komut, "REQUEST-921-PROTOCOL-SALDÝRÝ" adlı bir kural grubu için başka bir devre dışı bırakılmış kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49098-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="49098-111">Kural özel olarak geçirilir ve kural grubundaki tüm kurallar devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="49098-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="49098-112">Son komut, $disabledRuleGroup 1 ve $disabledRuleGroup 2 ' de yapılandırıldığı şekilde güvenlik duvarı kuralları devre dışı bırakılmış bir WAF yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="49098-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="49098-113">Yeni WAF yapılandırması $firewallConfig değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="49098-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="49098-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49098-114">PARAMETERS</span></span>

### <span data-ttu-id="49098-115">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="49098-115">-DisabledRuleGroups</span></span>
<span data-ttu-id="49098-116">Devre dışı bırakılan kural grupları.</span><span class="sxs-lookup"><span data-stu-id="49098-116">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49098-117">Özellikli</span><span class="sxs-lookup"><span data-stu-id="49098-117">-Enabled</span></span>
<span data-ttu-id="49098-118">WAF özelliğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="49098-118">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="49098-119">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="49098-119">-FirewallMode</span></span>
<span data-ttu-id="49098-120">Web uygulaması güvenlik duvarı modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="49098-120">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="49098-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="49098-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="49098-122">İti</span><span class="sxs-lookup"><span data-stu-id="49098-122">Detection</span></span>
- <span data-ttu-id="49098-123">Önleme</span><span class="sxs-lookup"><span data-stu-id="49098-123">Prevention</span></span>

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

### <span data-ttu-id="49098-124">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="49098-124">-RuleSetType</span></span>
<span data-ttu-id="49098-125">Web uygulaması güvenlik duvarı kuralı kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="49098-125">The type of the web application firewall rule set.</span></span> <span data-ttu-id="49098-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="49098-126">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="49098-127">OWASP</span><span class="sxs-lookup"><span data-stu-id="49098-127">OWASP</span></span>

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

### <span data-ttu-id="49098-128">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="49098-128">-RuleSetVersion</span></span>
<span data-ttu-id="49098-129">Kural kümesi türünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="49098-129">The version of the rule set type.</span></span>
<span data-ttu-id="49098-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="49098-130">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="49098-131">3,0</span><span class="sxs-lookup"><span data-stu-id="49098-131">3.0</span></span>
- <span data-ttu-id="49098-132">2.2.9</span><span class="sxs-lookup"><span data-stu-id="49098-132">2.2.9</span></span>

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

### <span data-ttu-id="49098-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="49098-133">-Confirm</span></span>
<span data-ttu-id="49098-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="49098-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49098-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49098-135">-WhatIf</span></span>
<span data-ttu-id="49098-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="49098-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49098-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="49098-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49098-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49098-138">-DefaultProfile</span></span>
<span data-ttu-id="49098-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49098-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49098-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49098-140">CommonParameters</span></span>
<span data-ttu-id="49098-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49098-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49098-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49098-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49098-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49098-143">INPUTS</span></span>

## <span data-ttu-id="49098-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49098-144">OUTPUTS</span></span>

### <span data-ttu-id="49098-145">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="49098-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="49098-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49098-146">NOTES</span></span>

## <span data-ttu-id="49098-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49098-147">RELATED LINKS</span></span>

[<span data-ttu-id="49098-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="49098-148">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="49098-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="49098-149">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


