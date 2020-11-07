---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNetworkRuleCollection.md
ms.openlocfilehash: af0a81cf915cd853bfc8ca957d706cdb45d96180
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760334"
---
# <span data-ttu-id="afdb0-101">New-AzFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="afdb0-101">New-AzFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="afdb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afdb0-102">SYNOPSIS</span></span>
<span data-ttu-id="afdb0-103">Ağ kuralları için bir Azure Güvenlik Duvarı ağ koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afdb0-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

## <span data-ttu-id="afdb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afdb0-104">SYNTAX</span></span>

```
New-AzFirewallNetworkRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNetworkRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afdb0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="afdb0-105">DESCRIPTION</span></span>
<span data-ttu-id="afdb0-106">**New-AzFirewallNetworkRuleCollection** cmdlet 'ı, güvenlik duvarı ağ kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afdb0-106">The **New-AzFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="afdb0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afdb0-107">EXAMPLES</span></span>

### <span data-ttu-id="afdb0-108">1: iki kuralla bir ağ koleksiyonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="afdb0-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="afdb0-109">Bu örnek, iki kuralla eşleşen tüm trafiğe izin verecek bir koleksiyon oluşturur.</span><span class="sxs-lookup"><span data-stu-id="afdb0-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="afdb0-110">İlk kural tüm UDP trafiği içindir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="afdb0-111">İkinci kural, 10.0.0.0 'den 60.1.5.0:4040 'e giden TCP trafiğine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="afdb0-112">Aynı zamanda $rule 1 veya $rule 2 ' de tanımlanan trafikle eşleşen daha yüksek önceliğe sahip bir ağ kuralı koleksiyonu varsa, kural koleksiyonunun yüksek önceliğe sahip olan eylemi geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="afdb0-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="afdb0-113">2: kural koleksiyonuna kural ekleme</span><span class="sxs-lookup"><span data-stu-id="afdb0-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="afdb0-114">Bu örnek, bir kuralla yeni bir ağ kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntem AddRule kullanarak kural koleksiyonuna ikinci bir kural ekler.</span><span class="sxs-lookup"><span data-stu-id="afdb0-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="afdb0-115">Verilen bir kural koleksiyonundaki her kuralın adı benzersiz olmalıdır ve büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="afdb0-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="afdb0-116">3: kural koleksiyonundan kural alma</span><span class="sxs-lookup"><span data-stu-id="afdb0-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="afdb0-117">Bu örnek, bir kuralla yeni bir ağ kuralı koleksiyonu oluşturur ve kuralı adı, kural koleksiyonu nesnesinde GetRuleByName yöntemini arayan kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="afdb0-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="afdb0-118">GetRuleByName metodunun kural adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="afdb0-119">4: kural koleksiyonundan kural kaldırma</span><span class="sxs-lookup"><span data-stu-id="afdb0-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="afdb0-120">Bu örnek, iki kural içeren yeni bir ağ kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntemi çağırarak kural koleksiyonundan ilk kuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="afdb0-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="afdb0-121">Yöntem için kural adı, büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="afdb0-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afdb0-122">PARAMETERS</span></span>

### <span data-ttu-id="afdb0-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="afdb0-123">-ActionType</span></span>
<span data-ttu-id="afdb0-124">Bu kuralın trafik eşleştirme koşullarıyla gerçekleştirilecek eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="afdb0-125">Kabul edilen eylemler "Izin ver" veya "Reddet".</span><span class="sxs-lookup"><span data-stu-id="afdb0-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdb0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afdb0-126">-DefaultProfile</span></span>
<span data-ttu-id="afdb0-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afdb0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afdb0-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="afdb0-128">-Name</span></span>
<span data-ttu-id="afdb0-129">Bu ağ kuralı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="afdb0-130">Ad tüm ağ kuralı koleksiyonunda benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="afdb0-130">The name must be unique across all network rule collection.</span></span>

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

### <span data-ttu-id="afdb0-131">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="afdb0-131">-Priority</span></span>
<span data-ttu-id="afdb0-132">Bu kural koleksiyonunun önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="afdb0-133">Öncelik, 100 ve 65000 arasındaki bir sayıdır.</span><span class="sxs-lookup"><span data-stu-id="afdb0-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="afdb0-134">Sayı ne kadar küçükse, öncelik o kadar yüksektir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdb0-135">-Kural</span><span class="sxs-lookup"><span data-stu-id="afdb0-135">-Rule</span></span>
<span data-ttu-id="afdb0-136">Bu koleksiyon altında Gruplanacak kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afdb0-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="afdb0-137">-Confirm</span></span>
<span data-ttu-id="afdb0-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="afdb0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afdb0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afdb0-139">-WhatIf</span></span>
<span data-ttu-id="afdb0-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afdb0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afdb0-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="afdb0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afdb0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afdb0-142">CommonParameters</span></span>
<span data-ttu-id="afdb0-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afdb0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afdb0-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afdb0-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afdb0-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afdb0-145">INPUTS</span></span>

### <span data-ttu-id="afdb0-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="afdb0-146">None</span></span>

## <span data-ttu-id="afdb0-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afdb0-147">OUTPUTS</span></span>

### <span data-ttu-id="afdb0-148">Microsoft. Azure. Commands. Network. model. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="afdb0-148">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="afdb0-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afdb0-149">NOTES</span></span>

## <span data-ttu-id="afdb0-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afdb0-150">RELATED LINKS</span></span>

[<span data-ttu-id="afdb0-151">Yeni-AzFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="afdb0-151">New-AzFirewallNetworkRule</span></span>](./New-AzFirewallNetworkRule.md)

[<span data-ttu-id="afdb0-152">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="afdb0-152">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="afdb0-153">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="afdb0-153">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
