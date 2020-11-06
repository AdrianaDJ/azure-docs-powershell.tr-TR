---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/Set-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: 90fbdc94c372cbe02aaecde4ff27ad28dcec8e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589194"
---
# Set-AzureRmNotificationHubsNamespace

## SYNOPSIS
Bildirim Merkezi ad alanı için özellik değerlerini ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tags] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmNotificationHubsNamespace** cmdlet 'i var olan bir Bildirim Hub ad alanının özellik değerlerini ayarlar.

Ad alanları, Bildirim Hub 'larınızı düzenlemenize ve yönetmenize yardımcı olan mantıksal kapsayıcılardır.
En az bir Bildirim Hub ad alanınız olmalıdır.
Ayrıca, tüm Bildirim Hub 'larının atanmış bir ad alanı olmalıdır.

Bu cmdlet öncelikle ad alanını etkinleştirmek ve devre dışı bırakmak için kullanılır.
Bir ad alanı devre dışı bırakıldığında, kullanıcılar ad alanındaki Bildirim Hub 'larına herhangi birine bağlanamaz ve bu hub 'ları kullanarak anında iletme bildirimleri gönderebilir.
Devre dışı bırakılmış bir ad alanını yeniden etkinleştirmek için, bu cmdlet 'i kullanarak ad uzayının **State** özelliğini etkin olarak ayarlayın.

Bu cmdlet 'i, bir ad alanını kritik olarak etiketlemek için de kullanabilirsiniz.
Bu, ad alanının silinmesini engeller.
Kritik bir ad alanını kaldırmak için önce kritik etiketini kaldırmalısınız.

## ÖRNEKLERDEN

### Örnek 1: ad alanını devre dışı bırakma
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Bu komut, Batı ABD veri merkezinde bulunan ContosoPartners adındaki ve ContosoNotificationsGroup kaynak grubuna atanmış olan ad alanını devre dışı bırakır.

### Örnek 2: ad alanını etkinleştirme
```
PS C:\>Set-AzureRmNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

Bu komut, Batı ABD veri merkezinde bulunan ContosoPartners adlı ve ContosoNotificationsGroup kaynak grubuna atanmış olan ad alanını etkinleştirmiştir.

## PARAMETRELERINE

### -Kritik
Ad alanının kritik bir ad alanı olup olmadığını gösterir.
Kritik ad alanları silinemez.
Kritik bir ad alanını silmek için, bu özelliğin değerini false olarak ayarlamanız gerekir ve ad alanını kritik olmayan olarak işaretlemektir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Onay sorma.

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

### -Konum
Ad alanını barındıran veri merkezinin görünen adını belirtir.
Bu parametreyi geçerli bir Azure konumuna ayarlayabilirsiniz, ancak en iyi performans için kullanıcılarınızın çoğunluğunda bulunan bir veri merkezi kullanmalısınız.

Azure konumlarının güncel listesini almak için aşağıdaki komutu çalıştırırsınız:

`Get-AzureLocation | Select-Object DisplayName`

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
Bu cmdlet 'in değiştirdiği ad boşluğunu belirtir.

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

### Durumlu
Ad alanının geçerli durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır: etkin ve devre dışı.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Etiketler
Azure öğelerini kategorilere ayırmak ve düzenlemek için kullanılabilecek ad değeri çiftlerini belirtir.
Etiketler, anahtar sözcüklere benzer ve bir dağıtımda çalışır.
Örneğin, etiket departmanı olan tüm öğeleri arıyorsanız, öğe türü, konum veya kaynak grubu gibi öğelere bakılmaksızın, arama bu etikete sahip tüm Azure öğelerini döndürür.

Tek bir etiket iki bölümden oluşur: *ad* ve (isteğe bağlı olarak) *değer*.
Örneğin, departmandaki bölüm, etiket adı bölümdedir ve etiket değeri olur.
Etiket eklemek için, CalendarYear: 2016 etiketini oluşturan buna benzer karma tablo söz dizimini kullanın:

-Etiketler @ {Name = "Takvimyılı"; Value = "2016"}

Aynı komutta birden çok etiket eklemek için, etiketleri virgülle ayırın:

-Tag @ {Name = "Takvimyılı"; Value = "2016"}, @ {Name = "Fcalyear"; Value = "2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
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

### Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[New-AzureRmNotificationHubsNamespace](./New-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)


