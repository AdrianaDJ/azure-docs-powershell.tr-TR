---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: c367c4b4f7ebe7c9d6d51b832eed22249f262864
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322222"
---
# Set-AzNotificationHubsNamespace

## SYNOPSIS
Bildirim Merkezi ad alanı için özellik değerlerini ayarlar.

## INDEKI

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzNotificationHubsNamespace** cmdlet 'i var olan bir Bildirim Hub ad alanının özellik değerlerini ayarlar.
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
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

Bu komut, Batı ABD veri merkezinde bulunan ContosoPartners adındaki ve ContosoNotificationsGroup kaynak grubuna atanmış olan ad alanını devre dışı bırakır.

### Örnek 2: ad alanını etkinleştirme
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
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
Azure konumlarının güncel listesini almak için aşağıdaki komutu çalıştırırsınız: `Get-AzLocation | Select-Object DisplayName`

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

### Etiketli
Azure öğelerini kategorilere ayırmak ve düzenlemek için kullanılabilecek ad değeri çiftlerini belirtir.
Etiketler, anahtar sözcüklere benzer ve bir dağıtımda çalışır.
Örneğin, etiket departmanı olan tüm öğeleri arıyorsanız, öğe türü, konum veya kaynak grubu gibi öğelere bakılmaksızın, arama bu etikete sahip tüm Azure öğelerini döndürür.
Tek bir etiket iki bölümden oluşur: *ad* ve (isteğe bağlı olarak) *değer*.
Örneğin, departmandaki bölüm, etiket adı bölümdedir ve etiket değeri olur.
Etiket eklemek için, CalendarYear: 2016:-Tags @ {Name = "CalendarYear" etiketini oluşturan buna benzer karma tablo söz dizimini kullanın; Value = "2016"} aynı komutta birden çok etiket eklemek Için, etiketleri virgülle ayırın:-Tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "Fcalyear"; Value = "2017"}

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceState

### System. Boolean

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Notificationhub. modeller. NamespaceAttributes

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[New-AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


