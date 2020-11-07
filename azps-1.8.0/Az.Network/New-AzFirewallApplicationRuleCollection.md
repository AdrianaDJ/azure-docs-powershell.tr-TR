---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallApplicationRuleCollection.md
ms.openlocfilehash: 2c88e38bba0b4242ff0b268936fbe246214d1921
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760342"
---
# <span data-ttu-id="3dccd-101">New-AzFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3dccd-101">New-AzFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="3dccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dccd-102">SYNOPSIS</span></span>
<span data-ttu-id="3dccd-103">Güvenlik Duvarı uygulama kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3dccd-103">Creates a collection of Firewall application rules.</span></span>

## <span data-ttu-id="3dccd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3dccd-104">SYNTAX</span></span>

```
New-AzFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallApplicationRule[]> -ActionType <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dccd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3dccd-105">DESCRIPTION</span></span>
<span data-ttu-id="3dccd-106">**New-AzFirewallApplicationRuleCollection** cmdlet 'ı bir güvenlik duvarı uygulaması kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3dccd-106">The **New-AzFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="3dccd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3dccd-107">EXAMPLES</span></span>

### <span data-ttu-id="3dccd-108">1: tek kuralla koleksiyon oluşturma</span><span class="sxs-lookup"><span data-stu-id="3dccd-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="3dccd-109">Bu örnek bir kural içeren bir koleksiyon oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3dccd-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="3dccd-110">$Rule 1 ' de belirtilen koşullara uyan tüm trafiğe izin verilir.</span><span class="sxs-lookup"><span data-stu-id="3dccd-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="3dccd-111">İlk kural, 10.0.0.0 ile bağlantı noktası 443 üzerindeki tüm HTTPS trafiği içindir.</span><span class="sxs-lookup"><span data-stu-id="3dccd-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="3dccd-112">Daha yüksek önceliğe sahip başka bir uygulama kuralı koleksiyonu varsa $rule 1 ' de tanımlanan trafikle de eşleşir; bunun yerine, kural koleksiyonunun yüksek önceliğe sahip eylemi geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3dccd-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="3dccd-113">2: kural koleksiyonuna kural ekleme</span><span class="sxs-lookup"><span data-stu-id="3dccd-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="3dccd-114">Bu örnek, bir kuralla yeni bir uygulama kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntem AddRule kullanarak kural koleksiyonuna ikinci bir kural ekler.</span><span class="sxs-lookup"><span data-stu-id="3dccd-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="3dccd-115">Verilen bir kural koleksiyonundaki her kuralın adı benzersiz olmalıdır ve büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="3dccd-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="3dccd-116">3: kural koleksiyonundan kural alma</span><span class="sxs-lookup"><span data-stu-id="3dccd-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="3dccd-117">Bu örnek, bir kuralla yeni bir uygulama kuralı koleksiyonu oluşturur ve kuralı adı, kural koleksiyonu nesnesinde GetRuleByName yöntemini arayan kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="3dccd-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="3dccd-118">GetRuleByName metodunun kural adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="3dccd-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="3dccd-119">4: kural koleksiyonundan kural kaldırma</span><span class="sxs-lookup"><span data-stu-id="3dccd-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="3dccd-120">Bu örnekte, iki kural içeren yeni bir uygulama kuralı koleksiyonu oluşturulur ve kural koleksiyonu nesnesinde yöntemi çağırarak kural koleksiyonundan ilk kuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3dccd-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="3dccd-121">Yöntem için kural adı, büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="3dccd-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="3dccd-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3dccd-122">PARAMETERS</span></span>

### <span data-ttu-id="3dccd-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="3dccd-123">-ActionType</span></span>
<span data-ttu-id="3dccd-124">Kural koleksiyonunun eylemi</span><span class="sxs-lookup"><span data-stu-id="3dccd-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="3dccd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dccd-125">-DefaultProfile</span></span>
<span data-ttu-id="3dccd-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3dccd-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dccd-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="3dccd-127">-Name</span></span>
<span data-ttu-id="3dccd-128">Bu uygulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dccd-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="3dccd-129">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3dccd-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="3dccd-130">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="3dccd-130">-Priority</span></span>
<span data-ttu-id="3dccd-131">Bu kuralın önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dccd-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="3dccd-132">Öncelik, 100 ve 65000 arasındaki bir sayıdır.</span><span class="sxs-lookup"><span data-stu-id="3dccd-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="3dccd-133">Sayı ne kadar küçükse öncelik o kadar büyük olur.</span><span class="sxs-lookup"><span data-stu-id="3dccd-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="3dccd-134">-Kural</span><span class="sxs-lookup"><span data-stu-id="3dccd-134">-Rule</span></span>
<span data-ttu-id="3dccd-135">Bu koleksiyon altında Gruplanacak kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3dccd-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dccd-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="3dccd-136">-Confirm</span></span>
<span data-ttu-id="3dccd-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3dccd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dccd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dccd-138">-WhatIf</span></span>
<span data-ttu-id="3dccd-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3dccd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dccd-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3dccd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dccd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dccd-141">CommonParameters</span></span>
<span data-ttu-id="3dccd-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3dccd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dccd-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dccd-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dccd-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3dccd-144">INPUTS</span></span>

### <span data-ttu-id="3dccd-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3dccd-145">None</span></span>

## <span data-ttu-id="3dccd-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3dccd-146">OUTPUTS</span></span>

### <span data-ttu-id="3dccd-147">Microsoft. Azure. Commands. Network. model. PSAzureFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="3dccd-147">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="3dccd-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3dccd-148">NOTES</span></span>

## <span data-ttu-id="3dccd-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3dccd-149">RELATED LINKS</span></span>

[<span data-ttu-id="3dccd-150">New-AzFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="3dccd-150">New-AzFirewallApplicationRule</span></span>](./New-AzFirewallApplicationRule.md)

[<span data-ttu-id="3dccd-151">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3dccd-151">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="3dccd-152">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="3dccd-152">Get-AzFirewall</span></span>](./Get-AzFirewall.md)
