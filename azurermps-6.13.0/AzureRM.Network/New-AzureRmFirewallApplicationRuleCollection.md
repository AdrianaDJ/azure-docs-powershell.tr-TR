---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A29E9921-C1B9-42C2-B816-5D4873AC6688
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermfirewallapplicationrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmFirewallApplicationRuleCollection.md
ms.openlocfilehash: e5fbad2b63213af972260948439984754e9eaa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764615"
---
# <span data-ttu-id="4fc3f-101">New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4fc3f-101">New-AzureRmFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="4fc3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc3f-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc3f-103">Güvenlik Duvarı uygulama kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-103">Creates a collection of Firewall application rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fc3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4fc3f-104">SYNTAX</span></span>

```
New-AzureRmFirewallApplicationRuleCollection -Name <String> -Priority <UInt32>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4fc3f-105">DESCRIPTION</span></span>
<span data-ttu-id="4fc3f-106">**New-AzureRmFirewallApplicationRuleCollection** cmdlet 'ı, güvenlik duvarı uygulama kuralları koleksiyonu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-106">The **New-AzureRmFirewallApplicationRuleCollection** cmdlet creates a collection of Firewall Application Rules.</span></span>

## <span data-ttu-id="4fc3f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4fc3f-107">EXAMPLES</span></span>

### <span data-ttu-id="4fc3f-108">1: tek kuralla koleksiyon oluşturma</span><span class="sxs-lookup"><span data-stu-id="4fc3f-108">1:  Create a collection with one rule</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name "httpsRule" -Protocol "https:443" -TargetFqdn "*" -SourceAddress "10.0.0.0"
New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 1000 -Rule $rule1 -ActionType "Allow"
```

<span data-ttu-id="4fc3f-109">Bu örnek bir kural içeren bir koleksiyon oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-109">This example creates a collection with one rule.</span></span> <span data-ttu-id="4fc3f-110">$Rule 1 ' de belirtilen koşullara uyan tüm trafiğe izin verilir.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-110">All traffic that matches the conditions identified in $rule1 will be allowed.</span></span>
<span data-ttu-id="4fc3f-111">İlk kural, 10.0.0.0 ile bağlantı noktası 443 üzerindeki tüm HTTPS trafiği içindir.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-111">The first rule is for all HTTPS traffic on port 443 from 10.0.0.0.</span></span> <span data-ttu-id="4fc3f-112">Daha yüksek önceliğe sahip başka bir uygulama kuralı koleksiyonu varsa $rule 1 ' de tanımlanan trafikle de eşleşir; bunun yerine, kural koleksiyonunun yüksek önceliğe sahip eylemi geçerli olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-112">If there is another application rule collection with higher priority (smaller number) which also matches traffic identified in $rule1, the action of the rule collection with higher priority will take in effect instead.</span></span> 

### <span data-ttu-id="4fc3f-113">2: kural koleksiyonuna kural ekleme</span><span class="sxs-lookup"><span data-stu-id="4fc3f-113">2:  Add a rule to a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"

$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection.AddRule($rule2)
```

<span data-ttu-id="4fc3f-114">Bu örnek, bir kuralla yeni bir uygulama kuralı koleksiyonu oluşturur ve ardından kural koleksiyonu nesnesinde yöntem AddRule kullanarak kural koleksiyonuna ikinci bir kural ekler.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-114">This example creates a new application rule collection with one rule and then adds a second rule to the rule collection using method AddRule on the rule collection object.</span></span> <span data-ttu-id="4fc3f-115">Verilen bir kural koleksiyonundaki her kuralın adı benzersiz olmalıdır ve büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-115">Each rule name in a given rule collection must have a unique name and is case insensitive.</span></span>

### <span data-ttu-id="4fc3f-116">3: kural koleksiyonundan kural alma</span><span class="sxs-lookup"><span data-stu-id="4fc3f-116">3:  Get a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1 -ActionType "Allow"
$getRule=$ruleCollection.GetRuleByName("r1")
```

<span data-ttu-id="4fc3f-117">Bu örnek, bir kuralla yeni bir uygulama kuralı koleksiyonu oluşturur ve kuralı adı, kural koleksiyonu nesnesinde GetRuleByName yöntemini arayan kuralı alır.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-117">This example creates a new application rule collection with one rule and then gets the rule by name, calling method GetRuleByName on the rule collection object.</span></span> <span data-ttu-id="4fc3f-118">GetRuleByName metodunun kural adı büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-118">The rule name for method GetRuleByName is case-insensitive.</span></span>

