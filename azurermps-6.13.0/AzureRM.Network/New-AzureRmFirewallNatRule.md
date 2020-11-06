---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C0E1D4DF-232F-49C6-BE4C-05C8E8038329
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRule.md
ms.openlocfilehash: 0bad5133dd57ec0bee88949fbc9536a6389d6112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591354"
---
# <span data-ttu-id="00d07-101">New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="00d07-101">New-AzureRmFirewallNatRule</span></span>

## <span data-ttu-id="00d07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00d07-102">SYNOPSIS</span></span>
<span data-ttu-id="00d07-103">Güvenlik Duvarı NAT kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00d07-103">Creates a Firewall NAT Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00d07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00d07-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRule -Name <String> [-Description <String>]
 -SourceAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationAddress <System.Collections.Generic.List`1[System.String]>
 -DestinationPort <System.Collections.Generic.List`1[System.String]>
 -Protocol <System.Collections.Generic.List`1[System.String]> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00d07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00d07-105">DESCRIPTION</span></span>
<span data-ttu-id="00d07-106">**Yeni-AzureRmFirewallNatRule** cmdlet 'ı, Azure Güvenlik Duvarı IÇIN bir NAT kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00d07-106">The **New-AzureRmFirewallNatRule** cmdlet creates a NAT rule for Azure Firewall.</span></span>

## <span data-ttu-id="00d07-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00d07-107">EXAMPLES</span></span>

### <span data-ttu-id="00d07-108">1: hedef 10.1.2.3 ile 10.0.0.0/24 adresinden tüm TCP trafiğine yönelik bir kural oluşturun.</span><span class="sxs-lookup"><span data-stu-id="00d07-108">1:  Create a rule to DNAT all TCP traffic from 10.0.0.0/24 with destination 10.1.2.3:80 to destination 10.4.5.6:8080</span></span>
```
New-AzureRmFirewallNatRule -Name "dnat-rule" -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.1.2.3" -DestinationPort "80" -TranslatedAddress "10.4.5.6" -TranslatedPort "8080"
```

<span data-ttu-id="00d07-109">Bu örnek, hedef 10.1.2.3 ile 10.0.0.0/24 ile gelen tüm trafikten bir kural oluşturur: 10.4.5.6:8080</span><span class="sxs-lookup"><span data-stu-id="00d07-109">This example creates a rule which will DNAT all traffic originating in 10.0.0.0/24 with destination 10.1.2.3:80 to 10.4.5.6:8080</span></span>

## <span data-ttu-id="00d07-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00d07-110">PARAMETERS</span></span>

### <span data-ttu-id="00d07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d07-111">-DefaultProfile</span></span>
<span data-ttu-id="00d07-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00d07-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00d07-113">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="00d07-113">-Description</span></span>
<span data-ttu-id="00d07-114">Bu kural için isteğe bağlı bir açıklama belirtin.</span><span class="sxs-lookup"><span data-stu-id="00d07-114">Specifies an optional description of this rule.</span></span>

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

### <span data-ttu-id="00d07-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="00d07-115">-DestinationAddress</span></span>
<span data-ttu-id="00d07-116">Kuralın hedef adresleri.</span><span class="sxs-lookup"><span data-stu-id="00d07-116">The destination addresses of the rule.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d07-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="00d07-117">-DestinationPort</span></span>
<span data-ttu-id="00d07-118">Kuralın hedef bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="00d07-118">The destination ports of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d07-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="00d07-119">-Name</span></span>
<span data-ttu-id="00d07-120">Bu NAT kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00d07-120">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="00d07-121">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="00d07-121">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="00d07-122">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="00d07-122">-Protocol</span></span>
<span data-ttu-id="00d07-123">Bu kurala göre filtre uygulanacak trafik türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="00d07-123">Specifies the type of traffic to be filtered by this rule.</span></span>
<span data-ttu-id="00d07-124">Desteklenen protokoller TCP ve UDP.</span><span class="sxs-lookup"><span data-stu-id="00d07-124">The supported protocols are TCP and UDP.</span></span>
<span data-ttu-id="00d07-125">"Herhangi" özel bir değere izin verilir, anlamı hem TCP hem de UDP ile eşleşir, ancak başka protokoller içermez.</span><span class="sxs-lookup"><span data-stu-id="00d07-125">A special value "Any" is allowed, meaning it will match both TCP and UDP, but no other protocols.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:
Accepted values: Any, TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d07-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="00d07-126">-SourceAddress</span></span>
<span data-ttu-id="00d07-127">Kuralın kaynak adresleri</span><span class="sxs-lookup"><span data-stu-id="00d07-127">The source addresses of the rule</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d07-128">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="00d07-128">-TranslatedAddress</span></span>
<span data-ttu-id="00d07-129">Adres çevirisinin istenilen sonucunu belirtir</span><span class="sxs-lookup"><span data-stu-id="00d07-129">Specifies the desired result of the address translation</span></span>

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

### <span data-ttu-id="00d07-130">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="00d07-130">-TranslatedPort</span></span>
<span data-ttu-id="00d07-131">Bağlantı noktası çevirisinin istenilen sonucunu belirtir</span><span class="sxs-lookup"><span data-stu-id="00d07-131">Specifies the desired result of the port translation</span></span>

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

### <span data-ttu-id="00d07-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="00d07-132">-Confirm</span></span>
<span data-ttu-id="00d07-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00d07-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00d07-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00d07-134">-WhatIf</span></span>
<span data-ttu-id="00d07-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00d07-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00d07-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00d07-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00d07-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d07-137">CommonParameters</span></span>
<span data-ttu-id="00d07-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00d07-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d07-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d07-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d07-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00d07-140">INPUTS</span></span>

### <span data-ttu-id="00d07-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="00d07-141">None</span></span>
<span data-ttu-id="00d07-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="00d07-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00d07-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00d07-143">OUTPUTS</span></span>

### <span data-ttu-id="00d07-144">Microsoft. Azure. Commands. Network. modeller. PSFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="00d07-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRule</span></span>

## <span data-ttu-id="00d07-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00d07-145">NOTES</span></span>

## <span data-ttu-id="00d07-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00d07-146">RELATED LINKS</span></span>

[<span data-ttu-id="00d07-147">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="00d07-147">New-AzureRmFirewallNatRuleCollection</span></span>](./New-AzureRmFirewallNatRuleCollection.md)

[<span data-ttu-id="00d07-148">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="00d07-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="00d07-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="00d07-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
