---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105426"
---
# Start-AzureSqlDatabaseRestore

## SYNOPSIS
Bir veritabanının zaman içinde geri yüklenmesini gerçekleştirir.

## INDEKI

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Start-AzureSqlDatabaseRestore** cmdlet 'i temel, standart veya Premium veritabanının zaman içinde geri yüklemesini gerçekleştirir.
Azure SQL veritabanı, temel veritabanı yedeklemelerini 7 gün, 14 gün için standart ve 35 gündür Premium korur.
Geri yükleme işlemi yeni bir veritabanı oluşturur.
Kaynak veritabanı silinmişse, *SourceDatabaseName* ve *TargetDatabaseName* parametresinde farklı değerler olmalıdır.

Azure SQL veritabanı şu anda çapraz sunucu geri yüklemeyi desteklemiyor.
Kaynak ve hedef sunucu adları aynı olmalıdır.

## ÖRNEKLERDEN

### Örnek 1: nesne olarak belirtilen veritabanını zaman bir noktaya geri yükleme
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

İlk komut, server01 adındaki sunucuda Database17 adlı veritabanı için bir veritabanı nesnesi alır ve $Database değişkeninde depolar.

İkinci komut, veritabanını belirli bir zaman noktasına geri yükler.
Bu komut yeni veritabanının adını belirtir.

### Örnek 2: adla belirtilen bir veritabanını zaman bir noktaya geri yükleme
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

Bu komut, Database17 adlı veritabanını belirli bir zaman içinde geri yükler.
Bu komut yeni veritabanının adını belirtir.

### Örnek 3: nesne olarak belirtilen bırakılmış veritabanını zaman bir noktaya geri yükleme
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

İlk komut, server01 adındaki sunucuda Database01 adlı veritabanı için bir veritabanı nesnesi alır.
Komut geri *yüklenebilen* parametreyi belirtir.
Bu nedenle, cmdlet geri yüklenebilen bir veritabanını belirtilen geri yükleme noktasına alır.
Komut, veritabanı nesnesini $Database değişkeninde depolar.

İkinci komut $Database tarafından belirtilen bırakılmış veritabanını geri yükler.
Bu komut yeni veritabanının adını belirtir.

## PARAMETRELERINE

### -Pointıntime
Veritabanının geri yükleneceği geri yükleme noktasını belirtir.
Geri yükleme işlemi bittiğinde veritabanı, bu parametrenin belirttiği tarih ve saat olan durumuna geri yüklenir.
Varsayılan olarak, bu geçerli saate ayarlanan canlı bir veritabanı için ve bırakılan bir veritabanı için, bu cmdlet veritabanının bırakılmadığı zamanı kullanır.

```yaml
Type: DateTime
Parameter Sets: (All)
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

### -Geri yüklenebilen
Bu cmdlet 'in geri yüklenebilen bir veritabanını geri aldığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabase
Bu cmdlet 'in geri belirttiği veritabanının adını belirtir.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
Veritabanının silindiği tarih ve saati belirtir.
Gerçek veritabanı silme zamanına uygun zamanı belirttiğinizde milisaniyeyi belirtmeniz gerekir.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Bu cmdlet 'in geri belirttiği canlı veritabanının adını belirtir.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
Bu cmdlet 'in geri bildirdiği geri yüklenebilen veritabanını temsil eden bir nesne belirtir.
**Restorabledroppeddatabase** nesnesi almak için Get-AzureSqlDatabase cmdlet 'ini kullanın ve yeniden *stoklama* parametresini belirtin.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
Kaynak veritabanının canlı ve çalışıyor olduğu veya kaynak veritabanının silinmeden önce çalıştığı sunucunun adını belirtir.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Geri yükleme işleminin oluşturduğu yeni veritabanının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
Bu cmdlet 'in veritabanını geri yüklediğinde sunucunun adını belirtir.

Azure SQL veritabanı şu anda çapraz sunucu geri yüklemeyi desteklemiyor.
Kaynak ve hedef sunucu adları aynı olmalıdır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

## ÇıKıŞLAR

### Microsoft. Windowsazve. Commands. SqlDatabase. Services. Server. Restoredatabaseişlemi

## NOTLARıNDA
* Bu cmdlet 'i çalıştırmak için sertifika tabanlı kimlik doğrulaması kullanmalısınız. Bu cmdlet 'i çalıştıran bilgisayarda aşağıdaki komutları çalıştırın: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Veritabanı geri yükleme Isteği oluşturma](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqldatabase](./Get-AzureSqlDatabase.md)


