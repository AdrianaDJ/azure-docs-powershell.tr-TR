---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: e24ea6e0b5bf88b17a6209f2ea69634200a10a62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759531"
---
# <span data-ttu-id="20195-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20195-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="20195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20195-102">SYNOPSIS</span></span>
<span data-ttu-id="20195-103">Redis önbelleğinden bir güvenlik duvarı kuralını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="20195-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="20195-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20195-104">SYNTAX</span></span>

### <span data-ttu-id="20195-105">Normal değer kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="20195-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20195-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="20195-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20195-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="20195-107">DESCRIPTION</span></span>
<span data-ttu-id="20195-108">Redis önbelleğinden bir güvenlik duvarı kuralını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="20195-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="20195-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20195-109">EXAMPLES</span></span>

### <span data-ttu-id="20195-110">Örnek 1: tek bir güvenlik duvarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="20195-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="20195-111">Bu komut, myCache adlı Red. Cache 'den ruleone adındaki bir güvenlik duvarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="20195-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="20195-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20195-112">PARAMETERS</span></span>

### <span data-ttu-id="20195-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20195-113">-DefaultProfile</span></span>
<span data-ttu-id="20195-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="20195-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20195-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20195-115">-InputObject</span></span>
<span data-ttu-id="20195-116">PSRedisFirewallRule türündeki nesne</span><span class="sxs-lookup"><span data-stu-id="20195-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20195-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="20195-117">-Name</span></span>
<span data-ttu-id="20195-118">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="20195-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="20195-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="20195-119">-PassThru</span></span>
<span data-ttu-id="20195-120">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="20195-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20195-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20195-121">-ResourceGroupName</span></span>
<span data-ttu-id="20195-122">Önbelleğin olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="20195-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="20195-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="20195-123">-RuleName</span></span>
<span data-ttu-id="20195-124">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="20195-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="20195-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="20195-125">-Confirm</span></span>
<span data-ttu-id="20195-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20195-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20195-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20195-127">-WhatIf</span></span>
<span data-ttu-id="20195-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20195-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20195-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="20195-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20195-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20195-130">CommonParameters</span></span>
<span data-ttu-id="20195-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20195-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20195-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20195-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20195-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20195-133">INPUTS</span></span>

### <span data-ttu-id="20195-134">System. String</span><span class="sxs-lookup"><span data-stu-id="20195-134">System.String</span></span>

### <span data-ttu-id="20195-135">Microsoft. Azure. Commands. RedisCache. model. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20195-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="20195-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20195-136">OUTPUTS</span></span>

### <span data-ttu-id="20195-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20195-137">System.Boolean</span></span>

## <span data-ttu-id="20195-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20195-138">NOTES</span></span>

## <span data-ttu-id="20195-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20195-139">RELATED LINKS</span></span>

[<span data-ttu-id="20195-140">New-Azredecachefirewallrule</span><span class="sxs-lookup"><span data-stu-id="20195-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="20195-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="20195-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="20195-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20195-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="20195-143">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20195-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="20195-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20195-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="20195-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="20195-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)