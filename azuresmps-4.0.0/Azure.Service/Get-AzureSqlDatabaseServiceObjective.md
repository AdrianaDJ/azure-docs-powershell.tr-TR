---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105568"
---
# Get-AzureSqlDatabaseServiceObjective

## SYNOPSIS
Bir Azure SQL veritabanı sunucusu için hizmet amaçlarını alır.

## INDEKI

### ByConnectionContext (varsayılan)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-azures, Databaseserviceamacın** cmdlet 'ı BIR Azure SQL veritabanı sunucusu için hizmet amaçlarını alır.
Hizmet hedeflerine performans düzeyleri denir.
Hizmet hedefi belirtmezseniz, bu cmdlet belirtilen sunucunun geçerli tüm hizmet amaçlarını döndürür.

Bu cmdlet, temel, standart ve Premium hizmet katmanlarına uygulanır.

## ÖRNEKLERDEN

### Örnek 1: bağlantı bağlamı kullanarak tüm hizmet amaçlarını alma
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

Bu komut, bağlantı $Context bağlamının belirttiği sunucunun tüm hizmet amaçlarını alır.

### Örnek 2: sunucu adı kullanarak tüm hizmet amaçlarını alma
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

Bu komut, server01 adındaki sunucunun tüm hizmet amaçlarını alır.

## PARAMETRELERINE

### -Context
Sunucunun bağlantı bağlamını belirtir.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

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

### -Serviceamacın
Bu cmdlet 'in aldığı hizmet hedefini temsil eden bir nesne belirtir.
Geçerli değerler: 

- Temel: dd6d99bb-f193-4EC1-86f2-43d3bccbc49c
- Standart (S0): f1173c43-91bd-4AAA-973c-54e79e15235b
- Standart (S1): 1b1ebd4d-vseç903-4baa-97f9-4ea675f5e928
- Standart (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standart (S3): 789681b8-CA10-4EB0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- Premium (P3): a7c4c615-cfb1-464B-b252-925be0a19446

* Standart (S3) en son SQL veritabanı güncelleştirme V12 (Önizleme) parçasıdır.
Daha fazla bilgi için, Azure kitaplığındaki [Azure SQL Veritabanı V12 Preview](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) () Ile sunulan yenilikleri görün `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceObjectiveName
Alınacak hizmet amacın adını belirtir.
Geçerli değerler: Basic, S0, S1, S2, S3, P1, P2 ve P3.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Windowsazde. Commands. SqlDatabase. Services. Server. Serviceamacın

## ÇıKıŞLAR

### 'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://msdn.microsoft.com/library/ee336279.aspx)

[Hizmet düzeyi amacını alma](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-Azuressqldatabaseservercontext](./New-AzureSqlDatabaseServerContext.md)


