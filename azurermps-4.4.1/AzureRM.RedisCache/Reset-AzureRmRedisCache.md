---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 2b352c649d01e2fceb42f99a6c4dad20859a2adc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762416"
---
# <span data-ttu-id="6ac73-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ac73-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="6ac73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ac73-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac73-103">Bir önbelleğin düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="6ac73-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ac73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ac73-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ac73-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ac73-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac73-106">**Reset-AzureRmRedisCache** cmdlet 'ı Azure Redis Cache örneğinin düğümlerini yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="6ac73-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="6ac73-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ac73-107">EXAMPLES</span></span>

### <span data-ttu-id="6ac73-108">Örnek 1: iki düğümü de yeniden Başlat</span><span class="sxs-lookup"><span data-stu-id="6ac73-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="6ac73-109">Bu komut, RedisCache06 adlı önbelleğin her iki düğümünü yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="6ac73-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="6ac73-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ac73-110">PARAMETERS</span></span>

### <span data-ttu-id="6ac73-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6ac73-111">-Force</span></span>
<span data-ttu-id="6ac73-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6ac73-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ac73-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ac73-113">-Name</span></span>
<span data-ttu-id="6ac73-114">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac73-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="6ac73-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6ac73-115">-PassThru</span></span>
<span data-ttu-id="6ac73-116">Bu cmdlet 'in işlemin başarılı olup olmadığını belirten bir Boole değeri döndürdüğünden emin olur.</span><span class="sxs-lookup"><span data-stu-id="6ac73-116">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="6ac73-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6ac73-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6ac73-118">-RebootType</span><span class="sxs-lookup"><span data-stu-id="6ac73-118">-RebootType</span></span>
<span data-ttu-id="6ac73-119">Hangi düğümün veya düğümlerin yeniden başlatılacağı.</span><span class="sxs-lookup"><span data-stu-id="6ac73-119">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="6ac73-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="6ac73-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6ac73-121">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="6ac73-121">PrimaryNode</span></span> 
- <span data-ttu-id="6ac73-122">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="6ac73-122">SecondaryNode</span></span> 
- <span data-ttu-id="6ac73-123">AllNodes</span><span class="sxs-lookup"><span data-stu-id="6ac73-123">AllNodes</span></span>

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

### <span data-ttu-id="6ac73-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac73-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ac73-125">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac73-125">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="6ac73-126">-Shargerçekleşti</span><span class="sxs-lookup"><span data-stu-id="6ac73-126">-ShardId</span></span>
<span data-ttu-id="6ac73-127">Kümeleme etkinleştirilmiş olan Premium önbellek için bu cmdlet 'in yeniden başladığı Shard 'in KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ac73-127">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="6ac73-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ac73-128">-Confirm</span></span>
<span data-ttu-id="6ac73-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ac73-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ac73-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ac73-130">-WhatIf</span></span>
<span data-ttu-id="6ac73-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ac73-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ac73-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ac73-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ac73-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac73-133">-DefaultProfile</span></span>
<span data-ttu-id="6ac73-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ac73-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ac73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac73-135">CommonParameters</span></span>
<span data-ttu-id="6ac73-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ac73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac73-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ac73-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac73-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ac73-138">INPUTS</span></span>

### <span data-ttu-id="6ac73-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ac73-139">None</span></span>
<span data-ttu-id="6ac73-140">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ac73-140">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="6ac73-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ac73-141">OUTPUTS</span></span>

### <span data-ttu-id="6ac73-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ac73-142">None</span></span>

## <span data-ttu-id="6ac73-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ac73-143">NOTES</span></span>
* <span data-ttu-id="6ac73-144">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="6ac73-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6ac73-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ac73-145">RELATED LINKS</span></span>

[<span data-ttu-id="6ac73-146">Dışarı aktarma-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ac73-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="6ac73-147">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ac73-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="6ac73-148">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ac73-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="6ac73-149">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ac73-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="6ac73-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="6ac73-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

