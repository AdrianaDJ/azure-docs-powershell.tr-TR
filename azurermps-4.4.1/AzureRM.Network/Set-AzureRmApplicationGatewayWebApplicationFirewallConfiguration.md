---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 03acee0ee1e15ffe0be605753d166ff4a956c274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764263"
---
# <span data-ttu-id="f5683-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5683-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="f5683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5683-102">SYNOPSIS</span></span>
<span data-ttu-id="f5683-103">Uygulama ağ geçidinin WAF yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f5683-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5683-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5683-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5683-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5683-105">DESCRIPTION</span></span>
<span data-ttu-id="f5683-106">**Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i, uygulama ağ geçidinin Web uygulaması güvenlik duvarı (WAF) yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f5683-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="f5683-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5683-107">EXAMPLES</span></span>

### <span data-ttu-id="f5683-108">Örnek 1: uygulama ağ geçidi Web uygulaması güvenlik duvarı yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f5683-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="f5683-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f5683-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f5683-110">İkinci komut $AppGw uygulamasında depolanan uygulama ağ geçidi için güvenlik duvarı yapılandırmasını belirler ve güvenlik duvarı modunu "algılama", RuleSetType "OWASP" ve RuleSetVersion "3,0" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f5683-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="f5683-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5683-111">PARAMETERS</span></span>

### <span data-ttu-id="f5683-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5683-112">-ApplicationGateway</span></span>
<span data-ttu-id="f5683-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5683-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="f5683-114">Uygulama ağ geçidi nesnesi almak için Get-AzureRmApplicationGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f5683-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5683-115">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="f5683-115">-DisabledRuleGroups</span></span>
<span data-ttu-id="f5683-116">Devre dışı bırakılan kural grupları.</span><span class="sxs-lookup"><span data-stu-id="f5683-116">The disabled rule groups.</span></span>

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

### <span data-ttu-id="f5683-117">Özellikli</span><span class="sxs-lookup"><span data-stu-id="f5683-117">-Enabled</span></span>
<span data-ttu-id="f5683-118">Web uygulaması güvenlik duvarının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5683-118">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="f5683-119">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="f5683-119">-FirewallMode</span></span>
<span data-ttu-id="f5683-120">Web uygulaması güvenlik duvarı modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5683-120">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="f5683-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f5683-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5683-122">İti</span><span class="sxs-lookup"><span data-stu-id="f5683-122">Detection</span></span>
- <span data-ttu-id="f5683-123">Önleme</span><span class="sxs-lookup"><span data-stu-id="f5683-123">Prevention</span></span>

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

### <span data-ttu-id="f5683-124">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="f5683-124">-RuleSetType</span></span>
<span data-ttu-id="f5683-125">Web uygulaması güvenlik duvarı kuralı kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="f5683-125">The type of the web application firewall rule set.</span></span> <span data-ttu-id="f5683-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f5683-126">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="f5683-127">OWASP</span><span class="sxs-lookup"><span data-stu-id="f5683-127">OWASP</span></span>

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

### <span data-ttu-id="f5683-128">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="f5683-128">-RuleSetVersion</span></span>
<span data-ttu-id="f5683-129">Kural kümesi türünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="f5683-129">The version of the rule set type.</span></span>
<span data-ttu-id="f5683-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f5683-130">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="f5683-131">3,0</span><span class="sxs-lookup"><span data-stu-id="f5683-131">3.0</span></span>
- <span data-ttu-id="f5683-132">2.2.9</span><span class="sxs-lookup"><span data-stu-id="f5683-132">2.2.9</span></span>

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

### <span data-ttu-id="f5683-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5683-133">-Confirm</span></span>
<span data-ttu-id="f5683-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5683-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5683-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5683-135">-WhatIf</span></span>
<span data-ttu-id="f5683-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5683-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5683-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5683-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5683-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5683-138">-DefaultProfile</span></span>
<span data-ttu-id="f5683-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5683-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5683-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5683-140">CommonParameters</span></span>
<span data-ttu-id="f5683-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5683-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5683-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5683-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5683-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5683-143">INPUTS</span></span>

### <span data-ttu-id="f5683-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5683-144">PSApplicationGateway</span></span>
<span data-ttu-id="f5683-145">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="f5683-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="f5683-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5683-146">OUTPUTS</span></span>

### <span data-ttu-id="f5683-147">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5683-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f5683-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5683-148">NOTES</span></span>

## <span data-ttu-id="f5683-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5683-149">RELATED LINKS</span></span>

[<span data-ttu-id="f5683-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5683-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="f5683-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5683-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="f5683-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="f5683-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


