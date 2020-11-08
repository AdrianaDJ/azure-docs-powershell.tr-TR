---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106294"
---
# Get-AzureSqlDatabaseImportExportStatus

## SYNOPSIS
İçeri veya dışarı aktarma isteğinin durumunu alır.

## INDEKI

### Byconnectionınfo
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRequestObject
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-Azureskurdatabaseımportexportstatus** cmdlet 'i içeri aktarma veya dışarı aktarma isteğinin durumunu alır.
Start-AzureSqlDatabaseImport veya Start-AzureSqlDatabaseExport cmdlet 'i istekleri başlatır.
Request nesnesini *Request* parametresini kullanarak belirtebilirsiniz veya *İstekKimliği RequestId* parametresini ve *Kullanıcı adı* , *parola* ve *ServerName* parametrelerini kullanarak tanımlayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: dışarı aktarma isteğinin durumunu alma
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

İlk komut bir dışarı aktarma isteği oluşturur ve $ExportRequest değişkeninde depolar.

İkinci komut $ExportRequest uygulamasında depolanan dışarı aktarma isteğinin durumunu alır.

## PARAMETRELERINE

### -Parola
Azure SQL veritabanı sunucusuna bağlanmak için gereken parolayı belirtir.
*RequestId* parametresini belirttiyseniz bu parametreyi belirtmeniz gerekir.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

### -İstek
**Importexportrequest** nesnesini belirtir.
İçeri veya dışarı aktarma isteği nesnesi almak için Start-AzureSqlDatabaseImport veya Start-AzureSqlDatabaseExport cmdlet 'ini kullanın.

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequestId
Bu cmdlet 'in durumu aldığı içeri veya dışarı aktarma işleminin GUID 'sini belirtir.
Bu parametreyi belirtirseniz *Kullanıcı adı* , *parola* ve *ServerName* parametrelerini belirtmeniz gerekir.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Azure SQL veritabanı sunucusunun adını belirtir.
*RequestId* parametresini belirttiyseniz bu parametreyi belirtmeniz gerekir.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kullanıcı adı
Azure SQL veritabanı sunucusuna bağlanmak için gereken kullanıcı adını belirtir.
*RequestId* parametresini belirttiyseniz bu parametreyi belirtmeniz gerekir.

```yaml
Type: String
Parameter Sets: ByConnectionInfo
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

### Microsoft. Windowsazde. Commands. SqlDatabase. Services. ımportexport. StatusInfo

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Içeri aktarma veritabanı durumunu alma](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-Azuressqldatabaseexport](./Start-AzureSqlDatabaseExport.md)

[Start-Azuressqldatabaseimport](./Start-AzureSqlDatabaseImport.md)


