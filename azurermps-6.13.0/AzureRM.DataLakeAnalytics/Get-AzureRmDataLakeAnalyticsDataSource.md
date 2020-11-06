---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 2f6dfae3d13a6de57a7dc04367ec2886be78f5f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593273"
---
# Get-AzureRmDataLakeAnalyticsDataSource

## SYNOPSIS
Data Lake Analytics veri kaynağını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### GetAllDataSources (varsayılan)
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetDataLakeStoreAccount
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBlobStorageAccount
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics veri kaynağını alır.

## ÖRNEKLERDEN

### Örnek 1: hesaptan veri kaynağı alma
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

Bu komut, Data Lake Analytics hesabından ContosoAdls adlı bir Data Lake Store veri kaynağını alır.

### Örnek 2: veri Lake Analytics hesabındaki veri Lake Store hesaplarının listesini alma
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

Bu komut, veri Lake Analytics hesabındaki tüm Data Lake Store hesaplarını alır.

## PARAMETRELERINE

### -Hesap
Bu cmdlet 'in veri kaynaklarını aldığı Data Lake Analytics hesabını belirtir.

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

### -Blob
Azure Blob depolama veri kaynağının adını belirtir.

```yaml
Type: System.String
Parameter Sets: GetBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataLakeStore
Data Lake Store hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: GetDataLakeStoreAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -ResourceGroupName
Veri kaynağını içeren kaynak grubu adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataLakeAnalytics. model. Psstorageaccountınfo

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeStoreAccountInfo

### Microsoft. Azure. Commands. DataLakeAnalytics. model. AdlDataSource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermdatalakeanalyzer Ticsdatasource](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[Remove-Azurermdatalakeanalyzer Ticsdatasource](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[Set-Azurermdatalakeanalyzer Ticsdatasource](./Set-AzureRmDataLakeAnalyticsDataSource.md)


