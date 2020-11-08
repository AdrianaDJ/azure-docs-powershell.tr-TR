---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106403"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
Sürekli bir kopya ilişkisini sonlandırır.

## INDEKI

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### VeritabanıAdı
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Stop-Azuresurdatabasecopy** cmdlet 'i sürekli bir kopyalama ilişkisini sonlandırır.
Bu cmdlet, kaynak veritabanı ile ikincil veya hedef veritabanı arasındaki veri hareketini durdurur ve ikincil veritabanının durumunu tek başına bir çevrimiçi veritabanı olacak şekilde değiştirir.

Sürekli bir kopya ilişkisini, sonlandırmasını veya planlı sonlandırmayı ve olası veri kaybına karşı zorla sonlandırmanın iki yolu vardır.
Kaynak veritabanını barındıran sunucuda bu cmdlet 'i sonlandırma veya zorunlu sonlandırma modunda çalıştırabilirsiniz.
İkincil veritabanını barındıran sunucuda Zorlanmış sonlandırma modunu kullanmalısınız.

Bir planlı sonlandırma, kaynak veritabanındaki tüm teslim edilen işlemlerin, cmdlet 'i çalıştırdığınız sırada ikincil veritabanına çoğaltıldığını belirten şekilde bekler.
Zorunlu sonlandırma, bekleyen kaydedilmiş işlemlerin çoğaltılmasını beklemez ve ikincil veritabanında olası veri kaybına neden olabilir.

Çoğaltma durumu beklemede olduğunda, sürekli bir kopya ilişkisini başarıyla sonlandırabilir.
Çoğaltma durumu beklemede olduğunda, zorunlu olmayan sonlandırma desteklenmez.

## ÖRNEKLERDEN

### Örnek 1: sürekli bir kopya ilişkisini sonlandırma
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Bu komut, lpqd0zbr8y adlı sunucudaki veritabanı adlı siparişlerin sürekli kopyalama ilişkisini sonlandırır.
Bk0b8kf658 adındaki sunucu ikincil veritabanını barındırır.

### Örnek 2: sürekli bir kopya ilişkisini zorla sonlandırma
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

İlk komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanı için veritabanı kopyalama ilişkisini alır.

İkinci komut, ikincil veritabanını barındıran sunucudan sürekli bir kopya ilişkisini zorla sonlandırır.

## PARAMETRELERINE

### -Veritabanı
Kaynak Azure SQL veritabanını temsil eden bir nesne belirtir.
Bu cmdlet, bu parametrenin belirttiği veritabanının sürekli kopyalama ilişkisini sonlandırır.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
Veritabanını temsil eden bir nesne belirtir.
Bu cmdlet, bu parametrenin belirttiği veritabanının sürekli kopyalama ilişkisini sonlandırır.
Bu parametre kanal girişini kabul eder.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Veritabanının adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veritabanının sürekli kopyalama ilişkisini sonlandırır.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Forcevseçişten çıkarma
Bu cmdlet 'in sürekli kopyalama ilişkisinin zorunlu olarak sonlandırılmasına neden olduğunu gösterir.
Zorunlu sonlandırma veri kaybına neden olabilir.
Bu cmdlet 'i hedef veritabanını barındıran bir sunucuda çalıştırmak için bu parametreyi belirtmeniz gerekir.
Bu cmdlet 'i kaynak veritabanını barındıran bir sunucuda çalıştırmak için, ikincil veritabanı kullanılamıyorsa bu parametreyi belirtmeniz gerekir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
İkincil veritabanının adını belirtir.
Bir ad belirtirseniz, kaynak veritabanının adıyla eşleşmelidir.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Hedef veritabanını barındıran sunucunun adını belirtir.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Kaynak veritabanının bulunduğu sunucunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Windowsazve. Commands. SqlDatabase. model. DatabaseCopy

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

## ÇıKıŞLAR

### Yabilirsiniz

## NOTLARıNDA
* Kimlik doğrulama: Bu cmdlet, sertifika tabanlı kimlik doğrulama gerektirir. Geçerli aboneliği ayarlamak için sertifika tabanlı kimlik doğrulamanın nasıl kullanılacağına ilişkin bir örnek için, **New-Azuressqldatabaseservercontext** cmdlet 'ine bakın.
* Kısıtlamalar: ikincil veritabanını barındıran sunucuda, yalnızca zorunlu sonlandırma desteklenir.
* Eski ikincil veritabanında sonlandırma etkisi: sonlandırıldıktan sonra, ikincil veritabanı bağımsız bir veritabanı olur. İkinci veritabanında dengeli dağıtım işlemi tamamlandıktan sonra, bu veritabanı tam erişim için açılır. Kaynak veritabanı bir okuma-yazma veritabanıdır, eski ikincil veritabanı da okuma-yazma veritabanı olur.

  Dengeli dağıtım devam ediyorsa, dengeli dağıtım durdurulur ve eski ikincil veritabanı ikincil veritabanını barındıran sunucuda hiçbir zaman görünmez duruma geçmez.

* Kaynak veritabanını salt okunur moduna getirebilirsiniz. Bu, kaynak ve ikincil veritabanlarının işten çıkarıldıktan sonra eşitlenmesini ve sonlandırma sırasında hiçbir hareketin tutulmamasını sağlar. Sonlandırma işlemi tamamlandıktan sonra, kaynağı tekrar okuma moduna ayarlayın. İsteğe bağlı olarak, eski ikincil veritabanını okuma yazma moduna da ayarlayabilirsiniz.
* İzleme: işlemlerin durumunu sürekli kopyalama ilişkisinin hem kaynağına hem de hedeften doğrulamak Için **Get-Azuressqldatabaseoperation** cmdlet 'ini kullanın.

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Veritabanını Kopyalamayı durdur](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Azure SQL veritabanı cmdlet 'Leri](./Azure.SQLDatabase.md)

[Get-Azuressqldatabasecopy](./Get-AzureSqlDatabaseCopy.md)

[Start-Azuressqldatabasecopy](./Start-AzureSqlDatabaseCopy.md)


