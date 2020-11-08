---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheFirewallRule.md
ms.openlocfilehash: c19be1f524519a55a5a95a575e97cfd250952570
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266947"
---
# <span data-ttu-id="89225-101">Remove-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="89225-101">Remove-AzRedisCacheFirewallRule</span></span>

## <span data-ttu-id="89225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89225-102">SYNOPSIS</span></span>
<span data-ttu-id="89225-103">Redis önbelleğinden bir güvenlik duvarı kuralını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="89225-103">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="89225-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89225-104">SYNTAX</span></span>

### <span data-ttu-id="89225-105">Normal değer kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89225-105">NormalParameterSet (Default)</span></span>
```
Remove-AzRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89225-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="89225-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89225-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="89225-107">DESCRIPTION</span></span>
<span data-ttu-id="89225-108">Redis önbelleğinden bir güvenlik duvarı kuralını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="89225-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="89225-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89225-109">EXAMPLES</span></span>

### <span data-ttu-id="89225-110">Örnek 1: tek bir güvenlik duvarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="89225-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="89225-111">Bu komut, myCache adlı Red. Cache 'den ruleone adındaki bir güvenlik duvarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="89225-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="89225-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89225-112">PARAMETERS</span></span>

### <span data-ttu-id="89225-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89225-113">-DefaultProfile</span></span>
<span data-ttu-id="89225-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89225-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89225-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89225-115">-InputObject</span></span>
<span data-ttu-id="89225-116">PSRedisFirewallRule türündeki nesne</span><span class="sxs-lookup"><span data-stu-id="89225-116">object of type PSRedisFirewallRule</span></span>

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

### <span data-ttu-id="89225-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="89225-117">-Name</span></span>
<span data-ttu-id="89225-118">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="89225-118">Name of redis cache.</span></span>

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

### <span data-ttu-id="89225-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="89225-119">-PassThru</span></span>
<span data-ttu-id="89225-120">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="89225-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="89225-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89225-121">-ResourceGroupName</span></span>
<span data-ttu-id="89225-122">Önbelleğin olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89225-122">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="89225-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="89225-123">-RuleName</span></span>
<span data-ttu-id="89225-124">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="89225-124">Name of firewall rule.</span></span>

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

### <span data-ttu-id="89225-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="89225-125">-Confirm</span></span>
<span data-ttu-id="89225-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89225-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89225-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89225-127">-WhatIf</span></span>
<span data-ttu-id="89225-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89225-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89225-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89225-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89225-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89225-130">CommonParameters</span></span>
<span data-ttu-id="89225-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89225-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89225-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89225-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89225-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89225-133">INPUTS</span></span>

### <span data-ttu-id="89225-134">System. String</span><span class="sxs-lookup"><span data-stu-id="89225-134">System.String</span></span>

### <span data-ttu-id="89225-135">Microsoft. Azure. Commands. RedisCache. model. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="89225-135">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="89225-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89225-136">OUTPUTS</span></span>

### <span data-ttu-id="89225-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89225-137">System.Boolean</span></span>

## <span data-ttu-id="89225-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89225-138">NOTES</span></span>

## <span data-ttu-id="89225-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89225-139">RELATED LINKS</span></span>

[<span data-ttu-id="89225-140">New-Azredecachefirewallrule</span><span class="sxs-lookup"><span data-stu-id="89225-140">New-AzRedisCacheFirewallRule</span></span>](./New-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="89225-141">Get-AzRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="89225-141">Get-AzRedisCacheFirewallRule</span></span>](./Get-AzRedisCacheFirewallRule.md)

[<span data-ttu-id="89225-142">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="89225-142">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="89225-143">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="89225-143">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="89225-144">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="89225-144">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="89225-145">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="89225-145">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)