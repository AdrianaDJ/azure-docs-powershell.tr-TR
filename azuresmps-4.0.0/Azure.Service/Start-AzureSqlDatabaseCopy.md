---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105845"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Azure SQL veritabanının kopyalama işlemini başlatır.

## INDEKI

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Byinputobjectdevamlı
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VeritabanıAdı
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Start-azures, Databasecopy** cmdlet 'i bir kerelik bir kopya işlemi başlatır veya belirli BIR Azure SQL veritabanının sürekli kopyalama işlemini başlatır.
Bu cmdlet işlem değildir.

Özgün veritabanı kaynak veritabanıdır.
Kopya ikincil veya hedef veritabanıdır.
Sürekli bir kopyada, kaynak ve hedef veritabanları aynı sunucuda yer alamaz ve kaynak ve hedef veritabanlarını barındıran sunucular aynı aboneliğin bir parçası olmalıdır.

*ContinuousCopy* parametresini belirtmezseniz, bu cmdlet kaynak veritabanının tek seferlik bir kopyasını oluşturur.
Yanıt alındığında işlem hala devam ediyor olabilir.
Get-AzureSqlDatabaseCopy veya Get-AzureSqlDatabaseOperation cmdlet 'ini kullanarak işlemi izleyebilirsiniz.

*ContinuousCopy* belirtirseniz, bu cmdlet kaynak veritabanının sürekli bir kopyasını oluşturur.
Yanıt alındığında işlem devam eder.
**Get-azures, Databasecopy** veya **Get-azuressqldatabaseoperation** kullanarak işlemi izleyebilirsiniz.

Çevrimiçi veya çevrimdışı veritabanı olarak sürekli bir kopya oluşturabilirsiniz.
Çevrimiçi sürekli kopya, Azure SQL veritabanı için Active Geo-Replication Directory 'yi yapılandırmak için kullanılır https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
Çevrimdışı sürekli kopya, Azure SQL veritabanı için standart Geo-Replication yapılandırmak için kullanılır https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## ÖRNEKLERDEN

### Örnek 1: sürekli bir veritabanı kopyası zamanlama
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

Bu komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanının sürekli bir kopyasını zamanlar.
Komut, bk0b8kf658 adlı sunucuda bir hedef veritabanı oluşturur.

### Örnek 2: aynı sunucuda bir kerelik bir kopya oluşturma
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

Bu komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanının tek seferlik bir kopyasını oluşturur.
Bu komut aynı sunucuda OrdersCopy adlı bir kopya oluşturur.

### Örnek 3: sürekli bir çevrimdışı veritabanı kopyası zamanlama
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

Bu komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanının sürekli bir kopyasını zamanlar.
Bu komut, bk0b8kf658 adlı sunucuda bir çevrimdışı hedef veritabanı oluşturur.

## PARAMETRELERINE

### -ContinuousCopy
Veritabanı kopyasının sürekli kopya olacağını (yineleme veritabanı) gösterir.
Aynı sunucuda sürekli kopyalama desteklenmez.
Bu parametre belirtilmezse, bir kerelik kopya gerçekleştirilir.
Bir kerelik bir kopyada, kaynak ve iş ortağı veritabanları aynı sunucuda olmalıdır.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Veritabanı
Kaynak Azure SQL veritabanını temsil eden bir nesne belirtir.
Bu parametre kanal girişini kabul eder.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Kaynak veritabanının adını belirtir.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
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

### -OfflineSecondary
Etkin bir kopya yerine sürekli bir kopyanın pasif kopya olduğunu belirtir.
Kaynak veritabanı Standard Edition veritabanıdır, bu parametre gereklidir.
Bu parametre belirtilirse, *ContinuousCopy* de belirtilmelidir.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
Hedef veritabanının adını belirtir.
*ContinuousCopy* parametresini belirtirseniz, *partnerdatabase* değeri kaynak veritabanının adıyla eşleşmelidir.
*ContinuousCopy* belirtmezseniz, hedef veritabanı için kaynak veritabanı adından farklı olabilecek bir ad belirtmeniz gerekir.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Hedef veritabanını barındıran sunucunun adını belirtir.
Bu sunucunun kaynak veritabanı sunucusuyla aynı Azure aboneliği içinde olması gerekir.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
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

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

## ÇıKıŞLAR

### Microsoft. Windowsazve. Commands. SqlDatabase. model. DatabaseCopy

## NOTLARıNDA
* Kimlik doğrulama: Bu cmdlet, sertifika tabanlı kimlik doğrulama gerektirir. Geçerli aboneliği ayarlamak için sertifika tabanlı kimlik doğrulamanın nasıl kullanılacağına ilişkin bir örnek için New-AzureSqlDatabaseServerContext cmdlet bölümüne bakın.
* İzleme: sunucuda etkin bir veya daha fazla sürekli kopya ilişkisinin durumunu denetlemek Için **Get-Azuressqldatabasecopy** cmdlet 'ini kullanın. Sürekli kopyalama ilişkisinin hem kaynağı hem de hedefinin her ikisinde de işlemlerin durumunu doğrulamak için **Get-Azuressqldatabaseoperation** cmdlet 'ini kullanın.

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Veritabanı kopyasını başlatma](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Azure SQL veritabanı cmdlet 'Leri](./Azure.SQLDatabase.md)

[Get-Azuressqldatabasecopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-Azuresurdatabasecopy](./Stop-AzureSqlDatabaseCopy.md)


