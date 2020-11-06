---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: CE7B54BC-C493-49CE-93BD-346ED0B966A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/wait-azurermdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Wait-AzureRmDataLakeAnalyticsJob.md
ms.openlocfilehash: 43af4abf52c3441f25ec57ce659b6c4e47a79cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594093"
---
# Wait-AzureRmDataLakeAnalyticsJob

## SYNOPSIS
İşin tamamlanmasını bekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Wait-AzureRmDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-WaitIntervalInSeconds] <Int32>]
 [[-TimeoutInSeconds] <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Wait-Azurermdatalakeanalizleri** , bir Azure Data Lake Analytics işinin tamamlamasını bekler.

## ÖRNEKLERDEN

### Örnek 1: işin tamamlanmasını bekle
```
PS C:\>Wait-AzureRmDataLakeAnalyticsJob -Account "ContosoAdlAccount" -JobId "a0a78d72-3fa8-4564-9b18-6becb3fda48a"
```

Aşağıdaki komut belirtilen KIMLIğIN tamamlanma işini bekler.

## PARAMETRELERINE

### -Hesap
Data Lake Analytics hesap adını belirtir.

```yaml
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Bekleme işinin KIMLIĞINI belirtir.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Timeoutınseconds
Bekleme işleminden çıkmadan önce beklenecek saniye sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Waitıntervalınseconds
İş durumu denetimi arasında geçen saniye sayısını belirtin.

```yaml
Type: Int32
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

### 'Sine
' JobId ' parametresi ardışık düzenin ' Guid ' türünün değerini kabul eder

## ÇıKıŞLAR

### Jobınformation
Tamamlanan işin son iş ayrıntıları.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermdatalakeanalyzer](./Get-AzureRmDataLakeAnalyticsJob.md)

[Stop-Azurermdatalakeanalyzer](./Stop-AzureRmDataLakeAnalyticsJob.md)

[Submit-Azurermdatalakeanalyzer Ticsjob](./Submit-AzureRmDataLakeAnalyticsJob.md)


