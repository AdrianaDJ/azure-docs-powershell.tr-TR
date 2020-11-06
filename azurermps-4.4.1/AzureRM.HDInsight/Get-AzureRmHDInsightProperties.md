---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: e1701d60289343bb61a2891617fd10c6b9987b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594697"
---
# Get-AzureRmHDInsightProperties

## SYNOPSIS
HDInsight hizmeti hakkında, kullanılabilir konumlar ve kapasite gibi özellikleri alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmHDInsightProperties** cmdlet 'i, kullanılabilir konumlar, HDInsight küme sürümleri ve kullanılabilir işlem kapasitesi gibi Azure HDInsight 'a özgü özellikleri alır.

## ÖRNEKLERDEN

### Örnek 1: Azure HDInsight kümesinin özelliklerini alma
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

Bu komut, bir HDInsight hizmetinden Doğu US 2 konumundan Özellikler alır.

## PARAMETRELERINE

### -Konum
HDInsight özelliklerinin getirileceği konumu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Management. HDInsight. model. CapabilitiesResponse

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

