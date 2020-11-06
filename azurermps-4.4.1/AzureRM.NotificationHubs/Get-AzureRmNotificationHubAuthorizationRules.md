---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 7A9D8F5A-6035-411B-8FDB-96ABFEED05A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubAuthorizationRules.md
ms.openlocfilehash: 5d2398e86a5507e5672dba46cafbbb1f27c402a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594608"
---
# Get-AzureRmNotificationHubAuthorizationRules

## SYNOPSIS
Bildirim Hub ile ilişkili yetkilendirme kuralları hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmNotificationHubAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHub] <String> [[-AuthorizationRule] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmNotificationHubAuthorizationRules** cmdlet 'i bir Bildirim Hub Ile Ilişkili paylaşılan erişim IMZASı (SAS) yetkilendirme kuralları hakkında bilgi alır.
Cmdlet, bir hub ile ilişkili tüm kurallarla ilgili bilgileri döndürür veya *AuthorizationRule* parametresini ekleyerek belirli bir kural hakkında bilgi alır.

Yetkilendirme Kuralları Bildirim Hub 'larına erişimi yönetir.
Yetkilendirme kuralı, farklı izin düzeylerine dayalı olarak URL olarak bağlantı oluşturur.
İstemciler, uygun izin düzeyine dayalı olarak bu URI 'Lardan birine yönlendirilir.
Örneğin, listen iznine sahip bir istemci bu izin için URI 'ye yönlendirilir.

**Get-AzureRmNotificationHubAuthorizationRules** cmdlet 'i yalnızca Bildirim Hub ile ilişkili yetkilendirme kuralları hakkında bilgi alır.
Hub 'ın kendisiyle ilgili bilgi almak için Get-AzureRmNotificationHub seçeneğini kullanın.

## ÖRNEKLERDEN

### Örnek 1: Bildirim Hub 'ına atanan tüm yetkilendirme kuralları için bilgi alma
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub"
```

Bu komut, ContosoNamespace ad alanında Contosoınternalhub adındaki tüm yetkilendirme kuralları için bilgi alır.
Hub 'ın bulunduğu ad boşluğunu ve hub 'ın atandığı kaynak grubunu belirtmeniz gerekir.

### Örnek 2: Bildirim Hub 'ına atanmış yetkilendirme kuralları için bilgi alma
```
PS C:\>Get-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -NotificationHub "ContosoInternalHub" -AuthorizationRule "ListenRule"
```

Bu komut, ContosoNamespace ad alanında Contosoınternalhub adındaki tüm yetkilendirme kuralları için bilgi alır.
Komut döndürülen verileri ListenRule adlı tek bir yetkilendirme kuralıyla sınırlandırmak için *AuthorizationRule* parametresini kullanır.

## PARAMETRELERINE

### -AuthorizationRule
SAS kimlik doğrulama kuralının adını belirtir.
Bu kurallar, kullanıcıların Bildirim Hub 'ına sahip olduğu erişimin türünü belirler.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
Bu cmdlet 'in yetkilendirme kuralları atadığı Bildirim Merkezi 'ni belirtir.
Bildirim Hub 'ları, bu istemcilerin kullandığı platforma bakılmaksızın birden çok istemciye anında bildirim göndermek için kullanılır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Bildirim Hub 'ına atanmış kaynak grubunu belirtir.
Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri, envanter yönetimi ve Azure yönetimini basitleştirmeye yardımcı olacak yollarla düzenler.

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

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Notificationhublar. modeller. SharedAccessAuthorizationRuleAttributes]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)

[Yeni-AzureRmNotificationHubAuthorizationRules](./New-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Set-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