### <span data-ttu-id="4fc3f-119">4: kural koleksiyonundan kural kaldırma</span><span class="sxs-lookup"><span data-stu-id="4fc3f-119">4:  Remove a rule from a rule collection</span></span>
```
$rule1 = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$rule2 = New-AzureRmFirewallApplicationRule -Name R2 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" 
$ruleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $rule1, $rule1 -ActionType "Allow"
$ruleCollection.RemoveRuleByName("r1")
```

<span data-ttu-id="4fc3f-120">Bu örnekte, iki kural içeren yeni bir uygulama kuralı koleksiyonu oluşturulur ve kural koleksiyonu nesnesinde yöntemi çağırarak kural koleksiyonundan ilk kuralı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-120">This example creates a new application rule collection with two rules and then removes the first rule from the rule collection by calling method RemoveRuleByName on the rule collection object.</span></span> <span data-ttu-id="4fc3f-121">Yöntem için kural adı, büyük/küçük harf duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-121">The rule name for method RemoveRuleByName is case-insensitive.</span></span>

## <span data-ttu-id="4fc3f-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4fc3f-122">PARAMETERS</span></span>

### <span data-ttu-id="4fc3f-123">-ActionType</span><span class="sxs-lookup"><span data-stu-id="4fc3f-123">-ActionType</span></span>
<span data-ttu-id="4fc3f-124">Kural koleksiyonunun eylemi</span><span class="sxs-lookup"><span data-stu-id="4fc3f-124">The action of the rule collection</span></span>

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

### <span data-ttu-id="4fc3f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc3f-125">-DefaultProfile</span></span>
<span data-ttu-id="4fc3f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fc3f-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="4fc3f-127">-Name</span></span>
<span data-ttu-id="4fc3f-128">Bu uygulama kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-128">Specifies the name of this application rule.</span></span> <span data-ttu-id="4fc3f-129">Ad, bir kural koleksiyonunun içinde benzersiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-129">The name must be unique inside a rule collection.</span></span>

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

### <span data-ttu-id="4fc3f-130">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="4fc3f-130">-Priority</span></span>
<span data-ttu-id="4fc3f-131">Bu kuralın önceliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-131">Specifies the priority of this rule.</span></span> <span data-ttu-id="4fc3f-132">Öncelik, 100 ve 65000 arasındaki bir sayıdır.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-132">Priority is a number between 100 and 65000.</span></span> <span data-ttu-id="4fc3f-133">Sayı ne kadar küçükse öncelik o kadar büyük olur.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-133">The smaller the number, the bigger the priority.</span></span>

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

### <span data-ttu-id="4fc3f-134">-Kural</span><span class="sxs-lookup"><span data-stu-id="4fc3f-134">-Rule</span></span>
<span data-ttu-id="4fc3f-135">Bu koleksiyon altında Gruplanacak kuralların listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-135">Specifies the list of rules to be grouped under this collection.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallApplicationRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc3f-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="4fc3f-136">-Confirm</span></span>
<span data-ttu-id="4fc3f-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fc3f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc3f-138">-WhatIf</span></span>
<span data-ttu-id="4fc3f-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc3f-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fc3f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc3f-141">CommonParameters</span></span>
<span data-ttu-id="4fc3f-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc3f-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc3f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc3f-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4fc3f-144">INPUTS</span></span>

### <span data-ttu-id="4fc3f-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4fc3f-145">None</span></span>
<span data-ttu-id="4fc3f-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4fc3f-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4fc3f-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4fc3f-147">OUTPUTS</span></span>

### <span data-ttu-id="4fc3f-148">Microsoft. Azure. Commands. Network. model. PSFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="4fc3f-148">Microsoft.Azure.Commands.Network.Models.PSFirewallApplicationRuleCollection</span></span>

## <span data-ttu-id="4fc3f-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4fc3f-149">NOTES</span></span>

## <span data-ttu-id="4fc3f-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4fc3f-150">RELATED LINKS</span></span>

[<span data-ttu-id="4fc3f-151">New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="4fc3f-151">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="4fc3f-152">Yeni-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4fc3f-152">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="4fc3f-153">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="4fc3f-153">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)
