---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105973"
---
# New-AzureSqlDatabase

## SYNOPSIS
Azure SQL veritabanı oluşturur.

## INDEKI

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-Azurestabanı** cmdlet 'ı BIR Azure SQL veritabanı oluşturur.
**Yeni-Azuressqldatabaseservercontext** cmdlet 'ini kullanarak oluşturduğunuz BIR Azure SQL veritabanı sunucusu bağlantı bağlamını kullanarak sunucuyu belirtebilirsiniz.
Veya sunucu adını belirtirseniz, cmdlet, sunucuya erişim isteğinde kimlik doğrulaması yapmak için geçerli Azure aboneliği bilgilerini kullanır.

Bir Azure SQL veritabanı sunucusu belirterek yeni bir veritabanı oluşturduğunuzda, **Yeni-Azuressqldatabase** cmdlet 'i, bu işlemi gerçekleştirmek için belirtilen sunucu adını ve geçerli Azure aboneliği bilgilerini kullanarak geçici bir bağlantı bağlamı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: veritabanı oluşturma
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Bu komut, Azure SQL veritabanı sunucusu $Context bağlantı bağlamı için Database1 adlı bir Azure SQL veritabanı oluşturur.

### Örnek 2: geçerli abonelikte veritabanı oluşturma
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

Bu örnek, lpqd0zbr8y adlı belirtilen Azure SQL veritabanı sunucusunda Database1 adlı bir veritabanı oluşturur.
Cmdlet, sunucuya erişim isteğinin kimliğini doğrulamak için geçerli Azure aboneliği bilgilerini kullanır.

## PARAMETRELERINE

### -Harmanlama
Yeni veritabanı için harmanlamayı belirtir.

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

### -ConnectionContext
Bu cmdlet 'in veritabanı oluşturduğu sunucunun bağlantı bağlamını belirtir.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Yeni veritabanının adını belirtir.

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
Yeni Azure SQL veritabanı için sürümü belirtir.
Geçerli değerler: 

- Yabilirsiniz
- Web
- Karar
- Ana
- Ardından
-  Min

Varsayılan değer Web.

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

### -Force
Eylemin kullanıcıya onay istemeden yapılmasına izin verir.

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

### -MaxSizeBytes
En yüksek veritabanı boyutunu bayt olarak belirtir.
Bu parametreyi veya *Maxsizegb* parametresini belirtebilirsiniz.
Sürüm tabanlı kabul edilebilir değerler için *Maxsizegb* parametre açıklamasına bakın.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
En yüksek veritabanı boyutunu gigabayt olarak belirtir.
Bu parametreyi veya *Maxsizebytes* parametresini belirtebilirsiniz.
Kabul edilebilir değerler sürüme göre farklılık gösterir.

Temel sürüm değerleri: 1 veya 2

Standart sürüm değerleri: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 veya 250

Premium sürüm değerleri: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400 veya 500

Web Edition değerleri: 1 veya 5

İş sürümü değerleri: 10, 20, 30, 40, 50, 100 veya 150

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
Yeni veritabanını içerecek Azure SQL veritabanı sunucusunun adını belirtir.

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

### -Serviceamacın
Bu veritabanının yeni hizmet amacını (performans düzeyi) temsil eden bir nesne belirtir.
Bu değer, bu veritabanına atanan kaynakların düzeyini temsil eder.
Geçerli değerler: 

Temel: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c standart (S0): f1173c43-91bd-4AAA-973c-54e79e15235b standart (S1): 1b1ebd4d/cr903-4baa-97f9-4ea675f5e928 standart (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 * standart (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40 Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d Premium (P1): 720348,-c4fb-4304-9e9f-17c71c904f5d Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 Premium (P3): a7c4c615-cfb1-464B-b252-925be0a19446

* Standart (S3) en son SQL veritabanı güncelleştirme V12 (Önizleme) parçasıdır.
Daha fazla bilgi için, Azure SQL Veritabanı V12 Preview 'daki yeniliklere göz atın https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

## NOTLARıNDA
* **Yeni-azures, veritabanı** tarafından oluşturulan veritabanını silmek için Remove-AzureSqlDatabase cmdlet 'ini kullanın.

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Veritabanı oluşturma](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqldatabase](./Get-AzureSqlDatabase.md)

[New-Azuressqldatabaseservercontext](./New-AzureSqlDatabaseServerContext.md)

[Remove-Azuressqldatabase](./Remove-AzureSqlDatabase.md)

[Set-Azuressqldatabase](./Set-AzureSqlDatabase.md)


