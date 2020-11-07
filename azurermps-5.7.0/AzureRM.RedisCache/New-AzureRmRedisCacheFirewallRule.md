---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheFirewallRule.md
ms.openlocfilehash: c89589d966c03614255751bf13769689ff875332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762516"
---
# <span data-ttu-id="8bdef-101">New-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8bdef-101">New-AzureRmRedisCacheFirewallRule</span></span>

## <span data-ttu-id="8bdef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bdef-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdef-103">Redis önbelleğinde bir güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8bdef-103">Create a firewall rule on a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bdef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8bdef-104">SYNTAX</span></span>

### <span data-ttu-id="8bdef-105">Normal değer kümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8bdef-105">NormalParameterSet (Default)</span></span>
```
New-AzureRmRedisCacheFirewallRule [-ResourceGroupName <String>] -Name <String> -RuleName <String>
 -StartIP <String> -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8bdef-106">RedisCacheAttributesObject</span><span class="sxs-lookup"><span data-stu-id="8bdef-106">RedisCacheAttributesObject</span></span>
```
New-AzureRmRedisCacheFirewallRule -InputObject <RedisCacheAttributes> -RuleName <String> -StartIP <String>
 -EndIP <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bdef-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8bdef-107">ResourceIdParameterSet</span></span>
```
New-AzureRmRedisCacheFirewallRule -ResourceId <String> -RuleName <String> -StartIP <String> -EndIP <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bdef-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8bdef-108">DESCRIPTION</span></span>
<span data-ttu-id="8bdef-109">Redis önbelleğinde bir güvenlik duvarı kuralı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8bdef-109">Create a firewall rule on a Redis Cache.</span></span>

## <span data-ttu-id="8bdef-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8bdef-110">EXAMPLES</span></span>

### <span data-ttu-id="8bdef-111">Örnek 1: güvenlik duvarı kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="8bdef-111">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmRedisCacheFirewallRule -Name "mycache" -RuleName "ruleone" -StartIP "10.0.0.1" -EndIP "10.0.0.32"

        ResourceGroupName : myGroup
        Name              : mycache
        FirewallRuleId    : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/mycache/firewallRules/ruleone
        RuleName          : ruleone
        Type              : Microsoft.Cache/Redis/firewallRules
        StartIP           : 10.0.0.1
        EndIP             : 10.0.0.32
```

<span data-ttu-id="8bdef-112">Bu komut myCache adlı Red, Cache ile ruleone adlı güvenlik duvarı kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bdef-112">This command creates firewall rule named ruleone on Redis Cache named mycache.</span></span>

## <span data-ttu-id="8bdef-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8bdef-113">PARAMETERS</span></span>

### <span data-ttu-id="8bdef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdef-114">-DefaultProfile</span></span>
<span data-ttu-id="8bdef-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8bdef-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bdef-116">-BitişIP</span><span class="sxs-lookup"><span data-stu-id="8bdef-116">-EndIP</span></span>
<span data-ttu-id="8bdef-117">Bitiş IP adresi.</span><span class="sxs-lookup"><span data-stu-id="8bdef-117">Ending IP address.</span></span>

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

### <span data-ttu-id="8bdef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bdef-118">-InputObject</span></span>
<span data-ttu-id="8bdef-119">RedisCacheAttributes türünde nesne</span><span class="sxs-lookup"><span data-stu-id="8bdef-119">object of type RedisCacheAttributes</span></span>

```yaml
Type: RedisCacheAttributes
Parameter Sets: RedisCacheAttributesObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdef-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8bdef-120">-Name</span></span>
<span data-ttu-id="8bdef-121">Redis önbelleğinin adı.</span><span class="sxs-lookup"><span data-stu-id="8bdef-121">Name of redis cache.</span></span>

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

### <span data-ttu-id="8bdef-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdef-122">-ResourceGroupName</span></span>
<span data-ttu-id="8bdef-123">Önbelleğin olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8bdef-123">Name of resource group in which cache exists.</span></span>

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

### <span data-ttu-id="8bdef-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8bdef-124">-ResourceId</span></span>
<span data-ttu-id="8bdef-125">Redis Cache 'in ARM kimliği.</span><span class="sxs-lookup"><span data-stu-id="8bdef-125">ARM Id of Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdef-126">-RuleName</span><span class="sxs-lookup"><span data-stu-id="8bdef-126">-RuleName</span></span>
<span data-ttu-id="8bdef-127">Güvenlik duvarı kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="8bdef-127">Name of firewall rule.</span></span>

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

### <span data-ttu-id="8bdef-128">-BaşlangıçIP</span><span class="sxs-lookup"><span data-stu-id="8bdef-128">-StartIP</span></span>
<span data-ttu-id="8bdef-129">Başlangıç IP adresi.</span><span class="sxs-lookup"><span data-stu-id="8bdef-129">Starting IP address.</span></span>

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

### <span data-ttu-id="8bdef-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="8bdef-130">-Confirm</span></span>
<span data-ttu-id="8bdef-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8bdef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bdef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bdef-132">-WhatIf</span></span>
<span data-ttu-id="8bdef-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8bdef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bdef-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8bdef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bdef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdef-135">CommonParameters</span></span>
<span data-ttu-id="8bdef-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8bdef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdef-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bdef-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdef-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8bdef-138">INPUTS</span></span>

### <span data-ttu-id="8bdef-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8bdef-139">System.String</span></span>

## <span data-ttu-id="8bdef-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8bdef-140">OUTPUTS</span></span>

### <span data-ttu-id="8bdef-141">Microsoft. Azure. Commands. RedisCache. model. PSRedisFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8bdef-141">Microsoft.Azure.Commands.RedisCache.Models.PSRedisFirewallRule</span></span>

## <span data-ttu-id="8bdef-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8bdef-142">NOTES</span></span>

## <span data-ttu-id="8bdef-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8bdef-143">RELATED LINKS</span></span>

[<span data-ttu-id="8bdef-144">Get-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8bdef-144">Get-AzureRmRedisCacheFirewallRule</span></span>](./Get-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="8bdef-145">Remove-AzureRmRedisCacheFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8bdef-145">Remove-AzureRmRedisCacheFirewallRule</span></span>](./Remove-AzureRmRedisCacheFirewallRule.md)

[<span data-ttu-id="8bdef-146">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8bdef-146">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="8bdef-147">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8bdef-147">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="8bdef-148">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8bdef-148">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="8bdef-149">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="8bdef-149">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
