---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F371FD62-D138-4610-84A1-93EDC42D6AAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/get-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 724441a09ec2714048ec43b781f5792903bce73a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587396"
---
# Get-AzureRmStreamAnalyticsInput

## SYNOPSIS
Stream Analytics iş girdilerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmStreamAnalyticsInput** cmdlet 'ı bir Stream Analytics işinde tanımlanan tüm girdileri listeler veya belirli bir giriş hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: işte tanımlı girişler hakkında bilgi alma
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob"
```

Bu komut, iş StreamingJob 'da tanımlanan tüm girişlerle ilgili bilgileri döndürür.

### Örnek 2: işte tanımlı belirli bir girdi hakkında bilgi alma
```
PS C:\>Get-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EntryStream"
```

Bu komut, iş StreamingJob 'da tanımlanan EntryStream adlı girdi hakkındaki bilgileri döndürür.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -JobName
Azure Stream Analytics girişinin ait olduğu Azure Stream Analytics işinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Alınacak Azure Stream Analytics girişinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Azure Akış Analizi girişinin ait olduğu kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. StreamAnalytics. modeller. Psınınput, Microsoft. Azure. Commands. StreamAnalytics]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureRmStreamAnalyticsInput](./New-AzureRmStreamAnalyticsInput.md)

[Remove-AzureRmStreamAnalyticsInput](./Remove-AzureRmStreamAnalyticsInput.md)

[Test-AzureRmStreamAnalyticsInput](./Test-AzureRmStreamAnalyticsInput.md)


