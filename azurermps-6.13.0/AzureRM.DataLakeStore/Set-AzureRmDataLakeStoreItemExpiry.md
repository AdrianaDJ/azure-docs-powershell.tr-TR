---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemexpiry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: 4aff82a2621a462f0af14fe2dce620f297011874
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589578"
---
# Set-AzureRmDataLakeStoreItemExpiry

## SYNOPSIS
Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SetAbsoluteNeverExpireExpiry (varsayılan)
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Setrelativesüre sonu
```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-RelativeFileExpiryOption] <PathRelativeExpiryOptions> [[-RelativeTime] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmDataLakeStoreItemExpiry** cmdlet 'ı, Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.

## ÖRNEKLERDEN

### Örnek 1: dosya için son kullanma zamanını ayarlama
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt -Expiration [DateTimeOffset]::Now.AddHours(2)
```

Şu andan itibaren, ContosoADL hesabındaki myfile.txt zaman aşımı süresini iki saat olacak şekilde ayarlar.
Bu, dosyanın süresi dolmasına neden olur (silme için işaretlenir) iki saat içinde.

### Örnek 2: dosyanın süre sonunu kaldırma
```
PS C:\> Set-AzureRmDataLakeStoreItemExpiry -AccountName "ContosoADL" -Path /myfile.txt
```

' ContosoADL ' hesabında ' myfile.txt ' dosyasında daha önce ayarlanmış olan sona erdirmeyi kaldırır.
Bu, dosyanın otomatik olarak süresinin dolamayacağı anlamına gelir (silme için işaretlenir) ve el ile silinmesi veya yeniden kullanım süresi olarak ayarlanması gerekir.

### Örnek 3: Şu an için bir dosya için son kullanma tarihi ayarlama
```
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToNow -RelativeTime 240000
PS C:\> Set-AdlStoreItemExpiry -Account "ContosoADL" -path /myfile.txt -RelativeFileExpiryOption RelativeToCreationDate -RelativeTime 240000
```

İlk komut, sunucudaki geçerli saate göre dosya/myfile.txt 240 saniyesi kullanım süresi sonunu ayarlar.
İkinci komut, sunucudaki oluşturulma zamanı saatine göre dosya/myfile.txt 240 saniyesi kullanım süresi sonunu ayarlar.

## PARAMETRELERINE

### -Hesap
Data Lake Store hesap adını belirtir.

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

### -Süre sonu
Belirtilen dosyanın mutlak son kullanma tarihi.
Değer yoksa veya MaxValue olarak ayarlanmamışsa, dosyanın süresi dolmayacaktır.

```yaml
Type: System.DateTimeOffset
Parameter Sets: SetAbsoluteNeverExpireExpiry
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
Bitiş tarihi ayarlanacak veya kaldırılacak dosya öğesinin veri Lake Store yolunu belirtir.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeFileExpiryOption
Göreli süre sonu seçenekleri. RelativeToNow veya RelativeToCreationDate geçerli seçeneklerdir

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathRelativeExpiryOptions
Parameter Sets: SetRelativeExpiry
Aliases:
Accepted values: RelativeToNow, RelativeToCreationDate

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RelativeTime
Şimdi veya oluşturulma saatine göre milisaniye cinsinden göreli zaman

```yaml
Type: System.Int64
Parameter Sets: SetRelativeExpiry
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance

### System. DateTimeOffset

### Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + PathRelativeExpiryOptions

### System. Int64

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreItem

## NOTLARıNDA
Diğer ad: Set-AdlStoreItemExpiry

## ILGILI BAĞLANTıLAR

[Get-AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

