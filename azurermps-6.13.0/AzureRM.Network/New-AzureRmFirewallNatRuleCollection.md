---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallNatRuleCollection.md
ms.openlocfilehash: 12b45dd5fd62dabb2650f121f52a539962315513
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588469"
---
# <span data-ttu-id="1b2cb-101">New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1b2cb-101">New-AzureRmFirewallNatRuleCollection</span></span>

## <span data-ttu-id="1b2cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2cb-103">Güvenlik Duvarı NAT kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-103">Creates a collection of Firewall NAT rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b2cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b2cb-104">SYNTAX</span></span>

```
New-AzureRmFirewallNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b2cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2cb-106">**Yeni-AzureRmFirewallNatRuleCollection** cmdlet 'ı, GÜVENLIK duvarı NAT kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-106">The **New-AzureRmFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="1b2cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b2cb-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2cb-108">1: tek kuralla koleksiyon oluşturma</span><span class="sxs-lookup"><span data-stu-id="1b2cb-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="1b2cb-109">Bu örnek bir kural içeren bir koleksiyon oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="1b2cb-110">$Rule 1 ' de belirtilen koşullara uyan tüm trafik, çevrilmiş adres ve bağlantı noktasına dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="1b2cb-111">2: kural koleksiyonuna kural ekleme</span><span class="sxs-lookup"><span data-stu-id="1b2cb-111">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="1b2cb-112">Bu örnekte, bir kuralla yeni bir NAT kural koleksiyonu oluşturulur ve kural koleksiyonu nesnesinde yöntem AddRule kullanarak kural koleksiyonuna ikinci bir kural eklenir.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="1b2cb-113">Verilen bir kural koleksiyonundaki her kuralın adı benzersiz olmalıdır ve büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="1b2cb-114">3: kural koleksiyonundan kural alma</span><span class="sxs-lookup"><span data-stu-id="1b2cb-114">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="1b2cb-115">Bu örnek, bir kuralla yeni bir NAT kural koleksiyonu oluşturur ve kuralı adı, kural koleksiyonu nesnesinde GetRuleByName yöntemini arayan kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="1b2cb-116">GetRuleByName metodunun kural adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="1b2cb-117">4: kural koleksiyonundan kural kaldırma</span><span class="sxs-lookup"><span data-stu-id="1b2cb-117">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzureRmFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzureRmFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="1b2cb-118">Bu örnekte, iki kural içeren yeni bir NAT kural koleksiyonu oluşturulur ve kural koleksiyonundaki ilk kuralı kural koleksiyonu nesnesinde yöntemi çağırarak kural koleksiyonundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="1b2cb-119">Yöntem için kural adı, büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="1b2cb-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b2cb-120">PARAMETERS</span></span>

### <span data-ttu-id="1b2cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2cb-121">-DefaultProfile</span></span>
<span data-ttu-id="1b2cb-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2cb-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b2cb-123">-Name</span></span>
<span data-ttu-id="1b2cb-124">Bu NAT kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="1b2cb-125">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="1b2cb-126">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="1b2cb-126">-Priority</span></span>
<span data-ttu-id="1b2cb-127">Bu kuralın önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="1b2cb-128">Öncelik, 100 ve 65000 arasındaki bir sayıdır.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="1b2cb-129">Sayı ne kadar küçükse öncelik o kadar büyük olur.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="1b2cb-130">-Kural</span><span class="sxs-lookup"><span data-stu-id="1b2cb-130">-Rule</span></span>
<span data-ttu-id="1b2cb-131">Bu koleksiyon altında Gruplanacak kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b2cb-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b2cb-132">-Confirm</span></span>
<span data-ttu-id="1b2cb-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b2cb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b2cb-134">-WhatIf</span></span>
<span data-ttu-id="1b2cb-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2cb-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b2cb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2cb-137">CommonParameters</span></span>
<span data-ttu-id="1b2cb-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2cb-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2cb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2cb-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b2cb-140">INPUTS</span></span>

### <span data-ttu-id="1b2cb-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1b2cb-141">None</span></span>
<span data-ttu-id="1b2cb-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="1b2cb-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b2cb-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b2cb-143">OUTPUTS</span></span>

### <span data-ttu-id="1b2cb-144">Microsoft. Azure. Commands. Network. model. PSFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="1b2cb-144">Microsoft.Azure.Commands.Network.Models.PSFirewallNatRuleCollection</span></span>

## <span data-ttu-id="1b2cb-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b2cb-145">NOTES</span></span>

## <span data-ttu-id="1b2cb-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b2cb-146">RELATED LINKS</span></span>

[<span data-ttu-id="1b2cb-147">Yeni-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="1b2cb-147">New-AzureRmFirewallNatRule</span></span>](./New-AzureRmFirewallNatRule.md)

[<span data-ttu-id="1b2cb-148">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1b2cb-148">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="1b2cb-149">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="1b2cb-149">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
