---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLog.md
ms.openlocfilehash: 9b57d7584ee7720ec73aa57ddec070ad26ddff9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109538"
---
# Get-AzActivityLog

## SYNOPSIS
Etkinlik günlüğü olaylarını alma.

## INDEKI

### Getbybağıntıkimliği
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-CorrelationId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Getbyresourceıd
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceId] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceGroup
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceGroupName] <String> [-MaxRecord <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceProvider
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-ResourceProvider] <String> [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetBySubscription
```
Get-AzActivityLog [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>] [-Caller <String>]
 [-DetailedOutput] [-MaxRecord <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzActivityLog cmdlet etkinlik günlüğü olaylarını alır. Olaylar geçerli abonelik KIMLIĞI, bağıntı KIMLIĞI, kaynak grubu, kaynak KIMLIĞI veya kaynak sağlayıcısıyla ilişkilendirilebilir.

## ÖRNEKLERDEN

### Örnek 1: abonelik KIMLIĞINE göre olay günlüğü alma
```
PS C:\>Get-ActivityAzLog
```

Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili, geçerli tarih/saatten 7 gün kadar geçen 1000 olaylarını listeler.

### Örnek 2: en fazla etkinlik sayısına göre bir abonelik KIMLIĞI olay günlüğü alma
```
PS C:\>Get-AzActivityLog -MaxRecord 100
```

Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili, geçerli tarih/saatten 7 gün kadar geçen 100 olaylarını listeler.

### Örnek 3: başlangıç saati olan abonelik KIMLIĞINE göre olay günlüğü alma.
```
PS C:\>Get-AzActivityLog -StartTime 2017-06-01T10:30
```

Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili olan en çok 1000 olayı, bu tarih/saat geçerli tarih/saat 90 günden daha eski bir tarih/saatten daha eski bir tarih

### Örnek 4: başlangıç saati ve bitiş saati olan abonelik KIMLIĞINE göre olay günlüğü alma.
```
PS C:\>Get-AzActivityLog -StartTime 2017-04-01T10:30 -EndTime 2017-04-14T11:30
```

Bu komut, kullanıcının abonelik KIMLIĞIYLE ilişkili olan veya sonrasında 2017-04-01T10:30 yerel saat, öncesi ve öncesi 2017-04-14T11: tüm tarih/saat aralığının, geçerli tarih/saat 90 günden eski olmadığı durumlarda, (örneğin, bekletme dönemi) en çok 1000.

### Örnek 5: bağıntı KIMLIĞINE göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23"
```

Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen korelasyon KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler. 
**Not** : Bu genellikle yalnızca bir olaydır.

### Örnek 6: en fazla etkinlik sayısı
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -MaxRecord 100
```

Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen korelasyon KIMLIĞIYLE ilişkilendirilmiş en çok 100 olayı listeler. 
**Not** : Bu genellikle yalnızca bir olaydır.

### Örnek 7: bağıntı KIMLIĞINE ve başlangıç saatine göre bir olay günlüğü alma
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-05-22T04:30:00
```

Bu komut, 2017-05-22T04 tarihinde veya ondan sonraki belirtilen bağıntı KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.
**Not** : Bu genellikle yalnızca bir olaydır.

### Örnek 8: başlangıç zamanı ve bitiş saati olan bağıntı KIMLIĞINE göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -CorrelationId "60c694d0-e46f-4c12-bed1-9b7aef541c23" -StartTime 2017-04-15T04:30:00 -EndTime 2017-04-25T12:30:00
```

Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen bağıntı KIMLIĞIYLE ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).

### Örnek 9: kaynak grubu için olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceGroupName "Contoso-Web-CentralUS"
```

Bu komut en çok 1000, geçerli tarih/saatten 7 gün sonraki belirtilen kaynak grubuyla ilişkili olayları listeler.

### Örnek 10: en fazla etkinlik sayısına sahip kaynak grubu için olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -MaxRecord 100
```

Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak grubuyla ilişkilendirilmiş en çok 100 olayı listeler.

### Örnek 11: başlangıç zamanına göre bir kaynak grubu için olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-05-22T04:30:00
```

Bu komut, 2017-05-22T04 tarihinde veya bu tarihten sonra gerçekleşen belirtilen kaynak grubuyla ilişkili en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.

### Örnek 12: başlangıç saati ve bitiş saati olan bir kaynak grubu için olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceGroup "Contoso-Web-CentralUS" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen kaynak grubuyla ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).

### Örnek 13: kaynak KIMLIĞINE göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1"
```

Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler.

### Örnek 14: en fazla etkinlik sayısına göre bir olay günlüğü kaynak KIMLIĞINE göre alma
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -MaxRecord 100
```

Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 100 olayı listeler.

### Örnek 15: başlangıç saati olan kaynak KIMLIĞINE göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-05-22T04:30
```

Bu komut, %05-22T04 tarihinde veya bu tarihten sonra, belirtilen kaynak KIMLIĞIYLE ilişkilendirilmiş en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.

### Örnek 16: başlangıç saati ve bitiş saati olan kaynak KIMLIĞINE göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceId "/subscriptions/623d50f1-4fa8-4e46-a967-a9214aed43ab/ResourceGroups/Contoso-Web-CentralUS/providers/Microsoft.Web/ServerFarms/Contoso1" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Bu komut, 2017-04-15T04 ' ye dayalı olarak belirtilen kaynak KIMLIĞIYLE ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tüm tarih/saat aralığının geçerli tarih/saat 90 günden daha eski olmadığı durumlarda (örneğin, bekletme dönemi).

### Örnek 17: kaynak sağlayıcıya göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web"
```

Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak sağlayıcısıyla ilişkilendirilmiş en çok 1000 olayı listeler.

### Örnek 18: en fazla etkinlik sayısı olan kaynak sağlayıcıya göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -MaxRecord 100
```

Bu komut, geçerli tarih/saatten 7 gün sonra belirtilen kaynak sağlayıcısıyla ilişkilendirilmiş en çok 100 olayı listeler.

### Örnek 19: başlangıç zamanı olan kaynak sağlayıcıya göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-05-22T04:30
```

Bu komut, %05-22T04 tarihinde veya ondan sonra, belirtilen kaynak sağlayıcıyla ilişkili en çok 1000 olayı listeler ve başlangıç zamanı geçerli tarih/saatten 90 günden eski değilse, yerel saat.

### Örnek 20: başlangıç saati ve bitiş saati olan kaynak sağlayıcıya göre olay günlüğü alma
```
PS C:\>Get-AzActivityLog -ResourceProvider "Microsoft.Web" -StartTime 2017-04-15T04:30 -EndTime 2017-04-25T12:30
```

Bu komut, 2017-04-15T04 ' i n i n-04-15T04 ' ye geçen belirtilen kaynak sağlayıcıyla ilişkili en çok 1000 olayı listeler, ancak önce 2017-04-25T12: tam 90 Tarih

## PARAMETRELERINE

### Arayan
Getirilecek olayları arayan

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bağıntıkimliği
Bağıntıkimliği

```yaml
Type: System.String
Parameter Sets: GetByCorrelationId
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DetailedOutput
Olayların tüm ayrıntılarını içeren dönüş nesnesi (varsayılan olarak yalnızca bazı öznitelikleri döndürmeli; Yani, ayrıntı yok)

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bitişsaati
Sorgunun bitişsaati

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxRecord
Getirilecek en fazla kayıt sayısı.
Diğer ad: MaxRecords, MaxEvents

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
RESOURCEID

```yaml
Type: System.String
Parameter Sets: GetByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceProvider
ResourceProvider adı

```yaml
Type: System.String
Parameter Sets: GetByResourceProvider
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Başlangıçsaati
Sorgunun Bağıntıkimliği

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Durum
Getirilecek olayların durumu

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

### System. String

### System. Management. Automation. SwitchParameter

### System. Int32

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Insights. OutputClasses. PSEventData

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
