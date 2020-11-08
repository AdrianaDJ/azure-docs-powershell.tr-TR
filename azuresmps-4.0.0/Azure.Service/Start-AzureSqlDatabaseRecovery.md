---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105423"
---
# Start-AzureSqlDatabaseRecovery

## SYNOPSIS
Veritabanı için geri yükleme isteği başlatır.

## INDEKI

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Start-AzureSqlDatabaseRecovery** cmdlet 'i canlı veya bırakılmış bir veritabanı için geri yükleme isteği başlatır.
Bu cmdlet, veritabanında bilinen son kullanılabilir yedeği kullanan temel kurtarmayı destekler.
Kurtarma işlemi yeni bir veritabanı oluşturur.
Bir Live veritabanını aynı sunucuda kurtarmanız durumunda, yeni veritabanı için farklı bir ad belirtmeniz gerekir.

Bir veritabanı için zaman içinde bir nokta geri yükleme yapmak istiyorsanız, bunun yerine **Start-AzureSqlDatabaseRestore** cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: nesne olarak belirtilen veritabanını kurtarma
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

İlk komut **Get-Azuresılrecoverrecoverabledatabase** cmdlet 'ini kullanarak bir veritabanı nesnesi alır.
Komut bu nesneyi $Database değişkeninde depolar.

İkinci komut $Database depolanan veritabanını kurtarır.

### Örnek 2: adla belirtilen bir veritabanını kurtarma
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

Bu komut, veritabanı adını kullanarak veritabanını kurtarır.

## PARAMETRELERINE

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

### -SourceDatabase
Bu cmdlet 'in kurtarakullandığı veritabanını temsil eden veritabanı nesnesini belirtir.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
Bu cmdlet 'in kurtarakullandığı veritabanının adını belirtir.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
Kaynak veritabanının canlı ve çalışıyor olduğu veya kaynak veritabanının silinmeden önce çalıştığı sunucunun adını belirtir.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Kurtarılan veritabanının adını belirtir.
Kaynak veritabanı hala canlı durumdaysa, aynı sunucuya kurtarmak için kaynak veritabanı adından farklı bir ad belirtmeniz gerekir.

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

### -TargetServerName
Veritabanının geri yükleneceği sunucunun adını belirtir.
Bir veritabanını aynı sunucuya veya farklı bir sunucuya geri yükleyebilirsiniz.

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

### Microsoft. Windowsazme. Management. Sql. modeller. RecoverableDatabase

## ÇıKıŞLAR

### Microsoft. Windowsazve. Management. Sql. modeller. RecoverDatabaseOperation

## NOTLARıNDA
* Bu cmdlet 'i çalıştırmak için sertifika tabanlı kimlik doğrulaması kullanmalısınız. Bu cmdlet 'i çalıştırdığınız bilgisayarda aşağıdaki komutları çalıştırın: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Veritabanı kurtarma Isteği oluşturma](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Azure SQL veritabanında coğrafi çoğaltma](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqlrecoverabledatabase](./Get-AzureSqlRecoverableDatabase.md)

[Start-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


