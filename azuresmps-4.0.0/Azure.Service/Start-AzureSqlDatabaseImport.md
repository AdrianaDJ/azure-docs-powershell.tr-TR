---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105427"
---
# Start-AzureSqlDatabaseImport

## SYNOPSIS
BLOB depolama alanından bir Azure SQL veritabanına içeri aktarma işlemi başlatır.

## INDEKI

### ByContainerObject
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByContainerName
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Start-Azuresddatabaseımport** cmdlet 'ı Azure Blob depolamasındaki BIR Azure SQL veritabanına içeri aktarma işlemini başlatır.
Veritabanı yoksa, bu cmdlet bunu belirttiğiniz boyut ve sürüm değerlerini kullanarak oluşturur.
İşlem bir veritabanı sunucusu bağlantı bağlamı gerektiriyor.
İçeri aktarma işleminin durumunu almak için Get-AzureSqlDatabaseImportExportStatus cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: veritabanını Içeri aktarma
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

Bu örnek, $BlobName değişkeninde blob depolamasındaki bir içeri aktarma işlemini DatabaseName adlı Azure SQL veritabanına oluşturur.

## PARAMETRELERINE

### -BlobName
Bu cmdlet 'in veritabanını içeri aktardıkları Azure Blob deposunun adını belirtir.

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

### -DatabaseMaxSize
Veritabanı için en büyük boyutu gigabayt cinsinden belirtir.
Veritabanı yoksa, bu cmdlet bu en büyük boyutu temel alarak oluşturur.
Kabul edilebilir değerler sürüme göre farklılık gösterir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Veritabanı için bir ad belirtir.
Veritabanı yoksa, bu cmdlet bunu oluşturur ve bu parametrenin belirttiği adı atar.

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

### -Edition
Veritabanının sürümünü belirtir.
Veritabanı yoksa, bu cmdlet bu sürüm olarak oluşturur.
Geçerli değerler: 

- Yabilirsiniz
- Web 
- Karar 
- Ana
- Ardından
- Min

Varsayılan Web.

```yaml
Type: DatabaseEdition
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

### -SqlConnectionContext
Veritabanının bulunduğu sunucunun bağlantı bağlamını belirtir.

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainer
Bu cmdlet 'in bir veritabanını aldığı blob 'U içeren depolama kapsayıcısını belirtir.

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContainerName
BLOB depolama kapsayıcısının adını belirtir.

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContext
BLOB depolama kapsayıcısı 'nın bağlamını belirtir.

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. SqlDatabase. Services. ımportexportrequest

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Veritabanını içeri aktarma](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqldatabaseımportexportstatus](./Get-AzureSqlDatabaseImportExportStatus.md)

[Start-Azuressqldatabaseexport](./Start-AzureSqlDatabaseExport.md)


