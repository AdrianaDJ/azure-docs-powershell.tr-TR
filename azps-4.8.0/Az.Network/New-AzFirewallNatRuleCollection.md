---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallnatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallNatRuleCollection.md
ms.openlocfilehash: 4ba57fd922319eb2be6ba001c723b3e668bce59e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274848"
---
# <span data-ttu-id="eaec6-101">New-AzFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="eaec6-101">New-AzFirewallNatRuleCollection</span></span>

## <span data-ttu-id="eaec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaec6-102">SYNOPSIS</span></span>
<span data-ttu-id="eaec6-103">Güvenlik Duvarı NAT kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eaec6-103">Creates a collection of Firewall NAT rules.</span></span>

## <span data-ttu-id="eaec6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eaec6-104">SYNTAX</span></span>

```
New-AzFirewallNatRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallNatRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaec6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eaec6-105">DESCRIPTION</span></span>
<span data-ttu-id="eaec6-106">**New-AzFirewallNatRuleCollection** cmdlet 'ı, GÜVENLIK duvarı NAT kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eaec6-106">The **New-AzFirewallNatRuleCollection** cmdlet creates a collection of Firewall NAT Rules.</span></span>

## <span data-ttu-id="eaec6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eaec6-107">EXAMPLES</span></span>

### <span data-ttu-id="eaec6-108">Örnek 1: tek bir kuralla koleksiyon oluşturma</span><span class="sxs-lookup"><span data-stu-id="eaec6-108">Example 1: Create a collection with one rule</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name "natRule" -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 1000 -Rule $rule1
```

<span data-ttu-id="eaec6-109">Bu örnek bir kural içeren bir koleksiyon oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eaec6-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="eaec6-110">$Rule 1 ' de belirtilen koşullara uyan tüm trafik, çevrilmiş adres ve bağlantı noktasına dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="eaec6-110">All traffic that matches the conditions identified in $rule1 will be DNAT'ed to translated address and port.</span></span>

### <span data-ttu-id="eaec6-111">Örnek 2: kural koleksiyonuna kural ekleme</span><span class="sxs-lookup"><span data-stu-id="eaec6-111">Example 2: Add a rule to a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="eaec6-112">Bu örnekte, bir kuralla yeni bir NAT kural koleksiyonu oluşturulur ve kural koleksiyonu nesnesinde yöntem AddRule kullanarak kural koleksiyonuna ikinci bir kural eklenir.</span><span class="sxs-lookup"><span data-stu-id="eaec6-112">This example creates a new NAT rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="eaec6-113">Verilen bir kural koleksiyonundaki her kuralın adı benzersiz olmalıdır ve büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="eaec6-113">Each rule name in a given rule collection must have an unique name and is case insensitive.</span></span>

### <span data-ttu-id="eaec6-114">Örnek 3: kural koleksiyonundan kural alma</span><span class="sxs-lookup"><span data-stu-id="eaec6-114">Example 3: Get a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "TCP" -SourceAddress "10.0.0.0/24" -DestinationAddress "10.0.1.0/24" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1

$rule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="eaec6-115">Bu örnek, bir kuralla yeni bir NAT kural koleksiyonu oluşturur ve kuralı adı, kural koleksiyonu nesnesinde GetRuleByName yöntemini arayan kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="eaec6-115">This example creates a new NAT rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="eaec6-116">GetRuleByName metodunun kural adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="eaec6-116">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="eaec6-117">Örnek 4: kural koleksiyonundan kural kaldırma</span><span class="sxs-lookup"><span data-stu-id="eaec6-117">Example 4: Remove a rule from a rule collection</span></span>
```powershell
$rule1 = New-AzFirewallNatRule -Name R1 -Protocol "UDP","TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "80" -TranslatedAddress "10.0.0.2" -TranslatedPort "8080"
$rule2 = New-AzFirewallNatRule -Name R2 -Protocol "TCP" -SourceAddress "*" -DestinationAddress "10.0.0.1" -DestinationPort "443" -TranslatedAddress "10.0.0.2" -TranslatedPort "8443"
$ruleCollection = New-AzFirewallNatRuleCollection -Name "MyNatRuleCollection" -Priority 100 -Rule $rule1, $rule2
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="eaec6-118">Bu örnekte, iki kural içeren yeni bir NAT kural koleksiyonu oluşturulur ve kural koleksiyonundaki ilk kuralı kural koleksiyonu nesnesinde yöntemi çağırarak kural koleksiyonundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="eaec6-118">This example creates a new NAT rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="eaec6-119">Yöntem için kural adı, büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="eaec6-119">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="eaec6-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eaec6-120">PARAMETERS</span></span>

### <span data-ttu-id="eaec6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaec6-121">-DefaultProfile</span></span>
<span data-ttu-id="eaec6-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eaec6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaec6-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="eaec6-123">-Name</span></span>
<span data-ttu-id="eaec6-124">Bu NAT kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaec6-124">Specifies the name of this NAT rule.</span></span> <span data-ttu-id="eaec6-125">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="eaec6-125">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="eaec6-126">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="eaec6-126">-Priority</span></span>
<span data-ttu-id="eaec6-127">Bu kuralın önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaec6-127">Specifies the priority of this rule.</span></span> <span data-ttu-id="eaec6-128">Öncelik, 100 ve 65000 arasındaki bir sayıdır.</span><span class="sxs-lookup"><span data-stu-id="eaec6-128">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="eaec6-129">Sayı ne kadar küçükse öncelik o kadar büyük olur.</span><span class="sxs-lookup"><span data-stu-id="eaec6-129">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="eaec6-130">-Kural</span><span class="sxs-lookup"><span data-stu-id="eaec6-130">-Rule</span></span>
<span data-ttu-id="eaec6-131">Bu koleksiyon altında Gruplanacak kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eaec6-131">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaec6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="eaec6-132">-Confirm</span></span>
<span data-ttu-id="eaec6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eaec6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaec6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaec6-134">-WhatIf</span></span>
<span data-ttu-id="eaec6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eaec6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaec6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eaec6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaec6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaec6-137">CommonParameters</span></span>
<span data-ttu-id="eaec6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eaec6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaec6-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaec6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaec6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eaec6-140">INPUTS</span></span>

### <span data-ttu-id="eaec6-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eaec6-141">None</span></span>

## <span data-ttu-id="eaec6-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eaec6-142">OUTPUTS</span></span>

### <span data-ttu-id="eaec6-143">Microsoft. Azure. Commands. Network. model. Psazurelecollection</span><span class="sxs-lookup"><span data-stu-id="eaec6-143">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNatRuleCollection</span></span>

## <span data-ttu-id="eaec6-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eaec6-144">NOTES</span></span>

## <span data-ttu-id="eaec6-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eaec6-145">RELATED LINKS</span></span>

[<span data-ttu-id="eaec6-146">Yeni-AzFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="eaec6-146">New-AzFirewallNatRule</span></span>](./New-AzFirewallNatRule.md)

[<span data-ttu-id="eaec6-147">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eaec6-147">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="eaec6-148">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="eaec6-148">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
