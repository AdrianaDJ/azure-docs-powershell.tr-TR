---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: A6899341-1E5E-4F8B-8D5D-5923B1223628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsCatalogItem.md
ms.openlocfilehash: b12b09c686a2e0a5fcd85854551608b16cb43d3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594294"
---
# Get-AzureRmDataLakeAnalyticsCatalogItem

## SYNOPSIS
Veri Lake Analytics Katalog öğesi veya öğe türleri alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmDataLakeAnalyticsCatalogItem [-Account] <String> [-ItemType] <CatalogItemType>
 [[-Path] <CatalogPathInstance>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermdatalakeanalizleri** , belirtilen Azure Data Lake Analytics Katalog öğesini alır veya belirtilen türde katalog öğelerini alır.

## ÖRNEKLERDEN

### Örnek 1: belirli bir veritabanı alma
```
PS C:\>Get-AzureRmDataLakeAnalyticsCatalogItem -Account "contosoadla" -ItemType Database -Path "databaseName"
```

Bu komut belirtilen veritabanını alır.

### Örnek 2: belirtilen veritabanı ve şemada tablolar alma
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "contosoadla" -ItemType Table -Path "databaseName.schemaName"
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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### CatalogItem
Belirtilen katalog öğesi.

### Listeniz<CatalogItem>
İlgili kapsayıcının altındaki belirtilen Katalog öğelerinin listesi.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Test-Azurermdatalakeanalyzer Tic, Alogıtem](./Test-AzureRmDataLakeAnalyticsCatalogItem.md)


