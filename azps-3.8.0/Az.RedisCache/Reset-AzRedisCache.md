---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938183"
---
# <span data-ttu-id="d0a51-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0a51-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="d0a51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0a51-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a51-103">Bir önbelleğin düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0a51-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="d0a51-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0a51-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0a51-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0a51-105">DESCRIPTION</span></span>
<span data-ttu-id="d0a51-106">**Reset-AzRedisCache** cmdlet 'ı bir Azure Redis Cache örneğinin düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0a51-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="d0a51-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0a51-107">EXAMPLES</span></span>

### <span data-ttu-id="d0a51-108">Örnek 1: iki düğümü de yeniden Başlat</span><span class="sxs-lookup"><span data-stu-id="d0a51-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="d0a51-109">Bu komut, RedisCache06 adlı önbelleğin her iki düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="d0a51-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="d0a51-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0a51-110">PARAMETERS</span></span>

### <span data-ttu-id="d0a51-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a51-111">-DefaultProfile</span></span>
<span data-ttu-id="d0a51-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0a51-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0a51-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d0a51-113">-Force</span></span>
<span data-ttu-id="d0a51-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d0a51-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d0a51-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d0a51-115">-Name</span></span>
<span data-ttu-id="d0a51-116">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0a51-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="d0a51-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d0a51-117">-PassThru</span></span>
<span data-ttu-id="d0a51-118">Bu cmdlet 'in işlemin başarılı olup olmadığını belirten bir Boole değeri döndürdüğünden emin olur.</span><span class="sxs-lookup"><span data-stu-id="d0a51-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="d0a51-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="d0a51-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0a51-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="d0a51-120">-RebootType</span></span>
<span data-ttu-id="d0a51-121">Hangi düğümün veya düğümlerin yeniden başlatılacağı.</span><span class="sxs-lookup"><span data-stu-id="d0a51-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="d0a51-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d0a51-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0a51-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="d0a51-123">PrimaryNode</span></span> 
- <span data-ttu-id="d0a51-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="d0a51-124">SecondaryNode</span></span> 
- <span data-ttu-id="d0a51-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="d0a51-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a51-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a51-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0a51-127">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0a51-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="d0a51-128">-Shargerçekleşti</span><span class="sxs-lookup"><span data-stu-id="d0a51-128">-ShardId</span></span>
<span data-ttu-id="d0a51-129">Kümeleme etkinleştirilmiş olan Premium önbellek için bu cmdlet 'in yeniden başladığı Shard 'in KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d0a51-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0a51-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="d0a51-130">-Confirm</span></span>
<span data-ttu-id="d0a51-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d0a51-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a51-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a51-132">-WhatIf</span></span>
<span data-ttu-id="d0a51-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d0a51-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a51-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d0a51-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a51-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a51-135">CommonParameters</span></span>
<span data-ttu-id="d0a51-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0a51-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a51-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a51-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a51-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0a51-138">INPUTS</span></span>

### <span data-ttu-id="d0a51-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d0a51-139">System.String</span></span>

### <span data-ttu-id="d0a51-140">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="d0a51-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d0a51-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0a51-141">OUTPUTS</span></span>

### <span data-ttu-id="d0a51-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0a51-142">System.Boolean</span></span>

## <span data-ttu-id="d0a51-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0a51-143">NOTES</span></span>
* <span data-ttu-id="d0a51-144">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="d0a51-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d0a51-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0a51-145">RELATED LINKS</span></span>

[<span data-ttu-id="d0a51-146">Dışarı aktarma-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0a51-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="d0a51-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0a51-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="d0a51-148">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0a51-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d0a51-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0a51-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d0a51-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d0a51-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


