---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespace.md
ms.openlocfilehash: 24a42fba23427f437cb064e1915c19e36e7a71bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323182"
---
# New-AzNotificationHubsNamespace

## SYNOPSIS
Bildirim Merkezi ad alanı oluşturur.

## INDEKI

```
New-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**New-AzNotificationHubsNamespace** cmdlet 'i bir bildirim merkezi ad alanı oluşturur.
Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.
En az bir Bildirim Hub ad alanınız olmalıdır.
Tek bir ad alanı birden çok hub 'ı oluşturabilir.
Hub 'larınızı düzenlemek veya belirli kişilere, hub 'larınızın seçili alt kümesini yönetme izni vermek için birden fazla ad alanınız olabilir.
Ad alanı oluşturmak için, ad alanı için benzersiz bir ad belirttiğinizden emin olun; ad alanının yerleştirileceği veri merkezi 'ni belirtin; ve ad alanının atanacağı kaynak grubunu belirtin.
Ad alanı oluşturulduktan sonra, bu ad alanına yetkilendirme kuralları atamak için New-AzNotificationHubsNamespaceAuthorizationRules cmdlet 'ini kullanabilirsiniz.
Kimlik alanı izinlerini yönetmek için yetkilendirme kuralları kullanılır.

## ÖRNEKLERDEN

### Örnek 1: bildirim merkezi oluşturma
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

Bu komut, ContosoPartners adlı bir bildirim merkezi oluşturur.
Ad alanı Batı ABD veri merkezinde yer alır ve ContosoNotificationsGroup kaynak grubuna atanır.

### Örnek 2: etiketlerle bildirim merkezi oluşturma
```
PS C:\>New-AzNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

Bu komut, ContosoPartners adlı bir bildirim merkezi oluşturur.
Ad alanı Batı ABD veri merkezinde yer alır ve ContosoNotificationsGroup kaynak grubuna atanır.
Buna ek olarak, bu komut ad Izleyicisine sahip bir etiket oluşturur ve bu da isim uzayına atanır.
Bu, hedef kitle etiketinin Partnerkuruluşları olarak ayarlandığı öğeleri filtrelediğinizde, ad alanının gösterilmesini sağlar.

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

### -Konum
Ad alanını barındıracak veri merkezinin görünen adını belirtir.
Bu parametreyi geçerli bir konuma ayarlayabilirsiniz, ancak en iyi performans için kullanıcılarınızın çoğunluğunda bulunan bir veri merkezi 'ni kullanmak isteyebilirsiniz.

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

### -Namespace
Yeni ad alanının adını belirtir.
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

### -ResourceGroup
Ad alanının atanacağı kaynak grubunu belirtir.
Kaynak grupları, ad alanları, Bildirim Hub 'ları ve yetkilendirme kuralları gibi öğeleri, yalnızca envanter yönetimi ve yönetimle ilgili yollarla düzenler.

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

### -SkuTier
Ad alanının SKU katmanı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Azure öğelerini kategorilere ayırmak ve düzenlemek için kullanılabilecek ad değeri çiftlerini belirtir.
Etiketler, anahtar sözcüklere benzer ve bir dağıtımda çalışır.
Örneğin, etiket departmanı olan tüm öğeleri arıyorsanız, öğe türü, konum veya kaynak grubu gibi öğelere bakılmaksızın, arama bu etikete sahip tüm Azure öğelerini döndürür.
Tek bir etiket iki bölümden oluşur: *ad* ve isteğe bağlı olarak *değer*.
Örneğin, departmandaki bölüm, etiket adı bölümdedir ve etiket değeri olur.
Etiket eklemek için, CalendarYear: 2016 etiketini oluşturan buna benzer karma tablo söz dizimini kullanın:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)

[Set-AzNotificationHubsNamespace](./Set-AzNotificationHubsNamespace.md)


