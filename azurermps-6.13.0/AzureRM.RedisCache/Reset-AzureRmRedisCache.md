---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 8aad14bde950a5e98d8d9331428a62e957cb0afe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593912"
---
# <span data-ttu-id="fd17a-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd17a-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="fd17a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd17a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd17a-103">Bir önbelleğin düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="fd17a-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd17a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd17a-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd17a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd17a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd17a-106">**Reset-AzureRmRedisCache** cmdlet 'ı Azure Redis Cache örneğinin düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="fd17a-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="fd17a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd17a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd17a-108">Örnek 1: iki düğümü de yeniden Başlat</span><span class="sxs-lookup"><span data-stu-id="fd17a-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="fd17a-109">Bu komut, RedisCache06 adlı önbelleğin her iki düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="fd17a-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="fd17a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd17a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd17a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd17a-111">-DefaultProfile</span></span>
<span data-ttu-id="fd17a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd17a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd17a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fd17a-113">-Force</span></span>
<span data-ttu-id="fd17a-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fd17a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd17a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd17a-115">-Name</span></span>
<span data-ttu-id="fd17a-116">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd17a-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="fd17a-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fd17a-117">-PassThru</span></span>
<span data-ttu-id="fd17a-118">Bu cmdlet 'in işlemin başarılı olup olmadığını belirten bir Boole değeri döndürdüğünden emin olur.</span><span class="sxs-lookup"><span data-stu-id="fd17a-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="fd17a-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="fd17a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd17a-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="fd17a-120">-RebootType</span></span>
<span data-ttu-id="fd17a-121">Hangi düğümün veya düğümlerin yeniden başlatılacağı.</span><span class="sxs-lookup"><span data-stu-id="fd17a-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="fd17a-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fd17a-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fd17a-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="fd17a-123">PrimaryNode</span></span> 
- <span data-ttu-id="fd17a-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="fd17a-124">SecondaryNode</span></span> 
- <span data-ttu-id="fd17a-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="fd17a-125">AllNodes</span></span>

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

### <span data-ttu-id="fd17a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd17a-126">-ResourceGroupName</span></span>
<span data-ttu-id="fd17a-127">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd17a-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="fd17a-128">-Shargerçekleşti</span><span class="sxs-lookup"><span data-stu-id="fd17a-128">-ShardId</span></span>
<span data-ttu-id="fd17a-129">Kümeleme etkinleştirilmiş olan Premium önbellek için bu cmdlet 'in yeniden başladığı Shard 'in KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd17a-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="fd17a-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd17a-130">-Confirm</span></span>
<span data-ttu-id="fd17a-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd17a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd17a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd17a-132">-WhatIf</span></span>
<span data-ttu-id="fd17a-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd17a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd17a-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd17a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd17a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd17a-135">CommonParameters</span></span>
<span data-ttu-id="fd17a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd17a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd17a-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd17a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd17a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd17a-138">INPUTS</span></span>

### <span data-ttu-id="fd17a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fd17a-139">System.String</span></span>

### <span data-ttu-id="fd17a-140">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fd17a-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="fd17a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd17a-141">OUTPUTS</span></span>

### <span data-ttu-id="fd17a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd17a-142">System.Boolean</span></span>

## <span data-ttu-id="fd17a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd17a-143">NOTES</span></span>
* <span data-ttu-id="fd17a-144">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="fd17a-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="fd17a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd17a-145">RELATED LINKS</span></span>

[<span data-ttu-id="fd17a-146">Dışarı aktarma-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd17a-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="fd17a-147">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd17a-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="fd17a-148">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd17a-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="fd17a-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd17a-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="fd17a-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fd17a-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


