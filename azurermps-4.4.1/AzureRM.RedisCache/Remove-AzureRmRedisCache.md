---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: a9a879386bdbc22eef3094e2f1d0cf19cd42cc45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587808"
---
# Remove-AzureRmRedisCache

## SYNOPSIS
Redis önbelleğini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmRedisCache** cmdlet 'ı, Azure Redis önbelleğini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: Redis önbelleğini kaldırma ve sonucu döndürme
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

Bu komut, Redis önbelleğini kaldırır ve işlemin başarılı olup olmadığını gösterir.

### Örnek 2: Redis önbelleğini kaldırma ve sonucu görüntüleme
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

Bu komut, Redis önbelleğini kaldırır.
Geçiş parametresi *belirtilmediğinden, işlemin* sonucu görüntülenmiyor.

## PARAMETRELERINE

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -Ad
Kaldırılacak kırmızı önbelleğin adını belirtir.

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

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

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

### -ResourceGroupName
Kaldırılacak kırmızı önbelleği içeren kaynak grubunun adını belirtir.

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

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

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

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

### Boole
Özel durum oluşursa $True döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmRedisCache](./Get-AzureRmRedisCache.md)

[Yeni-AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Set-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


