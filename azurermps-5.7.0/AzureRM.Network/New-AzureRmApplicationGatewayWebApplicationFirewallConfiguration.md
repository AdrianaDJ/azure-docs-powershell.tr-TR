---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bcc40b77208506712a319d7f43d74f8928e18927
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588163"
---
# <span data-ttu-id="a7e24-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7e24-101">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a7e24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7e24-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e24-103">Uygulama ağ geçidi için WAF yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7e24-103">Creates a WAF configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7e24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7e24-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7e24-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7e24-105">DESCRIPTION</span></span>
<span data-ttu-id="a7e24-106">**New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'ı bir Azure Application Gateway için Web uygulaması güvenlik duvarı (WAF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7e24-106">The **New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="a7e24-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7e24-107">EXAMPLES</span></span>

### <span data-ttu-id="a7e24-108">Örnek 1: uygulama ağ geçidi için Web uygulaması güvenlik duvarı yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="a7e24-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="a7e24-109">İlk komut, Rule 942130 ile "REQUEST-942-APPLICATION-SALDÝRÝ-SQLI" adlı kural grubu için yeni bir devre dışı kural grubu yapılandırması oluşturur ve 942140 kuralı devre dışı bırakılıyor.</span><span class="sxs-lookup"><span data-stu-id="a7e24-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="a7e24-110">İkinci komut, "REQUEST-921-PROTOCOL-SALDÝRÝ" adlı bir kural grubu için başka bir devre dışı bırakılmış kural grubu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7e24-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="a7e24-111">Kural özel olarak geçirilir ve kural grubundaki tüm kurallar devre dışı bırakılır.</span><span class="sxs-lookup"><span data-stu-id="a7e24-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="a7e24-112">Son komut, $disabledRuleGroup 1 ve $disabledRuleGroup 2 ' de yapılandırıldığı şekilde güvenlik duvarı kuralları devre dışı bırakılmış bir WAF yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7e24-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="a7e24-113">Yeni WAF yapılandırması $firewallConfig değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="a7e24-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="a7e24-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7e24-114">PARAMETERS</span></span>

### <span data-ttu-id="a7e24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e24-115">-DefaultProfile</span></span>
<span data-ttu-id="a7e24-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7e24-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7e24-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="a7e24-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="a7e24-118">Devre dışı bırakılan kural grupları.</span><span class="sxs-lookup"><span data-stu-id="a7e24-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="a7e24-119">Özellikli</span><span class="sxs-lookup"><span data-stu-id="a7e24-119">-Enabled</span></span>
<span data-ttu-id="a7e24-120">WAF özelliğinin etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7e24-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e24-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="a7e24-121">-FirewallMode</span></span>
<span data-ttu-id="a7e24-122">Web uygulaması güvenlik duvarı modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7e24-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="a7e24-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a7e24-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a7e24-124">İti</span><span class="sxs-lookup"><span data-stu-id="a7e24-124">Detection</span></span>
- <span data-ttu-id="a7e24-125">Önleme</span><span class="sxs-lookup"><span data-stu-id="a7e24-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e24-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="a7e24-126">-RuleSetType</span></span>
<span data-ttu-id="a7e24-127">Web uygulaması güvenlik duvarı kuralı kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="a7e24-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="a7e24-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a7e24-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="a7e24-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="a7e24-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e24-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="a7e24-130">-RuleSetVersion</span></span>
<span data-ttu-id="a7e24-131">Kural kümesi türünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="a7e24-131">The version of the rule set type.</span></span>
<span data-ttu-id="a7e24-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a7e24-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="a7e24-133">3,0</span><span class="sxs-lookup"><span data-stu-id="a7e24-133">3.0</span></span>
- <span data-ttu-id="a7e24-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="a7e24-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e24-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7e24-135">-Confirm</span></span>
<span data-ttu-id="a7e24-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7e24-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e24-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7e24-137">-WhatIf</span></span>
<span data-ttu-id="a7e24-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7e24-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7e24-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7e24-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7e24-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e24-140">CommonParameters</span></span>
<span data-ttu-id="a7e24-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7e24-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e24-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7e24-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e24-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7e24-143">INPUTS</span></span>

### <span data-ttu-id="a7e24-144">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a7e24-144">None</span></span>
<span data-ttu-id="a7e24-145">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a7e24-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7e24-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7e24-146">OUTPUTS</span></span>

### <span data-ttu-id="a7e24-147">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7e24-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a7e24-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7e24-148">NOTES</span></span>

## <span data-ttu-id="a7e24-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7e24-149">RELATED LINKS</span></span>

[<span data-ttu-id="a7e24-150">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7e24-150">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="a7e24-151">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7e24-151">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


