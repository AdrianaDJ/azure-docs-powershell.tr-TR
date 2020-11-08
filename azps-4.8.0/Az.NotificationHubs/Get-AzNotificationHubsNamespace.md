---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 9805B3F1-C6BB-4A0F-A7C3-1DD1ACB75CDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubsNamespace.md
ms.openlocfilehash: 3d0e604d3984a40acde02fb1f977e2922ae2d1d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274760"
---
# Get-AzNotificationHubsNamespace

## SYNOPSIS
Bildirim Merkezi ad alanı hakkında bilgi alır.

## INDEKI

```
Get-AzNotificationHubsNamespace [[-ResourceGroup] <String>] [[-Namespace] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzNotificationHubsNamespace** cmdlet 'i Bildirim Hub ad alanları hakkında bilgi alır.
Bu cmdlet, tüm ad boşluklarınız ve belirli bir kaynak grubuna atanmış ad alanları hakkında bilgi alma seçeneğini sunar; belirli bir ad alanı hakkında bilgi döndürmek için.
Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.
En az bir Bildirim Hub ad alanınız olmalıdır: tüm bildirim hubları bir ad alanına atanmalıdır.
Tek bir ad alanı, kuruluşunuzda yalnızca bir ad alanı kullanmanız gerektiği anlamına gelen birden çok hub 'ı oluşturabilir.
Öte yandan, hub 'larınızı daha iyi düzenlemek veya belirli kişilere bir hub alt kümesini yönetme izni vermek için birden fazla ad alanı da kullanabilirsiniz.
**Get-AzNotificationHubsNamespace** cmdlet 'i ad alanı hakkında temel bilgileri döndürür.
Ad alanıyla ilişkilendirilmiş yetkilendirme kuralları hakkında bilgi edinmek için Get-AzNotificationHubsNamespaceAuthorizationRules kullanın.

## ÖRNEKLERDEN

### Örnek 1: tüm Bildirim Hub alanları için bilgi alma
```
PS C:\>Get-AzNotificationHubsNamespace
```

Bu komut, tüm Bildirim Hub ad boşluklarınız için bilgi döndürür.

### Örnek 2: tek bir bildirim merkezi ad alanı için bilgi alma
```
PS C:\>Get-AzNotificationHubsNamespace -Namespace "ContosoNamespace"
```

Bu komut tek bir bildirim merkezi ad alanı için bilgi alıyor: ContosoNamespace.

### Örnek 3: belirli bir ad alanına atanan tüm Bildirim Hub 'ları için bilgi alma
```
PS C:\>Get-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup"
```

Bu komut, kaynak grubu ContosoNotificationsGroup atanan tüm Bildirim Hub ad alanları için bilgi alır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Namespace
Ad alanı için benzersiz bir ad belirtir.
Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Ad alanının atandığı kaynak grubunu belirtir.
Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzNotificationHubsNamespaceAuthorizationRule](./Get-AzNotificationHubsNamespaceAuthorizationRule.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


