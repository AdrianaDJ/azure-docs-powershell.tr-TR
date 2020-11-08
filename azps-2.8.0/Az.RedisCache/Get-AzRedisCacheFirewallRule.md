---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 1bf6394621435293be1d00d4a9e9f435c160e668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932945"
---
# <span data-ttu-id="bb85e-101">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb85e-101">Get-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="bb85e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb85e-102">SYNOPSIS</span></span>
<span data-ttu-id="bb85e-103">Redis Cache 'de güvenlik duvarı kuralları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="bb85e-103">Get firewall rules set on Redis Cache.</span></span>

## <span data-ttu-id="bb85e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb85e-104">SYNTAX</span></span>

```
Get-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> [-RuleName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb85e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb85e-105">DESCRIPTION</span></span>
<span data-ttu-id="bb85e-106">If **RuleName** parametresi sağlanmışsa, **Get-AzRedisCacheFirewallRule** cmdlet 'ı, Azure Redis Cache 'de belirtilen güvenlik duvarı kuralı hakkında ayrıntılı bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bb85e-106">If **RuleName** parameter if provided, **Get-AzRedisCacheFirewallRule** cmdlet gets detail about the specified firewall rule on Azure Redis Cache.</span></span> <span data-ttu-id="bb85e-107">Yalnızca **ad** belirtilirse, bu, bu Red</span><span class="sxs-lookup"><span data-stu-id="bb85e-107">If only **Name** is specified this operation gets all firewall rules available on that Redis Cache.</span></span>

## <span data-ttu-id="bb85e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb85e-108">EXAMPLES</span></span>

### <span data-ttu-id="bb85e-109">Örnek 1: tek bir güvenlik duvarı kuralı edinin</span><span class="sxs-lookup"><span data-stu-id="bb85e-109">Example 1: Get a single firewall rule</span></span>
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

<span data-ttu-id="bb85e-110">Bu komut myCache adlı Red, Cache 'den Rule adlı güvenlik duvarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="bb85e-110">This command gets firewall rule named ruleone from Redis Cache named mycache.</span></span>

### <span data-ttu-id="bb85e-111">Örnek 2: tüm güvenlik duvarı kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="bb85e-111">Example 2: Get all firewall rules</span></span>
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

<span data-ttu-id="bb85e-112">Bu komut myCache adındaki tüm güvenlik duvarı kurallarını Redcache 'den alır.</span><span class="sxs-lookup"><span data-stu-id="bb85e-112">This command gets all firewall rules from Redis Cache named mycache.</span></span>

## <span data-ttu-id="bb85e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb85e-113">PARAMETERS</span></span>

### <span data-ttu-id="bb85e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb85e-114">-DefaultProfile</span></span>
<span data-ttu-id="bb85e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb85e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb85e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="bb85e-116">-Name</span></span>
<span data-ttu-id="bb85e-117">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="bb85e-117">Name of redis cache.</span></span>

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

### <span data-ttu-id="bb85e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb85e-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb85e-119">Önbelleğin olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bb85e-119">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="bb85e-120">-RuleName</span><span class="sxs-lookup"><span data-stu-id="bb85e-120">-RuleName</span></span>
<span data-ttu-id="bb85e-121">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="bb85e-121">Name of firewall rule.</span></span>

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

### <span data-ttu-id="bb85e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb85e-122">CommonParameters</span></span>
<span data-ttu-id="bb85e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb85e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb85e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb85e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb85e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb85e-125">INPUTS</span></span>

### <span data-ttu-id="bb85e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="bb85e-126">System.String</span></span>

## <span data-ttu-id="bb85e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb85e-127">OUTPUTS</span></span>

### <span data-ttu-id="bb85e-128">Microsoft. Azure. Commands. RedisCache. model. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb85e-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="bb85e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb85e-129">NOTES</span></span>

## <span data-ttu-id="bb85e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb85e-130">RELATED LINKS</span></span>

[<span data-ttu-id="bb85e-131">New-Azredecachefirewallrule</span><span class="sxs-lookup"><span data-stu-id="bb85e-131">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="bb85e-132">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="bb85e-132">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="bb85e-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bb85e-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="bb85e-134">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bb85e-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="bb85e-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bb85e-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="bb85e-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="bb85e-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)