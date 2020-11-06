---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571746"
---
# Get-AzureRmSubscription

## SYNOPSIS
Geçerli hesabın erişebileceği abonelikleri alın.

## INDEKI

### Listın (varsayılan)
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### Listbynamei
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## Tanım
Get-AzureRmSubscription cmdlet 'i, geçerli hesabın erişebileceği abonelikler için abonelik KIMLIĞI, abonelik adı ve ev kiracısını alır.

## ÖRNEKLERDEN

### Örnek 1: Tüm kiracıları tüm abonelikleri al
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

Bu komut, geçerli hesap için yetkilendirilmiş tüm kiracıları tüm abonelikleri alır.

### Örnek 2: belirli bir kiracıya yönelik tüm abonelikleri alma
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

Belirtilen Kiracıdaki geçerli hesap için yetkilendirilmiş tüm abonelikleri listeler.

### Örnek 3: geçerli Kiracıdaki tüm abonelikleri alma
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

Bu komut geçerli Kiracıdaki geçerli kullanıcı için yetkilendirilmiş tüm abonelikleri alır.

### Örnek 4: belirli bir aboneliği kullanmak için geçerli bağlamı değiştirme
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

Bu komut belirtilen aboneliği alır ve geçerli bağlamı kullanacak şekilde ayarlar.
Bu oturumdaki sonraki tüm cmdlet 'ler yeni aboneliği (contoso aboneliği 1) varsayılan olarak kullanır.

## PARAMETRELERINE

### -SubscriptionID
Alınacak aboneliğin KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Alınacak aboneliğin adını belirtir.

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tenantıd
Alınacak abonelikleri içeren kiracının KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Psazuyeniden gönderme komut dosyası

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

