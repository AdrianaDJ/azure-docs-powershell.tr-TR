---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRule.md
ms.openlocfilehash: c7519b6cf5f95f80a20f94bbae5ec097964bd01a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760340"
---
# <span data-ttu-id="e55de-101">New-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="e55de-101">New-AzFirewallNatRule</span></span>

## <span data-ttu-id="e55de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e55de-102">SYNOPSIS</span></span>
<span data-ttu-id="e55de-103">Güvenlik Duvarı NAT kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e55de-103">Creates a Firewall NAT Rule.</span></span>

## <span data-ttu-id="e55de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e55de-104">SYNTAX</span></span>

```
New-AzFirewallNatRule -Name <String> [-Description <String>] -SourceAddress <String[]>
 -DestinationAddress <String[]> -DestinationPort <String[]> -Protocol <String[]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e55de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e55de-105">DESCRIPTION</span></span>
<span data-ttu-id="e55de-106">**New-AzFirewallNatRule** cmdlet 'ı, Azure Güvenlik Duvarı IÇIN bir NAT kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e55de-106">The **New-AzFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="e55de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e55de-107">EXAMPLES</span></span>

### <span data-ttu-id="e55de-108">1: hedef 10.1.2.3 ile 10.0.0.0/24 adresinden tüm TCP trafiğine yönelik bir kural oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e55de-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="e55de-109">Bu örnek, hedef 10.1.2.3 ile 10.0.0.0/24 ile gelen tüm trafikten bir kural oluşturur: 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="e55de-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="e55de-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e55de-110">PARAMETERS</span></span>

### <span data-ttu-id="e55de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e55de-111">-DefaultProfile</span></span>
<span data-ttu-id="e55de-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e55de-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e55de-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e55de-113">-Description</span></span>
<span data-ttu-id="e55de-114">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="e55de-114">Specifies an optional description of this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e55de-115">-DestinationAddress</span></span>
<span data-ttu-id="e55de-116">Kuralın hedef adresleri.</span><span class="sxs-lookup"><span data-stu-id="e55de-116">The destination addresses of the rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e55de-117">-DestinationPort</span></span>
<span data-ttu-id="e55de-118">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="e55de-118">The destination ports of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e55de-119">-Name</span></span>
<span data-ttu-id="e55de-120">Bu NAT kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e55de-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="e55de-121">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e55de-121">The name must be unique inside a rule collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-122">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e55de-122">-Protocol</span></span>
<span data-ttu-id="e55de-123">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e55de-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="e55de-124">Desteklenen protokoller TCP ve UDP.</span><span class="sxs-lookup"><span data-stu-id="e55de-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="e55de-125">"Herhangi" özel bir değere izin verilir, anlamı hem TCP hem de UDP ile eşleşir, ancak başka protokoller içermez.</span><span class="sxs-lookup"><span data-stu-id="e55de-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="e55de-126">-SourceAddress</span></span>
<span data-ttu-id="e55de-127">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="e55de-127">The source addresses of the rule</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="e55de-128">-TranslatedAddress</span></span>
<span data-ttu-id="e55de-129">Adres çevirisinin istenilen sonucunu belirtir</span><span class="sxs-lookup"><span data-stu-id="e55de-129">Specifies the desired result of the address translation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="e55de-130">-TranslatedPort</span></span>
<span data-ttu-id="e55de-131">Bağlantı noktası çevirisinin istenilen sonucunu belirtir</span><span class="sxs-lookup"><span data-stu-id="e55de-131">Specifies the desired result of the port translation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55de-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="e55de-132">-Confirm</span></span>
<span data-ttu-id="e55de-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e55de-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e55de-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e55de-134">-WhatIf</span></span>
<span data-ttu-id="e55de-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e55de-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e55de-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e55de-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e55de-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55de-137">CommonParameters</span></span>
<span data-ttu-id="e55de-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e55de-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55de-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e55de-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55de-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e55de-140">INPUTS</span></span>

### <span data-ttu-id="e55de-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e55de-141">None</span></span>

## <span data-ttu-id="e55de-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e55de-142">OUTPUTS</span></span>

### <span data-ttu-id="e55de-143">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="e55de-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule</span></span>

## <span data-ttu-id="e55de-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e55de-144">NOTES</span></span>

## <span data-ttu-id="e55de-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e55de-145">RELATED LINKS</span></span>

[<span data-ttu-id="e55de-146">Yeni-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="e55de-146">New-AzFirewallNatRuleCollection</span></span>](./New-AzFirewallNatRuleCollection.md)

[<span data-ttu-id="e55de-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e55de-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="e55de-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e55de-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)