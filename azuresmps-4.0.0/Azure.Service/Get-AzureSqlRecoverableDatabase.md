---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106559"
---
# Get-AzureSqlRecoverableDatabase

## SYNOPSIS
Belirtilen sunucudan kurtarılabilir veritabanlarını alır.

## INDEKI

### AllDatabasesOnGivenServer (varsayılan)
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Givendatabaseon sunucu
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Givendatabasenesnesi
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-Azuressqlrecoverabledatabase** cmdlet 'i belirtilen sunucudan kurtarılabilir veritabanlarını alır.
Bu cmdlet, belirli bir kurtarılabilir veritabanını veya sunucudaki tüm kurtarılabilir veritabanlarını alır.

## ÖRNEKLERDEN

### Örnek 1: tüm kurtarılabilir veritabanları
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

Bu komut, server01 adlı sunucudaki tüm kurtarılabilir veritabanlarını alır.

### Örnek 2: kurtarılabilir bir veritabanı alma
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

Bu komut, server01 adındaki sunucuda Database17 adlı veritabanını alır.

## PARAMETRELERINE

### -Veritabanı
Bu cmdlet 'in aldığı kurtarılabilir veritabanını temsil eden bir nesne belirtir.

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Bu cmdlet 'in aldığı kurtarılabilir veritabanının adını belirtir.

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
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
Bu cmdlet 'in kurtarılabilir veritabanları aldığı sunucunun adını belirtir.

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
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

### Microsoft. Windowsazme. Management. Sql. modeller. RecoverableDatabase

## ÇıKıŞLAR

### 'A\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\>

## NOTLARıNDA
* Bu cmdlet 'i çalıştırmak için sertifika tabanlı kimlik doğrulaması kullanmalısınız. Bu cmdlet 'i çalıştıran bilgisayarda aşağıdaki komutları çalıştırın: 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Kurtarılabilir veritabanı](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Start-AzureSqlDatabaseRecovery](./Start-AzureSqlDatabaseRecovery.md)


