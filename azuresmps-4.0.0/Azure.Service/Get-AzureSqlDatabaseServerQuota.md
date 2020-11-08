---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105570"
---
# Get-AzureSqlDatabaseServerQuota

## SYNOPSIS
Bir Azure SQL veritabanı sunucusu için kota bilgilerini alır.

## INDEKI

### ByConnectionContext
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-Azuressqldatabaseserverquota** cmdlet 'i, belirli BIR Azure SQL veritabanı sunucusu örneğinin kota bilgilerini alır.
Bir bağlantı bağlamı veya sunucu adı belirtin.
Kota adı belirtmezseniz, bu cmdlet sunucunun tüm kota bilgilerini alır.

## ÖRNEKLERDEN

### Örnek 1: belirli bir kotanın bilgilerini alma
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

Bu komut Premium_Databases adlı kotayı, $Context değişkeninde depolanan bağlantının belirttiği Azure SQL veritabanı sunucusundan alır.

### Örnek 2: tüm kotalar için bilgi alma
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

Bu komut, bağlantı $Context belirtilen sunucudan tüm kota değerlerini alır.

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

### -Tırnak işareti
Bu cmdlet 'in aldığı kota değerinin adını belirtir.

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

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. Sunucuquota []

## NOTLARıNDA
* Kimlik doğrulama: Bu cmdlet SQL Server kimlik doğrulaması veya sertifika tabanlı kimlik doğrulaması kullanabilir. Kimlik doğrulamasını ayarlama örnekleri için New-AzureSqlDatabaseServerContext cmdlet 'ine bakın.

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-Azuressqldatabaseservercontext](./New-AzureSqlDatabaseServerContext.md)


