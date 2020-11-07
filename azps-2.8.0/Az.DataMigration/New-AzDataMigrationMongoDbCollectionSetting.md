---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 041f67940fbe79a751b969dd17223f453f4929d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752250"
---
# New-AzDataMigrationMongoDbCollectionSetting

## SYNOPSIS
MongoDb geçişine göre geçiş için koleksiyon ayarı oluşturur

## INDEKI

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## Tanım
New-AzDataMigrationMongoDbCollectionSetting cmdlet 'i, işleme ve silme davranışını belirten geçiş ayarı nesnesini oluşturur.
Derleme, koleksiyonun adı ve ayarın değeri olan anahtar değer çiftine sahip olur. Çıktı, geçiş için veritabanı düzeyi ayarlarının montajı sırasında kullanılır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## PARAMETRELERINE

### -Ad
Koleksiyonun adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Shardanahtarı
Shard anahtarlarının virgülle ayrılmış listesi. MongoDb hedefi için, "_id, e-posta:-1" gibi bir sıra, "ShardKeyName: Order" ifadesini

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetRequestUnit
Adanmış koleksiyon isteği birim değeri. Ayarlanmamışsa, bu koleksiyon paylaşılan veritabanı RU kullanır.

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

### -CanDelete
Hedef verilerin silinip silinmeyeceği beklenen bir anahtar ayarlıysa, geçiş sırasında temizlenir

```yaml
Type: System.Boolean
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

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataMigration. modeller. MongoDbCollectionSetting>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
