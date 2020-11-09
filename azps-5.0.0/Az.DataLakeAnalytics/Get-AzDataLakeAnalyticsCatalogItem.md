---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: fb0e73d338c54b93626ee3a5ee78bbbe4adca884
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320749"
---
# Get-AzDataLakeAnalyticsCatalogItem

## SYNOPSIS
Veri Lake Analytics Katalog öğesi veya öğe türleri alır.

## INDEKI

```
Get-AzDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azdatalakeanaliz Ticdağlı Alogıtem** , belirtilen Azure Data Lake Analytics Katalog öğesini alır veya belirtilen türde katalog öğelerini alır.

## ÖRNEKLERDEN

### Örnek 1: belirli bir veritabanı alma
```
PS C:\>Get-AzDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

Bu komut belirtilen veritabanını alır.

### Örnek 2: belirtilen veritabanı ve şemada tablolar alma
```
PS C:\>Get-AzDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
```

Bu komut, belirtilen veritabanındaki tabloların listesini alır.

## PARAMETRELERINE

### -Hesap
Data Lake Analytics hesap adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ItemType
Getirilen veya listelenen öğelerin Katalog öğesi türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Veritabanı
- Şemayla
- Derlemeyle
- Tablo
- Tablodeğerdenişlevi
- Tabloistatistikleri
- ExternalDataSource
- Görünümünde
- Anlatılan
- Gizlili
- Sertifika
- Tipte
- Tablobölümü

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+CatalogItemType
Parameter Sets: (All)
Aliases:
Accepted values: Database, Schema, Assembly, Table, TablePartition, TableValuedFunction, TableStatistics, ExternalDataSource, View, Procedure, Secret, Credential, Types, Package

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
Alınacak öğenin birden çok parçalı yolunu veya listedeki öğelerin üst öğesini belirtir.
Yolun bölümleri noktayla ayrılmalıdır (.).

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. DataLakeAnalytics. modeller. Datalakeanalizleri Ticsenums + Catalogıtemtype

### Microsoft. Azure. Commands. DataLakeAnalytics. model. Catalogpathınstance

## ÇıKıŞLAR

### Microsoft. Azure. Management. DataLake. Analytics. modeller. CatalogItem

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Test-Azdatalakeanaliz Ticdağlı Alogıtem](./Test-AzDataLakeAnalyticsCatalogItem.md)


