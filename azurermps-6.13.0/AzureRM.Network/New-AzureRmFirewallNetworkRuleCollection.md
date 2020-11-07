---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnetworkrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNetworkRuleCollection.md
ms.openlocfilehash: 79ead5ac618b4631c3ec790156fe1a75e4169882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591353"
---
# <span data-ttu-id="ce61a-101">New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce61a-101">New-AzureRmFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="ce61a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce61a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce61a-103">Ağ kuralları için bir Azure Güvenlik Duvarı ağ koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ce61a-103">Creates a Azure Firewall Network Collection of Network rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce61a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce61a-104">SYNTAX</span></span>

```
New-AzureRmFirewallNetworkRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce61a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce61a-105">DESCRIPTION</span></span>
<span data-ttu-id="ce61a-106">**New-AzureRmFirewallNetworkRuleCollection** cmdlet 'ı, güvenlik duvarı ağ kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ce61a-106">The **New-AzureRmFirewallNetworkRuleCollection** cmdlet creates a collection of Firewall Network Rules.</span></span>

## <span data-ttu-id="ce61a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce61a-107">EXAMPLES</span></span>

### <span data-ttu-id="ce61a-108">1: iki kuralla bir ağ koleksiyonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="ce61a-108">1:  Create a network collection with two rules</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
New-AzureRmFirewallNetworkRuleCollection -Name RC1 -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
```

<span data-ttu-id="ce61a-109">Bu örnek, iki kuralla eşleşen tüm trafiğe izin verecek bir koleksiyon oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ce61a-109">This example creates a collection which will allow all traffic that matches either of the two rules.</span></span>
<span data-ttu-id="ce61a-110">İlk kural tüm UDP trafiği içindir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-110">The first rule is for all UDP traffic.</span></span>
<span data-ttu-id="ce61a-111">İkinci kural, 10.0.0.0 'den 60.1.5.0:4040 'e giden TCP trafiğine yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-111">The second rule is for TCP traffic from 10.0.0.0 to 60.1.5.0:4040.</span></span>
<span data-ttu-id="ce61a-112">Aynı zamanda $rule 1 veya $rule 2 ' de tanımlanan trafikle eşleşen daha yüksek önceliğe sahip bir ağ kuralı koleksiyonu varsa, kural koleksiyonunun yüksek önceliğe sahip olan eylemi geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ce61a-112">If there is another Network rule collection with higher priority (smaller number) which also matches traffic identified in $rule1 or $rule2, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="ce61a-113">2: kural koleksiyonuna kural ekleme</span><span class="sxs-lookup"><span data-stu-id="ce61a-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="ce61a-114">Bu örnek, bir kuralla yeni bir ağ kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntem AddRule kullanarak kural koleksiyonuna ikinci bir kural ekler.</span><span class="sxs-lookup"><span data-stu-id="ce61a-114">This example creates a new network rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="ce61a-115">Verilen bir kural koleksiyonundaki her kuralın adı benzersiz olmalıdır ve büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="ce61a-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="ce61a-116">3: kural koleksiyonundan kural alma</span><span class="sxs-lookup"><span data-stu-id="ce61a-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("ALL-UDP-traffic")
```

<span data-ttu-id="ce61a-117">Bu örnek, bir kuralla yeni bir ağ kuralı koleksiyonu oluşturur ve kuralı adı, kural koleksiyonu nesnesinde GetRuleByName yöntemini arayan kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="ce61a-117">This example creates a new network rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="ce61a-118">GetRuleByName metodunun kural adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="ce61a-119">4: kural koleksiyonundan kural kaldırma</span><span class="sxs-lookup"><span data-stu-id="ce61a-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol UDP -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$rule2 = New-AzureRmFirewallNetworkRule -Name "partial-tcp-rule" -Description "Rule for all TCP traffic from 10.0.0.0 to 60.1.5.0:4040" -Protocol TCP -SourceAddress "10.0.0.0" -DestinationAddress "60.1.5.0" -DestinationPort "4040"
$ruleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $rule1, $rule2 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("ALL-udp-traffic")
```

<span data-ttu-id="ce61a-120">Bu örnek, iki kural içeren yeni bir ağ kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntemi çağırarak kural koleksiyonundan ilk kuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce61a-120">This example creates a new network rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="ce61a-121">Yöntem için kural adı, büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="ce61a-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce61a-122">PARAMETERS</span></span>

### <span data-ttu-id="ce61a-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="ce61a-123">-ActionType</span></span>
<span data-ttu-id="ce61a-124">Bu kuralın trafik eşleştirme koşullarıyla gerçekleştirilecek eylemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-124">Specifies the action to be taken for traffic matching conditions of this rule.</span></span> <span data-ttu-id="ce61a-125">Kabul edilen eylemler "Izin ver" veya "Reddet".</span><span class="sxs-lookup"><span data-stu-id="ce61a-125">Accepted actions are "Allow" or "Deny".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce61a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce61a-126">-DefaultProfile</span></span>
<span data-ttu-id="ce61a-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce61a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce61a-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce61a-128">-Name</span></span>
<span data-ttu-id="ce61a-129">Bu ağ kuralı koleksiyonunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-129">Specifies the name of this network rule collection.</span></span> <span data-ttu-id="ce61a-130">Ad tüm ağ kuralı koleksiyonunda benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ce61a-130">The name must be unique across all network rule collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce61a-131">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="ce61a-131">-Priority</span></span>
<span data-ttu-id="ce61a-132">Bu kural koleksiyonunun önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-132">Specifies the priority of this rule collection.</span></span> <span data-ttu-id="ce61a-133">Öncelik, 100 ve 65000 arasındaki bir sayıdır.</span><span class="sxs-lookup"><span data-stu-id="ce61a-133">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="ce61a-134">Sayı ne kadar küçükse, öncelik o kadar yüksektir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-134">The smaller the number, the higher the priority.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce61a-135">-Kural</span><span class="sxs-lookup"><span data-stu-id="ce61a-135">-Rule</span></span>
<span data-ttu-id="ce61a-136">Bu koleksiyon altında Gruplanacak kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-136">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce61a-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce61a-137">-Confirm</span></span>
<span data-ttu-id="ce61a-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce61a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce61a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce61a-139">-WhatIf</span></span>
<span data-ttu-id="ce61a-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce61a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce61a-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce61a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce61a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce61a-142">CommonParameters</span></span>
<span data-ttu-id="ce61a-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce61a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce61a-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce61a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce61a-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce61a-145">INPUTS</span></span>

### <span data-ttu-id="ce61a-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ce61a-146">None</span></span>
<span data-ttu-id="ce61a-147">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ce61a-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce61a-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce61a-148">OUTPUTS</span></span>

### <span data-ttu-id="ce61a-149">Microsoft. Azure. Commands. Network. model. PSFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="ce61a-149">Microsoft.Azure.Commands.Network.Models.PSFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="ce61a-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce61a-150">NOTES</span></span>

## <span data-ttu-id="ce61a-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce61a-151">RELATED LINKS</span></span>

[<span data-ttu-id="ce61a-152">Yeni-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce61a-152">New-AzureRmFirewallNetworkRule</span></span>](./New-AzureRmFirewallNetworkRule.md)

[<span data-ttu-id="ce61a-153">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce61a-153">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="ce61a-154">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="ce61a-154">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)