---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106298"
---
# Get-AzureSqlDatabase

## SYNOPSIS
Bir veya daha fazla veritabanını alır.

## INDEKI

### ByConnectionContext (varsayılan)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-Azurestabanı** cmdlet 'i BIR Azure SQL veritabanı sunucusundan bir veya birden çok Azure SQL veritabanının örneğini alır.
Sunucuyu, **New-Azuressqldatabaseservercontext** cmdlet 'ini kullanarak oluşturduğunuz BIR Azure SQL veritabanı sunucusu bağlantı içeriğiyle belirtebilirsiniz.
Veya Azure SQL veritabanı sunucusu adını belirtirseniz cmdlet, sunucuya erişim isteğinin kimliğini doğrulamak için geçerli Azure aboneliği bilgilerini kullanır.

Bir veritabanı belirtmezseniz, **Get-Azurestabanı** cmdlet 'i belirtilen sunucudaki tüm veritabanlarını döndürür.

Geri yüklenebilen veritabanları alınıyor:

*Restorabledroburparameter* 'ı kullanarak geri yüklenebilen veritabanlarını alın.
Geri yüklenebilen tüm veritabanlarını döndürmek için *DatabaseName* ve *Databasedeletiondate* olmadan *restorabledroburparameter* 'ı kullanın.
Geri yüklenebilen belirli bir veritabanını geri yüklemek için, *DatabaseName* ve *Databasedeletiondate* parametreleriyle *restorabledroburparametresini* kullanın.
*DatabaseName* parametresini kullanarak geri yüklenebilen belirli bir veritabanını alırken, *databasedeletiondate* parametresini de eklemeniz gerekir ve belirtilen *databasedeletiondate* değeri, istenen veritabanıyla eşleşen milisaniyeyi içermelidir.

**Get-Azurestabanı** cmdlet 'i, bir sunucuda bırakılmış tüm geri yüklenebilir veritabanları veya hem *DatabaseName* hem de *databasedeletiondate* ile eşleşen belirli bir veritabanıdır.
Belirli bir adın geri yüklenebilen tüm veritabanları gibi farklı ölçütlere uyan geri yüklenebilen bırakılmış veritabanlarını geri yüklemek için, geri yüklenebilen tüm veritabanlarını geri iade etmelisiniz ve ardından sonuçları istemcide filtrelemelisiniz.

## ÖRNEKLERDEN

### Örnek 1: sunucudaki tüm veritabanlarını alma
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Bu komut, lpqd0zbr8y adındaki sunucudaki tüm veritabanlarını alır.

### Örnek 2: sunucuda bırakılan tüm geri yüklenebilen veritabanlarını alma
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

Bu komut, lpqd0zbr8y adlı sunucudaki tüm geri yüklenebilen veritabanlarını alır.

### Örnek 3: bağlantı bağlamında belirtilen sunucudan veritabanı alma
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Bu komut, Database01 adlı veritabanını bağlantı bağlamında belirtilen sunucudan alır $Context.

### Örnek 4: bir değişkende veritabanı nesnesini depolama
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Bu komut, Database01 adlı sunucudan gelen veritabanını alır.
Komut, veritabanı nesnesini $Database 01 değişkeninde depolar.

### Örnek 5: geri yüklenebilen bir veritabanını alma
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

Bu komut, 11/9/2012 tarihinde lpqd0zbr8y adındaki sunucudan silinen Database01 adlı geri yüklenebilen veritabanını alır.
Bu komut sonuçları $DroppedDB değişkeninde depolar.

### Örnek 6: tüm geri yüklenebilen veritabanlarını bir sunucuda alma ve sonuçlara filtre uygulama
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

Bu komut, lpqd0zbr8y adlı sunucudaki tüm geri yüklenebilen veritabanlarını alır ve sonuçları yalnızca ContactDB adlı veritabanlarına süzer.

## PARAMETRELERINE

### -ConnectionContext
Veritabanının alınacağı sunucunun bağlantı bağlamını belirtir.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Veritabanı
Bu cmdlet 'in aldığı veritabanını temsil eden nesneyi belirtir.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
Silme işleminin tarih ve saatini belirtir.
Geri yüklenebilen parametreyi belirtirseniz, silme tarih ve saatine göre geri yüklenebilen bir veritabanını almak için *Bu parametreyi belirtin* .

*Databasedeletiondate* parametresi, istenen veritabanının saatine uyması için milisaniye içermelidir.
Milisaniye olmadan bir değer belirttiğinizde veritabanı bulunamamıştır.

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

### -DatabaseName
Bu cmdlet 'in aldığı veritabanının adını belirtir.

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
Bu cmdlet 'in *veritabanı* nesneleri yerine *Restorabledroppeddatabase* nesnelerini döndürmediğini belirtir.
Belirli bir geri yüklenebilen veritabanını seçmek için *Databasedeletiondate* parametresini kullanabilirsiniz.

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

### -RestorableDroppedDatabase
Bu cmdlet 'in aldığı geri yüklenebilen veritabanını temsil eden bir nesne belirtir.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServerName
Bu cmdlet 'in aldığı veritabanını içeren sunucunun adını belirtir.
Cmdlet sunucuya erişmek için geçerli Azure aboneliğini kullanır.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

### Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. RestorableDroppedDatabase

## ÇıKıŞLAR

### 'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
Geri *yüklenebilen* parametreyi belirtmezseniz, bu cmdlet *veritabanı* nesnesi döndürür.

### 'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
Bu cmdlet, *restorabledroburparameter* 'i belirttiğinizde bir *Restorabıledroppeddatabase* nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Yeni-Azuressqldatabase](./New-AzureSqlDatabase.md)

[New-Azuressqldatabaseservercontext](./New-AzureSqlDatabaseServerContext.md)

[Remove-Azuressqldatabase](./Remove-AzureSqlDatabase.md)

[Set-Azuressqldatabase](./Set-AzureSqlDatabase.md)


