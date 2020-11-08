---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274749"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Yetkilendirme kuralı oluşturur ve bu kuralı bir Bildirim Hub ad alanına atar.

## INDEKI

### Inputfileparameterset
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'ı paylaşılan erişim IMZASı (SAS) yetkilendirme kuralı oluşturur ve bunu bir Bildirim Hub alanına atar.
Yetkilendirme kuralları ad alanındaki Kullanıcı haklarını ve bu ad alanıyla birlikte gelen bildirim hubları yönetir.
Bu cmdlet, yeni yetkilendirme kuralı oluşturmak ve bunu bir ad alanına atamak için iki yol sağlar.
**Sharedaccessauthorizationruleattributes** nesnesinin bir örneğini oluşturabilir ve bu nesneyi yeni kuralın sahip olmasını istediğiniz özellik değerleriyle yapılandırabilirsiniz.
Bu, .NET Framework kullanılarak yapılabilir.
Bu özellik değerlerini, *sasrule* parametresini kullanarak yeni kuralınıza kopyalayabilirsiniz.
Alternatif olarak, ilgili yapılandırma değerlerini içeren bir JSON (JavaScript nesnesi Gösterim) dosyası oluşturabilir ve bu değerleri, *GirdiDosyası* parametresini kullanarak uygulayabilirsiniz.
JSON dosyası, aşağıdakine benzer sözdizimi kullanan bir metin dosyasıdır: {  
    "Ad": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =",  
    "Haklar": \[  
        "Dinle",  
        Göndermek  
    \]  
} **New-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i ile birlikte kullanıldığında, önceki JSON örneği, kullanıcılara ad boşluğuna izin veren, contosoauthorizationrule adlı bir yetkilendirme kuralı oluşturur.
Kimlik doğrulaması için kullanılan *PrimaryKey* , aşağıdaki Windows PowerShell komutu kullanılarak rasgele oluşturulabilir: \[ Convert \] :: ToBase64String ((1.. 32 |% { \[ Byte/] (Get-Random-en çok 255)}))

## ÖRNEKLERDEN

### Örnek 1: yetkilendirme kuralı oluşturma ve bunu bir ad alanına atama
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Bu komut, bir yetkilendirme kuralı oluşturur ve bu kuralı ContosoNamespace ad alanına atar.
Bu kuralı oluştururken, uygun ad alanını ve ad alanının atandığı kaynak grubunu belirtmeniz gerekir.
Bununla birlikte, kuralın kendisiyle ilgili herhangi bir bilgi belirtmeniz gerekmez: kural bilgileri C:\Configuration\NamespaceAuthorizationRules.jsgiriş dosyasından alınır.

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

### -GirdiDosyası
Yeni yetkilendirme kuralı için yapılandırma bilgilerini içeren bir JSON dosyasının yolunu belirtir.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Yetkilendirme kurallarının atanacağı ad boşluğunu belirtir.
Ad alanları, Bildirim Hub 'larının gruplamak ve kategorilere ayırmak için bir yol sağlar.
Yeni kuralların varolan bir ad alanına atanması gerekir.
**Yeni-AzNotificationHubsNamespaceAuthorizationRule** cmdlet 'i yeni bir ad alanı oluşturamaz.

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
Var olan bir kaynak grubunu kullanmalısınız.
Bu cmdlet yeni bir kaynak grubu oluşturamıyor.

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

### -SASRule
Yeni kuralların yapılandırma bilgilerini içeren **Sharedaccessauthorizationruleattributes** nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Notificationhub. modeller. SharedAccessAuthorizationRuleAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


