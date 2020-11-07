---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: d05b6507ea8e1d5244e23ab7b8b6222848a1d088
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752245"
---
# New-AzDataMigrationMongoDbDatabaseSetting

## SYNOPSIS
MongoDb geçişi için geçiş için veritabanı ayarı oluşturur

## INDEKI

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## Tanım
New-AzDataMigrationMongoDbDatabaseSetting cmdlet 'i, işleme ve silme davranışını belirten geçiş ayarı nesnesini oluşturur.
Çıkış, koleksiyonun adına ve geçiş görevini çağırmaya kullanılabilen ayarın değerine sahip bir anahtar değeri çiftidir.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## PARAMETRELERINE

### -Ad
Veritabanının adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -TargetRequestUnit
Adanmış veritabanı düzeyi istek birim değeri. Ayarlanmamışsa, bu koleksiyon paylaşılan veritabanı RU kullanır.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Koleksiyonlar
New-AzureRmDmsMongoDbDatabaseSetting çağrısı tarafından döndürülen MongoDb koleksiyon ayarı nesneleri dizisi.

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataMigration. modeller. MongoDbDatabaseSetting

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
