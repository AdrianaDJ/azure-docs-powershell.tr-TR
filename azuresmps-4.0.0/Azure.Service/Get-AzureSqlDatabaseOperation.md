---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106293"
---
# Get-AzureSqlDatabaseOperation

## SYNOPSIS
Bir Azure sunucusundaki veritabanı işlemlerinin durumunu alır.

## INDEKI

### ByConnectionContext (varsayılan)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-Azuressqldatabaseoperation** cmdlet 'ı belirtilen Azure sunucusundaki veritabanı işlemlerinin durumunu alır.
Yalnızca *ServerName* veya *ConnectionContext* parametresini belirtirseniz cmdlet, sunucunun tüm veritabanı işlemlerini alır.
*Veritabanı* veya *DatabaseName* parametresini kullanarak bir veritabanı belirtirseniz, bu cmdlet belirtilen veritabanı için tüm işlemleri alır.
Bir işlem GUID 'si ve *ServerName* veya *ConnectionContext* belirtirseniz cmdlet tek bir veritabanı işlemini alır.

## ÖRNEKLERDEN

### Örnek 1: veritabanı için tüm veritabanı işlemlerinin durumunu alma
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

Bu komut, Database17 adlı sunucudaki, bağlantı bağlamının $Context belirttiği tüm veritabanı işlemlerinin durumunu alır.

### Örnek 2: sunucunun tüm veritabanı işlemlerinin durumunu alma
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

Bu komut, sunucudaki bağlantı $Context bağlamının belirttiği tüm veritabanı işlemlerinin durumunu alır.

## PARAMETRELERINE

### -ConnectionContext
Sunucunun bağlantı bağlamını belirtir.

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
Azure SQL veritabanını temsil eden bir nesne belirtir.
Bu parametreyi belirtirseniz, *ServerName* parametresini veya *ConnectionContext* parametresini belirtmeniz gerekir.

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

### -DatabaseName
Veritabanının adını belirtir.
Bu parametreyi belirtirseniz, *ServerName* parametresini veya *ConnectionContext* parametresini belirtmeniz gerekir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationGuid
Bu cmdlet 'in durumu aldığı belirli bir veritabanı işlemini temsil eden işlem KIMLIĞINI belirtir.
Azure SQL veritabanı veya sunucusu için tüm veritabanı işlemlerini isteyerek işlem kimlikleri elde edebilirsiniz.
Bu parametreyi belirtirseniz, *ServerName* parametresini veya *ConnectionContext* parametresini belirtmeniz gerekir.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Sunucunun adını belirtir.

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

### Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext

### System. Guid

## ÇıKıŞLAR

### Microsoft. Windowsazve. Commands. SqlDatabase. Services. Server. veritabanı. DatabaseOperationResponseList []
Bu cmdlet birden fazla işlem alırsanız **Databaseoperationresponselist** nesnelerinin dizisini döndürür.

### Microsoft. Windowsazve. Commands. SqlDatabase. Services. Server. veritabanı. DatabaseOperationResponse

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://msdn.microsoft.com/library/ee336279.aspx)

[Veritabanı Işlemi durumu](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqldatabase](./Get-AzureSqlDatabase.md)

[New-Azuressqldatabaseservercontext](./New-AzureSqlDatabaseServerContext.md)


