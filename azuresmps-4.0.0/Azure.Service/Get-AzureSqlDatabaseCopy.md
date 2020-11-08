---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106295"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
İlişki kopyalama durumunu denetler.

## INDEKI

### ByServerNameOnly (varsayılan)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-azures, Databasecopy** cmdlet 'i bir veya daha fazla etkin kopya ilişkisinin durumunu denetler.
Start-AzureSqlDatabaseCopy veya Stop-AzureSqlDatabaseCopy cmdlet 'ini çalıştırdıktan sonra bu cmdlet 'i çalıştırın.
Belirli bir kopya ilişkisini, tüm kopya ilişkilerini veya belirli bir hedef sunucudaki tüm kopyalar gibi kopyalama ilişkilerinin filtrelenmiş listesini denetleyebilirsiniz.
Bu cmdlet 'i kaynak veya hedef veritabanını barındıran sunucuda çalıştırabilirsiniz.

Bu cmdlet zaman uyumludur.
Cmdlet, bir durum nesnesi döndürdüğünden Azure PowerShell konsolunu engeller.

*PartnerServer* ve *partnerdatabase* parametreleri isteğe bağlıdır.
Parametre belirtmezseniz, bu cmdlet bir sonuç tablosu döndürür.
Yalnızca belirli bir veritabanının durumunu görmek için her iki parametreyi de belirtin.

## ÖRNEKLERDEN

### Örnek 1: veritabanının kopyalama durumunu alma
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

Bu komut, lpqd0zbr8y adlı sunucudaki Siparişler adlı veritabanının durumunu alır.
*PartnerServer* parametresi bu komutu bk0b8kf658 sunucusuyla sınırlar.

### Örnek 2: sunucudaki tüm kopyaların durumunu alma sunucudaki tüm kopyaların durumunu alma
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

Bu komut, lpqd0zbr8y adındaki sunucudaki tüm etkin kopyaların durumunu alır.

## PARAMETRELERINE

### -Veritabanı
Kaynak Azure SQL veritabanını temsil eden bir nesne belirtir.
Bu cmdlet, bu parametrenin belirttiği veritabanının kopyalama durumunu alır.

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
Bu cmdlet, bu parametrenin belirttiği veritabanının kopyalama durumunu alır.
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
Kaynak veritabanının adını belirtir.
Bu cmdlet, bu parametrenin belirttiği veritabanının kopyalama durumunu alır.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
İkincil veritabanının adını belirtir.
Bu veritabanı sys.dm_database_copies dinamik yönetim görünümünde bulunmazsa, bu cmdlet boş bir durum nesnesi döndürür.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
Hedef veritabanını barındıran sunucunun adını belirtir.
Bu sunucu sys.dm_database_copies dinamik yönetim görünümünde bulunmazsa, bu cmdlet boş bir durum nesnesi döndürür.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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
Veritabanı kopyasının bulunduğu sunucunun adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Windowsazve. Commands. SqlDatabase. model. DatabaseCopy

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

## ÇıKıŞLAR

### Microsoft. Windowsazve. Commands. SqlDatabase. model. DatabaseCopy

## NOTLARıNDA
* Kimlik doğrulama: Bu cmdlet, sertifika tabanlı kimlik doğrulama gerektirir. Geçerli aboneliği ayarlamak için sertifika tabanlı kimlik doğrulamanın nasıl kullanılacağına ilişkin bir örnek için New-AzureSqlDatabaseServerContext cmdlet bölümüne bakın.

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Azure SQL veritabanı cmdlet 'Leri](./Azure.SQLDatabase.md)

[Start-Azuressqldatabasecopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-Azuresurdatabasecopy](./Stop-AzureSqlDatabaseCopy.md)


