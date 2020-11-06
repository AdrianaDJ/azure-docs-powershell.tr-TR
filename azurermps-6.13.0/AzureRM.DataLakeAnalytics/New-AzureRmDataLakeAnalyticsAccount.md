---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 2fec19864e9d13e4b0e4ede1d351a08427e95357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593266"
---
# New-AzureRmDataLakeAnalyticsAccount

## SYNOPSIS
Veri Lake Analytics hesabı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Yeni-Azurermdatalakeanalizizsaccount** cmdlet 'ı bir Azure Data Lake Analytics hesabı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: veri Lake Analytics hesabı oluşturma
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

Bu komut, ContosoOrg adlı kaynak grubunda ContosoAdlStore veri deposunu kullanan ContosoAdlAccount adlı bir Data Lake Analytics hesabı oluşturur.

## PARAMETRELERINE

### -DefaultDataLakeStore
Varsayılan veri kaynağı olarak ayarlanacak Data Lake Store hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
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

### -Konum
Veri Lake Analytics hesabının oluşturulacağı konumu belirtir.
Şu anda yalnızca Doğu ABD 2 destekleniyor.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Maxçözümlerken
Bu hesap için isteğe bağlı en yüksek çözümleme birimleri.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MaxJobCount
Aynı anda hesabın altında çalışan isteğe bağlı en yüksek işler. Hiçbiri belirtilmezse, varsayılan 3 olur

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Data Lake Analytics hesap adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -QueryStoreRetention
İş meta verilerinin tutulacağı isteğe bağlı gün sayısı. Belirtilmezse, varsayılan 30 gündür.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Data Lake Analytics hesabının kaynak grubu adını belirtir.
Kaynak grubu oluşturmak için New-AzureRmResourceGroup cmdlet 'ini kullanın.

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

### Etiketli
Bu hesapla ilişkilendirilmiş etiketlerin dize sözlüğü

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Katmanlı
Bu hesabın kullanması için istenen taahhüt katmanı.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. topluluklar. Hashtable

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### System. Nullable ' 1 [[Microsoft. Azure. Management. DataLake. Analytics. modeller. TierType, Microsoft. Azure. Management. DataLake. Analytics, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## ÇıKıŞLAR

### Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtalakeanaliz Ticsaccount

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermdatalakeanalyzer](./Get-AzureRmDataLakeAnalyticsAccount.md)

[Remove-Azurermdatalakeanalyzer Ticsaccount](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[Set-Azurermdatalakeanalyzer Ticsaccount](./Set-AzureRmDataLakeAnalyticsAccount.md)

[Test-Azurermdatalakeanalyzer](./Test-AzureRmDataLakeAnalyticsAccount.md)


