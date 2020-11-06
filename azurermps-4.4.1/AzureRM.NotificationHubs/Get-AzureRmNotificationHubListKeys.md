---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubListKeys.md
ms.openlocfilehash: 924b729ca8ba324a6f44cade48ed803b2867b6b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594604"
---
# Get-AzureRmNotificationHubListKeys

## SYNOPSIS
Bildirim Merkezi yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmNotificationHubListKeys [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmNotificationHubListKeys** cmdlet 'i, bir bildirim hub paylaşılan erişim IMZASı (SAS) yetkilendirme kuralının birincil ve ikincil bağlantı dizelerini döndürür.

Yetkilendirme kuralları, hub 'daki Kullanıcı haklarını yönetir.
Her kural bir birincil ve ikincil bağlantı dizesi içerir.
Bu bağlantı dizeleri (URI) aşağıdakileri gerçekleştirir:

- Kullanıcıları bir kaynağa yönlendirin.
- Sorgu parametrelerini içeren bir belirteç ekleyin.

Bu parametrelerden biri, imza, kullanıcının kimliğini doğrulamak ve belirtilen erişim düzeyini sağlamak için kullanılır.

## ÖRNEKLERDEN

### Örnek 1: yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini alma
```
PS C:\>Get-AzureRmNotificationHubListKeys -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Bu komut, Contosoınternalhub Bildirim Hub 'ına atanan bir kural olan yetkilendirme kuralı ListenRule için birincil ve ikincil bağlantı dizelerini alır.
Komutta hub ad alanı ve kaynak grubu bulunmalıdır.

## PARAMETRELERINE

### -AuthorizationRule
Paylaşılan erişim Imzası (SAS) kimlik doğrulama kuralının adını belirtir.
Bu kurallar, kullanıcıların Bildirim Hub 'ına sahip olduğu erişimin türünü belirler.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
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
Bu cmdlet 'e yetkilendirme kuralı atayan Bildirim Merkezi 'ni belirtir.
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

### Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)


