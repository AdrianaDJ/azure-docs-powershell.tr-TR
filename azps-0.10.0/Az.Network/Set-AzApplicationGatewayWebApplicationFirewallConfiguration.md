---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bf4a87ebae55329e4594d11559fda0aee9047cbc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936549"
---
# <span data-ttu-id="a24d5-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a24d5-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="a24d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a24d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a24d5-103">Uygulama ağ geçidinin WAF yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a24d5-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="a24d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a24d5-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a24d5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a24d5-105">DESCRIPTION</span></span>
<span data-ttu-id="a24d5-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i, uygulama ağ geçidinin Web uygulaması güvenlik duvarı (WAF) yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a24d5-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="a24d5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a24d5-107">EXAMPLES</span></span>

### <span data-ttu-id="a24d5-108">Örnek 1: uygulama ağ geçidi Web uygulaması güvenlik duvarı yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="a24d5-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="a24d5-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a24d5-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="a24d5-110">İkinci komut $AppGw uygulamasında depolanan uygulama ağ geçidi için güvenlik duvarı yapılandırmasını belirler ve güvenlik duvarı modunu "algılama", RuleSetType "OWASP" ve RuleSetVersion "3,0" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a24d5-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="a24d5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a24d5-111">PARAMETERS</span></span>

### <span data-ttu-id="a24d5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a24d5-112">-ApplicationGateway</span></span>
<span data-ttu-id="a24d5-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a24d5-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="a24d5-114">Uygulama ağ geçidi nesnesi almak için Get-AzApplicationGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a24d5-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="a24d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24d5-115">-DefaultProfile</span></span>
<span data-ttu-id="a24d5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a24d5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a24d5-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="a24d5-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="a24d5-118">Devre dışı bırakılan kural grupları.</span><span class="sxs-lookup"><span data-stu-id="a24d5-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="a24d5-119">Özellikli</span><span class="sxs-lookup"><span data-stu-id="a24d5-119">-Enabled</span></span>
<span data-ttu-id="a24d5-120">Web uygulaması güvenlik duvarının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a24d5-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="a24d5-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="a24d5-121">-FirewallMode</span></span>
<span data-ttu-id="a24d5-122">Web uygulaması güvenlik duvarı modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a24d5-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="a24d5-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a24d5-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a24d5-124">İti</span><span class="sxs-lookup"><span data-stu-id="a24d5-124">Detection</span></span>
- <span data-ttu-id="a24d5-125">Önleme</span><span class="sxs-lookup"><span data-stu-id="a24d5-125">Prevention</span></span>

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

### <span data-ttu-id="a24d5-126">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="a24d5-126">-RuleSetType</span></span>
<span data-ttu-id="a24d5-127">Web uygulaması güvenlik duvarı kuralı kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="a24d5-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="a24d5-128">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a24d5-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="a24d5-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="a24d5-129">OWASP</span></span>

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

### <span data-ttu-id="a24d5-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="a24d5-130">-RuleSetVersion</span></span>
<span data-ttu-id="a24d5-131">Kural kümesi türünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="a24d5-131">The version of the rule set type.</span></span>
<span data-ttu-id="a24d5-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a24d5-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="a24d5-133">3,0</span><span class="sxs-lookup"><span data-stu-id="a24d5-133">3.0</span></span>
- <span data-ttu-id="a24d5-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="a24d5-134">2.2.9</span></span>

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

### <span data-ttu-id="a24d5-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="a24d5-135">-Confirm</span></span>
<span data-ttu-id="a24d5-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a24d5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a24d5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a24d5-137">-WhatIf</span></span>
<span data-ttu-id="a24d5-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a24d5-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a24d5-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a24d5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a24d5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24d5-140">CommonParameters</span></span>
<span data-ttu-id="a24d5-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a24d5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24d5-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24d5-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24d5-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a24d5-143">INPUTS</span></span>

### <span data-ttu-id="a24d5-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a24d5-144">PSApplicationGateway</span></span>
<span data-ttu-id="a24d5-145">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a24d5-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="a24d5-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a24d5-146">OUTPUTS</span></span>

### <span data-ttu-id="a24d5-147">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a24d5-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a24d5-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a24d5-148">NOTES</span></span>

## <span data-ttu-id="a24d5-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a24d5-149">RELATED LINKS</span></span>

[<span data-ttu-id="a24d5-150">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a24d5-150">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="a24d5-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a24d5-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="a24d5-152">Yeni-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a24d5-152">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


