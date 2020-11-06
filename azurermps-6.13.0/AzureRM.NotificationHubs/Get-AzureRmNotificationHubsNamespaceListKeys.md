---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: F769A8AB-E025-49EE-AEA4-0D27EAEE341F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/get-azurermnotificationhubsnamespacelistkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Get-AzureRmNotificationHubsNamespaceListKeys.md
ms.openlocfilehash: 2e90a656b700c1fda3064b740ccbbec08f2c7031
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594356"
---
# Get-AzureRmNotificationHubsNamespaceListKeys

## SYNOPSIS
Bildirim Merkezi ad alanı yetkilendirme kuralıyla ilişkili birincil ve ikincil bağlantı dizelerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmNotificationHubsNamespaceListKeys [-ResourceGroup] <String> [-Namespace] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmNotificationHubsNamespaceListKeys** cmdlet 'i, bir Bildirim Hub ad alanına atanan paylaşılan erişim IMZASı (SAS) yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini döndürür.
Yetkilendirme kuralları, Bildirim Hub ad alanında Kullanıcı haklarını yönetir.
Her kural bir birincil ve ikincil bağlantı dizesi içerir.

## ÖRNEKLERDEN

### Örnek 1: yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini alma
```
PS C:\>Get-AzureRmNotificationHubsNamespaceListKeys -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Bu komut, ContosoNamespace ad alanına atanan ListenRule adlı yetkilendirme kuralı için birincil ve ikincil bağlantı dizelerini döndürür.
Bu komutu çalıştırdığınızda, ad alanının atandığı kaynak grubunun adını eklemeniz gerekir.

## PARAMETRELERINE

### -AuthorizationRule
SAS kimlik doğrulama kuralının adını belirtir.
Bu kurallar, kullanıcıların Bildirim Hub 'ına sahip olduğu erişimin türünü belirler.

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Namespace
Bu cmdlet 'in aldığı bağlantı dizelerini içeren ad boşluğunu belirtir.

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

### -ResourceGroup
Ad alanının atandığı kaynak grubunu belirtir.
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Management. Notificationhub. model. ResourceListKeys

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[Get-AzureRmNotificationHubsNamespaceAuthorizationRules](./Get-AzureRmNotificationHubsNamespaceAuthorizationRules.md)


