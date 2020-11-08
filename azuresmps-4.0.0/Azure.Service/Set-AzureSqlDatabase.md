---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105865"
---
# Set-AzureSqlDatabase

## SYNOPSIS
Azure SQL veritabanı için özellikleri ayarlar.

## INDEKI

### ByNameWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-Azurestabanı** cmdlet 'ı BIR Azure SQL veritabanının özelliklerini ayarlar.
Veritabanını adla belirtebilirsiniz veya ardışık düzen aracılığıyla Azure SQL veritabanı nesnesini geçirebilirsiniz.
Sunucuyu ada göre belirtebilir veya Azure SQL veritabanı sunucusu bağlantı bağlamını geçirebilirsiniz.
**New-azures, Databaseservercontext** cmdlet 'ini çalıştırarak bir bağlantı bağlamı oluşturun.
Sunucuyu adıyla belirtirseniz cmdlet, isteğin kimliğini doğrulamak için geçerli Azure aboneliği bilgilerini kullanır.

## ÖRNEKLERDEN

### Örnek 1: bağlantı bağlamı kullanarak veritabanının boyutunu değiştirme
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

Bu örnekte, Database01 adlı veritabanının boyutu, Azure SQL veritabanı sunucusu bağlantı bağlamında, $Context.

### Örnek 2: sunucu adı kullanarak veritabanının boyutunu değiştirme
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

Bu örnekte, lpqd0zbr8y adlı sunucuda Database01 adlı veritabanının boyutu 20 GB ile değişir.

## PARAMETRELERINE

### -ConnectionContext
Sunucunun bağlantı bağlamını belirtir.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Veritabanı
Bu cmdlet 'in değiştirdiği Azure SQL veritabanını temsil eden bir nesne belirtir.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Bu cmdlet 'in değiştirdiği veritabanının adını belirtir.

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
Azure SQL veritabanı için yeni sürümü belirtir.
Geçerli değerler: 

- Yabilirsiniz
- Web
- Karar
- Ana
- Ardından
-  Min

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
Eylemin onay istemeden yapılmasına izin verir.

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
Sürüm tabanlı kabul edilebilir değerler için *Maxsizegb* parametresine bakın.

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
Veritabanı için yeni en yüksek boyutu gigabayt cinsinden belirtir.
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

### -NewDatabaseName
Veritabanının yeni adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Güncelleştirilmiş Azure SQL veritabanını döndürür.

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
Bu cmdlet 'in değiştirdiği veritabanını içeren sunucunun adını belirtir.

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Serviceamacın
Bu veritabanının yeni hizmet amacını (performans düzeyi) temsil eden bir nesne belirtir.
Geçerli değerler: 

- Temel: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c
- Standart (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Standart (S1): 1b1ebd4d-vseç903-4baa-97f9-4ea675f5e928
- Standart (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standart (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464B-b252-925be0a19446

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

### -Eşitleme
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

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

## ÇıKıŞLAR

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Veritabanını güncelleştir](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[Get-Azuressqldatabase](./Get-AzureSqlDatabase.md)

[Yeni-Azuressqldatabase](./New-AzureSqlDatabase.md)

[Remove-Azuressqldatabase](./Remove-AzureSqlDatabase.md)

[New-Azuressqldatabaseservercontext](./New-AzureSqlDatabaseServerContext.md)


