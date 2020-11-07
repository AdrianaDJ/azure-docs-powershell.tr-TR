---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762420"
---
# New-AzureRmRedisCache

## SYNOPSIS
Redis Cache oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmRedisCache** cmdlet 'ı Azure Redis Cache oluşturur.

## ÖRNEKLERDEN

### Örnek 1: Redis Cache oluşturma
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
```

Bu komut, Redbir önbellek oluşturur.

### Örnek 2: Standart SKU ön belleğini oluşturma
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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
```

Bu komut, zaten varsa Redis önbelleğini oluşturur

## PARAMETRELERINE

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

### -Konum
Redis önbelleğinin oluşturulacağı konumu belirtir.
Geçerli değerler: 

- Kuzey Orta ABD
- Güney Orta ABD
- Orta ABD
- Batı Avrupa
- Kuzey Avrupa
- Batı ABD
- Doğu ABD
- Doğu ABD 2
- Japon Doğu
- Japon Batı
- Brezilya Güney
- Güneydoğu Asya
- Doğu Asya
- Avustralya Doğu
- Avustralya Güneydoğu

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

### -MaxMemoryPolicy
Bu parametre kullanımdan kaldırıldı.
MaxMemory-ilkesini ayarlamak için *Redisconfiguration* parametresini kullanın.
Örneğin: 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### -Ad
Oluşturulacak Redis önbelleğinin adını belirtir.

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

### -RedisVersion
Bu parametre kullanım dışıdır ve ileriki sürümlerden kaldırılacaktır.

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

### -ResourceGroupName
Redis önbelleğinin oluşturulacağı kaynak grubun adını belirtir.

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

### -Shardsay
Premium küme önbelleğinde oluşturulacak paylaşım sayısını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- 2
- 2
- @
- 1.921.024
- tir
- +
- +
- 8@@
- döndürdü 
- on

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

Varsayılan değer 1GB veya C1.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

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
- Min

Varsayılan değer standarttır.

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

### -StaticIP
Redis Cache için alt ağda benzersiz bir IP adresi belirtir.

Bu parametre için bir değer belirtmezseniz, bu cmdlet alt ağdan bir IP adresi seçer.

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

### -Alt ağ
Redis önbelleğinin dağıtılacağı alt ağın adını belirtir.

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

### -SubnetId
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

### -VirtualNetwork
Redis önbelleğinin dağıtılacağı sanal ağın kaynak KIMLIĞINI belirtir.

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

### Microsoft. Azure. Commands. RedisCache. modeller. RedisCacheAttributesWithAccessKeys
Bu cmdlet, birincil ve ikincil erişim tuşları gibi bir kırmızı tür önbelleğinin tüm özniteliklerini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


