---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheLink.md
ms.openlocfilehash: 58c52e30270af309eb5104bbc0a9308f83df91ea
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274695"
---
# Get-AzRedisCacheLink

## SYNOPSIS
Redis Cache için coğrafi çoğaltma bağlantısı alın.

## INDEKI

### AllLinksForCache (varsayılan)
```
Get-AzRedisCacheLink -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Alllinkforprimarycache
```
Get-AzRedisCacheLink -PrimaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SingleLink
```
Get-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Alllinkforsecondarycache
```
Get-AzRedisCacheLink -SecondaryServerName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Coğrafi çoğaltma bağlantı ayrıntısı almanın dört farklı yolu vardır. Parametre adı veya PrimaryServerName ve/veya SecondaryServerName sağlayın. Ad verilirse, önbelleğin var olduğu tüm bağlantılar verilir. Yalnızca PrimaryServerName verilirse, önbelleğin birincili olduğu tüm bağlantılar verilir. Yalnızca SecondaryServerName etkinleştirilirse önbelleğin ikincil olduğu tüm bağlantılar verilir. PrimaryServerName ve SecondaryServerName her ikisi de verilirse, doğru role sahip belirli bir bağlantı döndürülür. 

## ÖRNEKLERDEN

### Örnek 1: AllLinksForCache parametresini kullanma
```
PS C:\>Get-AzRedisCacheLink -Name "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Bu komut, myCache1 adlı Red, Cache için tüm coğrafi çoğaltma bağlantılarını alır.

### Örnek 2: Alllinkforprimarycache parametresini kullanma
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Bu komut, myCache1 adındaki Redis önbelleğinin birincili coğrafi çoğaltma bağlantılarını alır.

### Örnek 3: Alllinkforsecondarycache parametresini kullanma
```
PS C:\>Get-AzRedisCacheLink -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Bu komut, mycache2 adındaki Redis önbelleğinin ikincili coğrafi çoğaltma bağlantılarını alır.

### Örnek 4: parametre kümesi SingleLink kullanmaya başlama
```
PS C:\>Get-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Succeeded
```

Bu komut, myCache1 adındaki Redis önbelleğinin birincil ve mycache2 adındaki Redis Cache olan tek bir coğrafi çoğaltma bağlantısını alır.

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

### -Ad
Redis önbelleğinin adı.

```yaml
Type: System.String
Parameter Sets: AllLinksForCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PrimaryServerName
Bağlantıdaki birincil Redis önbelleğinin adı.

```yaml
Type: System.String
Parameter Sets: AllLinksForPrimaryCache, SingleLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SecondaryServerName
Bağlantıdaki ikincil Redis önbelleğinin adı.

```yaml
Type: System.String
Parameter Sets: SingleLink, AllLinksForSecondaryCache
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RedisCache. model. PSRedisLinkedServer

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azreercachelink](./New-AzRedisCacheLink.md)

[Remove-AzRedisCacheLink](./Remove-AzRedisCacheLink.md)

[Get-AzRedisCache](./Get-AzRedisCache.md)

[Yeni-AzRedisCache](./New-AzRedisCache.md)

[Remove-AzRedisCache](./Remove-AzRedisCache.md)

[Set-AzRedisCache](./Set-AzRedisCache.md)