---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 8EF45FCE-5475-4A18-BFB0-C016E239612E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCache.md
ms.openlocfilehash: 4cdd81b0cf9f83482192fbe6f484fb0b0d1beaf6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594184"
---
# Get-AzureRmRedisCache

## SYNOPSIS
Redis Cache alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tüm abonelikte (varsayılan)
```
Get-AzureRmRedisCache [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Tümü kaynak grubunda
```
Get-AzureRmRedisCache -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Belirli bir Redis Cache
```
Get-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmRedisCache** cmdlet 'i, belirtilen Azure Redis önbelleğini alır.
Parametre belirtmezseniz, bu işlem geçerli aboneliğin tüm Redis Cache 'i alır.

## ÖRNEKLERDEN

### Örnek 1: ad ile kırmızı bir önbellek alma
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup" -Name "myexists"

          ResourceGroupName  : myGroup


          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}

          EnableNonSslPort   : False

          RedisVersion       : 2.8

          Size               : 1GB

          Sku                : Basic
```

Bu komut myexists adındaki Redis Cache 'i alır.

### Örnek 2: kaynak grubundaki her bir kırmızı önbelleğe alma
```
PS C:\>Get-AzureRmRedisCache -ResourceGroupName "myGroup"


          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Basic

          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
          Location           : North Central US
          Name               : myearlier
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : True
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
```

Bu komut, belirtilen kaynak grubundaki tüm kırmızı önbelleğe alma önbelleğini alır.

### Örnek 3: geçerli abonelikteki her bir kırmızı önbelleğe alma
```
PS C:\>Get-AzureRmRedisCache


          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myexists
          Location           : North Central US
          Name               : myexists
          Type               : Microsoft.Cache/Redis
          HostName           : myexists.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Basic

          ResourceGroupName  : myGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup/providers/Microsoft.Cache/Redis/myearlier
          Location           : North Central US
          Name               : myearlier
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : True
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard


          ResourceGroupName  : myGroup2
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/myGroup2/providers/Microsoft.Cache/Redis/myearlier2
          Location           : North Central US
          Name               : myearlier2
          Type               : Microsoft.Cache/Redis
          HostName           : myearlier2.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : succeeded
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Basic
```

Bu komut geçerli abonelikteki tüm Redis Cache 'i alır.

## PARAMETRELERINE

### -Ad
Alınacak Redis önbelleğinin adını belirtir.
*Resourcegroupname* parametresiyle kullanın.

```yaml
Type: System.String
Parameter Sets: Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Alınacak Redis Cache içeren kaynak grubunun adını belirtir.

Yalnızca *Resourcegroupname* parametresini belirtirseniz, bu işlem belirtilen kaynak grubundaki tüm Redis Cache 'i alır.

```yaml
Type: System.String
Parameter Sets: All In Resource Group, Specific Redis Cache
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributes
Bir **RedisCacheAttributes** nesneleri dizisi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


