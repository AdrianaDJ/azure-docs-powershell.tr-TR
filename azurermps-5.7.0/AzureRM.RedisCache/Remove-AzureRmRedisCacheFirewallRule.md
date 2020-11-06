---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: 7f2e9a3bb54aab9def9eba7bdc2a84680fe121c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573317"
---
# <span data-ttu-id="69e29-101">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="69e29-101">Remove-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="69e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69e29-102">SYNOPSIS</span></span>
<span data-ttu-id="69e29-103">Redis önbelleğinden bir güvenlik duvarı kuralını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="69e29-103">Remove a firewall rule from a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69e29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69e29-104">SYNTAX</span></span>

### <span data-ttu-id="69e29-105">Normal değer kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69e29-105">NormalParameterSet (Default)</span></span>
```
Remove-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69e29-106">PSRedisFirewallRuleObject</span><span class="sxs-lookup"><span data-stu-id="69e29-106">PSRedisFirewallRuleObject</span></span>
```
Remove-AzureRmRedisCacheFirewallRule -InputObject <PSRedisFirewallRule> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69e29-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="69e29-107">DESCRIPTION</span></span>
<span data-ttu-id="69e29-108">Redis önbelleğinden bir güvenlik duvarı kuralını kaldırma.</span><span class="sxs-lookup"><span data-stu-id="69e29-108">Remove a firewall rule from a Redis Cache.</span></span>

## <span data-ttu-id="69e29-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69e29-109">EXAMPLES</span></span>

### <span data-ttu-id="69e29-110">Örnek 1: tek bir güvenlik duvarı kuralını kaldırma</span><span class="sxs-lookup"><span data-stu-id="69e29-110">Example 1: Remove a single firewall rule</span></span>
```
PS C:\>Remove-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -PassThru
True
```

<span data-ttu-id="69e29-111">Bu komut, myCache adlı Red. Cache 'den ruleone adındaki bir güvenlik duvarı kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="69e29-111">This command removes a firewall rule named ruleone from Redis Cache named mycache.</span></span> 

## <span data-ttu-id="69e29-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69e29-112">PARAMETERS</span></span>

### <span data-ttu-id="69e29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69e29-113">-DefaultProfile</span></span>
<span data-ttu-id="69e29-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69e29-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69e29-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69e29-115">-InputObject</span></span>
<span data-ttu-id="69e29-116">PSRedisFirewallRule türündeki nesne</span><span class="sxs-lookup"><span data-stu-id="69e29-116">object of type PSRedisFirewallRule</span></span>

```yaml
Type: PSRedisFirewallRule
Parameter Sets: PSRedisFirewallRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69e29-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="69e29-117">-Name</span></span>
<span data-ttu-id="69e29-118">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="69e29-118">Name of redis cache.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e29-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="69e29-119">-PassThru</span></span>
<span data-ttu-id="69e29-120">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="69e29-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e29-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69e29-121">-ResourceGroupName</span></span>
<span data-ttu-id="69e29-122">Önbelleğin olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="69e29-122">Name of resource group in which cache exists.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e29-123">-RuleName</span><span class="sxs-lookup"><span data-stu-id="69e29-123">-RuleName</span></span>
<span data-ttu-id="69e29-124">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="69e29-124">Name of firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: NormalParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69e29-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="69e29-125">-Confirm</span></span>
<span data-ttu-id="69e29-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69e29-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e29-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69e29-127">-WhatIf</span></span>
<span data-ttu-id="69e29-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69e29-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69e29-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69e29-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e29-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e29-130">CommonParameters</span></span>
<span data-ttu-id="69e29-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69e29-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e29-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69e29-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e29-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69e29-133">INPUTS</span></span>

### <span data-ttu-id="69e29-134">System. String</span><span class="sxs-lookup"><span data-stu-id="69e29-134">System.String</span></span>

## <span data-ttu-id="69e29-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69e29-135">OUTPUTS</span></span>

### <span data-ttu-id="69e29-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="69e29-136">System.Boolean</span></span>

## <span data-ttu-id="69e29-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69e29-137">NOTES</span></span>

## <span data-ttu-id="69e29-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69e29-138">RELATED LINKS</span></span>

[<span data-ttu-id="69e29-139">Yeni-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="69e29-139">New-AzureRmRedisCacheFirewallRule</span></span>](./New-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="69e29-140">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="69e29-140">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="69e29-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="69e29-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="69e29-142">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="69e29-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="69e29-143">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="69e29-143">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="69e29-144">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="69e29-144">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
