---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheFirewallRule.md
ms.openlocfilehash: 50a2df73d6cfa1e9d34f2c5c4b426f601c9d9309
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096811"
---
# <span data-ttu-id="61bcf-101">New-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61bcf-101">New-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="61bcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="61bcf-103">Redis önbelleğinde bir güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61bcf-103">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="61bcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61bcf-104">SYNTAX</span></span>

### <span data-ttu-id="61bcf-105">Normal değer kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="61bcf-105">NormalParameterSet (Default)</span></span>
```
New-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bcf-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="61bcf-106">RedisCacheAttributesObject</span></span>
```
New-AzRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61bcf-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="61bcf-107">ResourceIdParameterSet</span></span>
```
New-AzRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61bcf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="61bcf-108">DESCRIPTION</span></span>
<span data-ttu-id="61bcf-109">Redis önbelleğinde bir güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="61bcf-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="61bcf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61bcf-110">EXAMPLES</span></span>

### <span data-ttu-id="61bcf-111">Örnek 1: güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="61bcf-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="61bcf-112">Bu komut myCache adlı Red, Cache ile ruleone adlı güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="61bcf-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="61bcf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61bcf-113">PARAMETERS</span></span>

### <span data-ttu-id="61bcf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61bcf-114">-DefaultProfile</span></span>
<span data-ttu-id="61bcf-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61bcf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61bcf-116">-BitişIP</span><span class="sxs-lookup"><span data-stu-id="61bcf-116">-EndIP</span></span>
<span data-ttu-id="61bcf-117">Bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="61bcf-117">Ending IP address.</span></span>

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

### <span data-ttu-id="61bcf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61bcf-118">-InputObject</span></span>
<span data-ttu-id="61bcf-119">RedisCacheAttributes türünde nesne</span><span class="sxs-lookup"><span data-stu-id="61bcf-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61bcf-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="61bcf-120">-Name</span></span>
<span data-ttu-id="61bcf-121">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="61bcf-121">Name of redis cache.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bcf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61bcf-122">-ResourceGroupName</span></span>
<span data-ttu-id="61bcf-123">Önbelleğin olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="61bcf-123">Name of resource group in which cache exists.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bcf-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="61bcf-124">-ResourceId</span></span>
<span data-ttu-id="61bcf-125">Redis Cache 'in ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="61bcf-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61bcf-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="61bcf-126">-RuleName</span></span>
<span data-ttu-id="61bcf-127">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="61bcf-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="61bcf-128">-BaşlangıçIP</span><span class="sxs-lookup"><span data-stu-id="61bcf-128">-StartIP</span></span>
<span data-ttu-id="61bcf-129">Başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="61bcf-129">Starting IP address.</span></span>

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

### <span data-ttu-id="61bcf-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="61bcf-130">-Confirm</span></span>
<span data-ttu-id="61bcf-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61bcf-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bcf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61bcf-132">-WhatIf</span></span>
<span data-ttu-id="61bcf-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61bcf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61bcf-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61bcf-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61bcf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61bcf-135">CommonParameters</span></span>
<span data-ttu-id="61bcf-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61bcf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61bcf-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61bcf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61bcf-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61bcf-138">INPUTS</span></span>

### <span data-ttu-id="61bcf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="61bcf-139">System.String</span></span>

### <span data-ttu-id="61bcf-140">Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributes</span><span class="sxs-lookup"><span data-stu-id="61bcf-140">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributes</span></span>

## <span data-ttu-id="61bcf-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61bcf-141">OUTPUTS</span></span>

### <span data-ttu-id="61bcf-142">Microsoft. Azure. Commands. RedisCache. model. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61bcf-142">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="61bcf-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61bcf-143">NOTES</span></span>

## <span data-ttu-id="61bcf-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61bcf-144">RELATED LINKS</span></span>

[<span data-ttu-id="61bcf-145">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61bcf-145">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="61bcf-146">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="61bcf-146">Remove-AzRedisCacheFirewallRule</span></span>](./Remove-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="61bcf-147">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="61bcf-147">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="61bcf-148">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="61bcf-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="61bcf-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="61bcf-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="61bcf-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="61bcf-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)