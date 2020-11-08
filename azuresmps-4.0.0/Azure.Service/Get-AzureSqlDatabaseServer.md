---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105571"
---
# Get-AzureSqlDatabaseServer

## SYNOPSIS
Azure SQL veritabanı sunucuları hakkında bilgi alır.

## INDEKI

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-Azuressqldatabaseserver** cmdlet 'i, geçerli ABONELIKTEKI Azure SQL veritabanı sunucusu örnekleri hakkında bilgi alır.
Bir sunucuyu adıyla belirtirseniz, bu cmdlet bu sunucu hakkında bilgi içeren bir nesne döndürür.
Aksi halde cmdlet, tüm sunucular hakkında bilgi döndürür.

## ÖRNEKLERDEN

### Örnek 1: tüm sunucular hakkında bilgi edinme
```
PS C:\> Get-AzureSqlDatabaseServer
```

Bu komut, geçerli abonelikteki tüm Azure SQL veritabanı sunucusu örnekleri hakkında bilgi döndürür.

### Örnek 2: belirli bir sunucu hakkında bilgi alma
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

Bu komut, lpqd0zbr8y adlı sunucu hakkındaki bilgileri döndürür.

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

### -ServerName
Bu cmdlet 'in kaldırdığı sunucunun adını belirtir.
Tam DNS adını değil, sunucu adını belirtin.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext

## ÇıKıŞLAR

### 'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Liste sunucuları](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-Azuressqldatabaseserver](./New-AzureSqlDatabaseServer.md)

[Remove-Azuressqldatabaseserver](./Remove-AzureSqlDatabaseServer.md)

[Set-Azuressqldatabaseserver](./Set-AzureSqlDatabaseServer.md)


