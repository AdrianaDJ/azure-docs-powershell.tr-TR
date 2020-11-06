---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 796396B4-1F9D-4D53-AD2E-4CE83B563E93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHub.md
ms.openlocfilehash: 2bb7d6f6addbbbf91f7f9f93e7e30de9cb3ece81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594652"
---
# Get-AzureRmNotificationHub

## SYNOPSIS
Bildirim Hub 'larınız hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [[-NotificationHub] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmNotificationHub** cmdlet 'i belirtilen ad alanındaki Bildirim Hub 'ları hakkında bilgi alır ve belirli bir kaynak grubuna atanır.
Örneğin, ContosoNamespace ad alanı 'ndaki tüm Bildirim Hub 'ları için bilgi alabilir ve ContosoNotificationsGroup kaynak grubuna atayabilirsiniz.

Alternatif olarak, döndürülen verileri belirli bir Bildirim Hub 'ı hakkındaki bilgilerle sınırlandırmak için *Notificationhub* parametresini kullanabilirsiniz.

Bu istemciler tarafından kullanılan iOS, Android, Windows Phone 8 ve Windows Mağazası gibi platforma bakılmaksızın birden fazla istemciye anında bildirim göndermek için bildirim hubları kullanılır.
Bu hub 'lar kabaca tek tek uygulamalara eşdeğerdir ve tüm uygulamalarınız kendi Bildirim Hub 'ına sahip olur.

Bu cmdlet yalnızca Hub 'ın kendisi hakkında bilgi alır.
Bir hub yetkilendirme kuralları, bağlantı dizeleri ve platform bildirimi hizmeti kimlik bilgileri hakkında bilgi almak için Get-AzureRmNotificationHubAuthorizationRules, Get-AzureRmNotificationHubListKeys ve Get-AzureRmNotificationHubPNSCredentials gibi diğer cmdlet 'ler gereklidir.

## ÖRNEKLERDEN

### Örnek 1: belirli bir ad alanındaki tüm Bildirim Hub 'larının bilgilerini alma
```
PS C:\>Get-AzureRmNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup"
```

Bu komut, kaynak grubuna atanmış olan ContosoNamespace adındaki tüm Bildirim Hub 'larının bilgilerini alır.

## PARAMETRELERINE

### -Namespace
Bildirim Hub 'ına atanmış olan ad boşluğunu belirtir.

Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
Bu cmdlet 'in aldığı Bildirim Hub 'ının adını belirtir.

Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Bildirim Hub 'ına atanmış kaynak grubunu belirtir.

Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri yalnızca envanter yönetimi ve Azure yönetimine yardımcı olacak yollarla düzenler.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Notificationhub..

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[Get-AzureRmNotificationHubListKeys](./Get-AzureRmNotificationHubListKeys.md)

[Get-AzureRmNotificationHubPNSCredentials](./Get-AzureRmNotificationHubPNSCredentials.md)

[Yeni-AzureRmNotificationHub](./New-AzureRmNotificationHub.md)

[Remove-AzureRmNotificationHub](./Remove-AzureRmNotificationHub.md)

[Set-AzureRmNotificationHub](./Set-AzureRmNotificationHub.md)


