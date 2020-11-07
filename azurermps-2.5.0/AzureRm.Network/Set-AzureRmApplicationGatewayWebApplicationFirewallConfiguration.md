---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: fd925829248c7f11f047de90ddc2bc0b57f51b71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939500"
---
# <span data-ttu-id="db87b-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="db87b-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="db87b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db87b-102">SYNOPSIS</span></span>
<span data-ttu-id="db87b-103">Uygulama ağ geçidinin WAF yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="db87b-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db87b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db87b-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db87b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db87b-105">DESCRIPTION</span></span>
<span data-ttu-id="db87b-106">**Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i, uygulama ağ geçidinin Web uygulaması güvenlik duvarı (WAF) yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="db87b-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="db87b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db87b-107">EXAMPLES</span></span>

### <span data-ttu-id="db87b-108">Örnek 1: uygulama ağ geçidi Web uygulaması güvenlik duvarı yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="db87b-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="db87b-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="db87b-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="db87b-110">İkinci komut $AppGw uygulamasında depolanan uygulama ağ geçidi için güvenlik duvarı yapılandırmasını belirler ve güvenlik duvarı modunu "algılama", RuleSetType "OWASP" ve RuleSetVersion "3,0" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="db87b-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="db87b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db87b-111">PARAMETERS</span></span>

### <span data-ttu-id="db87b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db87b-112">-ApplicationGateway</span></span>
<span data-ttu-id="db87b-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="db87b-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="db87b-114">Uygulama ağ geçidi nesnesi almak için Get-AzureRmApplicationGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db87b-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db87b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db87b-115">-DefaultProfile</span></span>
<span data-ttu-id="db87b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db87b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db87b-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="db87b-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="db87b-118">Devre dışı bırakılan kural grupları.</span><span class="sxs-lookup"><span data-stu-id="db87b-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="db87b-119">Özellikli</span><span class="sxs-lookup"><span data-stu-id="db87b-119">-Enabled</span></span>
<span data-ttu-id="db87b-120">Web uygulaması güvenlik duvarının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="db87b-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="db87b-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="db87b-121">-FirewallMode</span></span>
<span data-ttu-id="db87b-122">Web uygulaması güvenlik duvarı modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="db87b-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="db87b-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db87b-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db87b-124">İti</span><span class="sxs-lookup"><span data-stu-id="db87b-124">Detection</span></span>
- <span data-ttu-id="db87b-125">Önleme</span><span class="sxs-lookup"><span data-stu-id="db87b-125">Prevention</span></span>

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

### <span data-ttu-id="db87b-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="db87b-126">-RuleSetType</span></span>
<span data-ttu-id="db87b-127">Web uygulaması güvenlik duvarı kuralı kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="db87b-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="db87b-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db87b-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="db87b-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="db87b-129">OWASP</span></span>

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

### <span data-ttu-id="db87b-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="db87b-130">-RuleSetVersion</span></span>
<span data-ttu-id="db87b-131">Kural kümesi türünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="db87b-131">The version of the rule set type.</span></span>
<span data-ttu-id="db87b-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="db87b-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="db87b-133">3,0</span><span class="sxs-lookup"><span data-stu-id="db87b-133">3.0</span></span>
- <span data-ttu-id="db87b-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="db87b-134">2.2.9</span></span>

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

### <span data-ttu-id="db87b-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="db87b-135">-Confirm</span></span>
<span data-ttu-id="db87b-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db87b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db87b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db87b-137">-WhatIf</span></span>
<span data-ttu-id="db87b-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db87b-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db87b-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db87b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db87b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db87b-140">CommonParameters</span></span>
<span data-ttu-id="db87b-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db87b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db87b-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db87b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db87b-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db87b-143">INPUTS</span></span>

### <span data-ttu-id="db87b-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db87b-144">PSApplicationGateway</span></span>
<span data-ttu-id="db87b-145">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="db87b-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="db87b-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db87b-146">OUTPUTS</span></span>

### <span data-ttu-id="db87b-147">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db87b-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="db87b-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db87b-148">NOTES</span></span>

## <span data-ttu-id="db87b-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db87b-149">RELATED LINKS</span></span>

[<span data-ttu-id="db87b-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="db87b-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="db87b-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="db87b-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="db87b-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="db87b-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


