---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 231787f57061ff4e118510c3dc166915b39da436
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589716"
---
# <span data-ttu-id="2942a-101">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2942a-101">Get-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="2942a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2942a-102">SYNOPSIS</span></span>
<span data-ttu-id="2942a-103">Redis Cache 'de güvenlik duvarı kuralları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2942a-103">Get firewall rules set on Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2942a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2942a-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2942a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2942a-105">DESCRIPTION</span></span>
<span data-ttu-id="2942a-106">If **RuleName** parametresi sağlanmışsa, **Get-AzureRmRedisCacheFirewallRule** cmdlet 'ı Azure Redis Cache 'de belirtilen güvenlik duvarı kuralı hakkında ayrıntılı bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="2942a-106">If **RuleName** parameter if provided, **Get-AzureRmRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="2942a-107">Yalnızca **ad** belirtilirse, bu, bu Red</span><span class="sxs-lookup"><span data-stu-id="2942a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="2942a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2942a-108">EXAMPLES</span></span>

### <span data-ttu-id="2942a-109">Örnek 1: tek bir güvenlik duvarı kuralı edinin</span><span class="sxs-lookup"><span data-stu-id="2942a-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="2942a-110">Bu komut myCache adlı Red, Cache 'den Rule adlı güvenlik duvarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="2942a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="2942a-111">Örnek 2: tüm güvenlik duvarı kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="2942a-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzureRmRedisCacheFirewallRule -Name "mycache"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruletwo
        RuleName          : ruletwo
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.33
        EndIP             : 10.0.0.64
```

<span data-ttu-id="2942a-112">Bu komut myCache adındaki tüm güvenlik duvarı kurallarını Redcache 'den alır.</span><span class="sxs-lookup"><span data-stu-id="2942a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="2942a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2942a-113">PARAMETERS</span></span>

### <span data-ttu-id="2942a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2942a-114">-DefaultProfile</span></span>
<span data-ttu-id="2942a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2942a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2942a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="2942a-116">-Name</span></span>
<span data-ttu-id="2942a-117">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="2942a-117">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2942a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2942a-118">-ResourceGroupName</span></span>
<span data-ttu-id="2942a-119">Önbelleğin olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2942a-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2942a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="2942a-120">-RuleName</span></span>
<span data-ttu-id="2942a-121">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="2942a-121">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2942a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2942a-122">CommonParameters</span></span>
<span data-ttu-id="2942a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2942a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2942a-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2942a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2942a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2942a-125">INPUTS</span></span>

### <span data-ttu-id="2942a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2942a-126">System.String</span></span>
<span data-ttu-id="2942a-127">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2942a-127">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="2942a-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2942a-128">OUTPUTS</span></span>

### <span data-ttu-id="2942a-129">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. RedisCache. modeller. PSRedisFirewallRule, Microsoft. Azure. Commands. RedisCache, Version = 4.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2942a-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule, Microsoft.Azure.Commands.RedisCache, Version=4.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2942a-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2942a-130">NOTES</span></span>

## <span data-ttu-id="2942a-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2942a-131">RELATED LINKS</span></span>

[<span data-ttu-id="2942a-132">Yeni-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2942a-132">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="2942a-133">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2942a-133">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="2942a-134">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2942a-134">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="2942a-135">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2942a-135">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="2942a-136">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2942a-136">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="2942a-137">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2942a-137">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
