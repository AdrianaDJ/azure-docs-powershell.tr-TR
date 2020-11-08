---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 8e28951f826c5a049f345bb3182bda10e7de82fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098979"
---
# <span data-ttu-id="6752a-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6752a-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="6752a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6752a-102">SYNOPSIS</span></span>
<span data-ttu-id="6752a-103">Redis Cache 'de güvenlik duvarı kuralları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6752a-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="6752a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6752a-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6752a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6752a-105">DESCRIPTION</span></span>
<span data-ttu-id="6752a-106">If **RuleName** parametresi sağlanmışsa, **Get-AzRedisCacheFirewallRule** cmdlet 'ı, Azure Redis Cache 'de belirtilen güvenlik duvarı kuralı hakkında ayrıntılı bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="6752a-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="6752a-107">Yalnızca **ad** belirtilirse, bu, bu Red</span><span class="sxs-lookup"><span data-stu-id="6752a-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="6752a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6752a-108">EXAMPLES</span></span>

### <span data-ttu-id="6752a-109">Örnek 1: tek bir güvenlik duvarı kuralı edinin</span><span class="sxs-lookup"><span data-stu-id="6752a-109">Example 1: Get a single firewall rule</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="6752a-110">Bu komut myCache adlı Red, Cache 'den Rule adlı güvenlik duvarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="6752a-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="6752a-111">Örnek 2: tüm güvenlik duvarı kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="6752a-111">Example 2: Get all firewall rules</span></span>
```
PS C:\>Get-AzRedisCacheFirewallRule -Name "mycache"

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

<span data-ttu-id="6752a-112">Bu komut myCache adındaki tüm güvenlik duvarı kurallarını Redcache 'den alır.</span><span class="sxs-lookup"><span data-stu-id="6752a-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="6752a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6752a-113">PARAMETERS</span></span>

### <span data-ttu-id="6752a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6752a-114">-DefaultProfile</span></span>
<span data-ttu-id="6752a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6752a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6752a-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="6752a-116">-Name</span></span>
<span data-ttu-id="6752a-117">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="6752a-117">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6752a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6752a-118">-ResourceGroupName</span></span>
<span data-ttu-id="6752a-119">Önbelleğin olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6752a-119">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6752a-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="6752a-120">-RuleName</span></span>
<span data-ttu-id="6752a-121">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="6752a-121">Name of firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6752a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6752a-122">CommonParameters</span></span>
<span data-ttu-id="6752a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6752a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6752a-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6752a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6752a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6752a-125">INPUTS</span></span>

### <span data-ttu-id="6752a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6752a-126">System.String</span></span>

## <span data-ttu-id="6752a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6752a-127">OUTPUTS</span></span>

### <span data-ttu-id="6752a-128">Microsoft. Azure. Commands. RedisCache. model. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6752a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="6752a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6752a-129">NOTES</span></span>

## <span data-ttu-id="6752a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6752a-130">RELATED LINKS</span></span>

[<span data-ttu-id="6752a-131">New-Azredecachefirewallrule</span><span class="sxs-lookup"><span data-stu-id="6752a-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6752a-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6752a-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="6752a-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6752a-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="6752a-134">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6752a-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="6752a-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6752a-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="6752a-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="6752a-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)