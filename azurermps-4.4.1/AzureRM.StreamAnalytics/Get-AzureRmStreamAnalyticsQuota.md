---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: ECD0950F-2490-49E2-85E6-5FA2A59364E6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Get-AzureRmStreamAnalyticsQuota.md
ms.openlocfilehash: b6edc46131bac545d649e6ea3fe41b142d596850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587735"
---
# Get-AzureRmStreamAnalyticsQuota

## SYNOPSIS
Bir bölgenin akış birimi kotası hakkında bilgi alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmStreamAnalyticsQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmStreamAnalyticsQuota** cmdlet 'i bir bölgenin akış birimi kotası hakkında bilgi alır.

## ÖRNEKLERDEN

### Örnek 1: bir bölgenin akış birimi kotası hakkında bilgi alma
```
PS C:\>Get-AzureRmStreamAnalyticsQuota -Location "West US"
```

Bu komut, Batı bölgesinde akış birimi kotası ve kullanımı hakkındaki bilgileri döndürür.

## PARAMETRELERINE

### -Konum
Akış birimi kota bilgilerinin alınacağı bir Azure bölgesinin veya veri merkezi konumunun adını belirtir.
https://azure.microsoft.com/en-us/regions/#serviceshttps://azure.microsoft.com/en-us/regions/#servicesDesteklenen Azure bölgelerinin listesini görün.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. StreamAnalytics.. PSQuota, Microsoft. Azure. Commands. StreamAnalytics]] Microsoft. Azure. Commands. StreamAnalytics. modeller. PSQuota

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure Stream Analytics cmdlet 'Leri](./AzureRM.StreamAnalytics.md)


