---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: aaec1ed3f165338c0aea6bf93e38dfaa8460cdf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932646"
---
# Set-AzRedisCache

## SYNOPSIS
Redis önbelleğini değiştirir.

## INDEKI

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Set-AzRedisCache** cmdlet 'ı, Azure Redis önbelleğini değiştirir.

## ÖRNEKLERDEN

### Örnek 1: Redis önbelleğini değiştirme
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

Bu komut MyCache adındaki Redis Cache için MaxMemory-ilkesini güncelleştirir.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Enablen, SslPort
SSL olmayan bağlantı noktasının etkinleştirilip etkinleştirilmediğini gösterir.
Varsayılan değer $False (SSL olmayan bağlantı noktası devre dışı bırakılır).

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Güncelleştirilecek Redis önbelleğinin adını belirtir.

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

### -RedisConfiguration
Redis yapılandırma ayarlarını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- RDB-yedekleme etkinleştirildi.
Veri kalıcılığını etkinleştirmeyeceğini belirtir.
Yalnızca Premium katman.
- RDB-depolama-bağlantı dizesi.
Veri kalıcılığı için depolama hesabının bağlantı dizesini belirtir.
Yalnızca Premium katman.
- RDB-yedekleme-frekans.
Redis veri kalıcılığı için yedekleme sıklığını belirtir.
Yalnızca Premium katman. 
- MaxMemory-ayrılmış.
Önbelleğe alınmayan işlemler için ayrılan belleği yapılandırır.
Standart ve Premium katmanlar. 
- MaxMemory-ilke.
Önbellek için çıkarma ilkesini yapılandırır.
Tüm fiyatlandırma katmanları. 
- Notify-anahtar uzayı-olaylar.
Anahtar alanı bildirimlerini yapılandırır.
Standart ve Premium katmanlar. 
- Hash-Max-ZipList-Entries.
Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.
Standart ve Premium katmanlar. 
- Hash-Max-ZipList-değer.
Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.
Standart ve Premium katmanlar. 
- Set-Max-ıntset-Entries.
Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.
Standart ve Premium katmanlar. 
- zset-Max-ZipList-Entries.
Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.
Standart ve Premium katmanlar. 
- zset-Max-ZipList-değer.
Küçük toplama veri türleri için bellek iyileştirmeyi yapılandırır.
Standart ve Premium katmanlar. 
- Databases.
Veritabanlarının sayısını yapılandırır.
Bu özellik yalnızca önbellek oluşturulurken yapılandırılabilir.
Standart ve Premium katmanlar.
Daha fazla bilgi için Azure PowerShell ile Azure Redis Cache 'i yönetme https://go.microsoft.com/fwlink/?LinkId=800051 ( https://go.microsoft.com/fwlink/?LinkId=800051) .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Redis önbelleğini içeren kaynak grubunun adını belirtir.

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

### -Shardsay
Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.

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

### -Boyut
Redis önbelleğinin boyutunu belirtir.
Geçerli değerler: 
- P1
- P2
- P3
- P4
- P5
- C0
- İşlemcinin
- İşlemcinin
- C3
- C4
- C5
- C6
- 250MB
- 1GB
- 2,5 GB
- 6GB
- 13GB
- 26GB
- 53GB
- 120 GB varsayılan değer 1GB veya C1.

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

### -SKU
Oluşturulacak Redis önbelleğinin SKU adını belirtir.
Geçerli değerler: 
- Ana
- Ardından
- Premium varsayılan değer standarttır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Etiketleri temsil eden karma tablo.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantSettings
Bu parametre kullanımdan kaldırıldı.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

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

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. topluluklar. Hashtable

### System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

### System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzRedisCache](./Get-AzRedisCache.md)

[Yeni-AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)


