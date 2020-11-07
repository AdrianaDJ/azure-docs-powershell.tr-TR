---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: a5f60588a0db848d0b96aa0611b8647142db2b06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760028"
---
# <span data-ttu-id="d8483-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8483-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="d8483-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8483-102">SYNOPSIS</span></span>
<span data-ttu-id="d8483-103">Uygulama ağ geçidinin WAF yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d8483-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="d8483-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8483-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8483-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8483-105">DESCRIPTION</span></span>
<span data-ttu-id="d8483-106">**Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet 'i, uygulama ağ geçidinin Web uygulaması güvenlik duvarı (WAF) yapılandırmasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d8483-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="d8483-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8483-107">EXAMPLES</span></span>

### <span data-ttu-id="d8483-108">Örnek 1: uygulama ağ geçidi Web uygulaması güvenlik duvarı yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d8483-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="d8483-109">İlk komut ApplicationGateway01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8483-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d8483-110">İkinci komut $AppGw uygulamasında depolanan uygulama ağ geçidi için güvenlik duvarı yapılandırmasını belirler ve güvenlik duvarı modunu "algılama", RuleSetType "OWASP" ve RuleSetVersion "3,0" olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d8483-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="d8483-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8483-111">PARAMETERS</span></span>

### <span data-ttu-id="d8483-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8483-112">-ApplicationGateway</span></span>
<span data-ttu-id="d8483-113">Uygulama ağ geçidi nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8483-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="d8483-114">Uygulama ağ geçidi nesnesi almak için Get-AzApplicationGateway cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8483-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="d8483-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8483-115">-DefaultProfile</span></span>
<span data-ttu-id="d8483-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8483-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8483-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="d8483-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="d8483-118">Devre dışı bırakılan kural grupları.</span><span class="sxs-lookup"><span data-stu-id="d8483-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="d8483-119">Özellikli</span><span class="sxs-lookup"><span data-stu-id="d8483-119">-Enabled</span></span>
<span data-ttu-id="d8483-120">Web uygulaması güvenlik duvarının etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8483-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="d8483-121">-Dışlama</span><span class="sxs-lookup"><span data-stu-id="d8483-121">-Exclusion</span></span>
<span data-ttu-id="d8483-122">Dışlama Listeleri.</span><span class="sxs-lookup"><span data-stu-id="d8483-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="d8483-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="d8483-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="d8483-124">MB cinsinden dosya karşıya yükleme sınırı.</span><span class="sxs-lookup"><span data-stu-id="d8483-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="d8483-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="d8483-125">-FirewallMode</span></span>
<span data-ttu-id="d8483-126">Web uygulaması güvenlik duvarı modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8483-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="d8483-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d8483-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8483-128">İti</span><span class="sxs-lookup"><span data-stu-id="d8483-128">Detection</span></span>
- <span data-ttu-id="d8483-129">Önleme</span><span class="sxs-lookup"><span data-stu-id="d8483-129">Prevention</span></span>

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

### <span data-ttu-id="d8483-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="d8483-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="d8483-131">KB cinsinden en büyük istek gövdesi boyutu.</span><span class="sxs-lookup"><span data-stu-id="d8483-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="d8483-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="d8483-132">-RequestBodyCheck</span></span>
<span data-ttu-id="d8483-133">İstek gövdesinin işaretli olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="d8483-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="d8483-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="d8483-134">-RuleSetType</span></span>
<span data-ttu-id="d8483-135">Web uygulaması güvenlik duvarı kuralı kümesi türü.</span><span class="sxs-lookup"><span data-stu-id="d8483-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="d8483-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d8483-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="d8483-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="d8483-137">OWASP</span></span>

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

### <span data-ttu-id="d8483-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="d8483-138">-RuleSetVersion</span></span>
<span data-ttu-id="d8483-139">Kural kümesi türünün sürümü.</span><span class="sxs-lookup"><span data-stu-id="d8483-139">The version of the rule set type.</span></span>
<span data-ttu-id="d8483-140">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d8483-140">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="d8483-141">3,0</span><span class="sxs-lookup"><span data-stu-id="d8483-141">3.0</span></span>
- <span data-ttu-id="d8483-142">2.2.9</span><span class="sxs-lookup"><span data-stu-id="d8483-142">2.2.9</span></span>

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

### <span data-ttu-id="d8483-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8483-143">-Confirm</span></span>
<span data-ttu-id="d8483-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8483-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8483-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8483-145">-WhatIf</span></span>
<span data-ttu-id="d8483-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8483-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8483-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8483-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8483-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8483-148">CommonParameters</span></span>
<span data-ttu-id="d8483-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8483-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8483-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8483-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8483-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8483-151">INPUTS</span></span>

### <span data-ttu-id="d8483-152">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8483-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8483-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8483-153">OUTPUTS</span></span>

### <span data-ttu-id="d8483-154">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8483-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d8483-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8483-155">NOTES</span></span>

## <span data-ttu-id="d8483-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8483-156">RELATED LINKS</span></span>

[<span data-ttu-id="d8483-157">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d8483-157">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="d8483-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8483-158">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="d8483-159">Yeni-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8483-159">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

