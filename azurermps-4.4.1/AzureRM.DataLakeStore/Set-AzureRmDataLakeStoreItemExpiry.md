---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemExpiry.md
ms.openlocfilehash: f71c26e69f9f297a23d4e6902ca6aaac6b135c42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595178"
---
# Set-AzureRmDataLakeStoreItemExpiry

## SYNOPSIS
Azure Data Lake Store hesabındaki bir dosyanın süresi bitim süresini ayarlar veya kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmDataLakeStoreItemExpiry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [[-Expiration] <DateTimeOffset>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
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

### -Süre sonu
Belirtilen dosyanın mutlak son kullanma tarihi.
Değer yoksa veya MaxValue olarak ayarlanmamışsa, dosyanın süresi dolmayacaktır.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
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

### DataLakeStoreItem
Yeni son kullanma tarihi olan güncelleştirilmiş dosya.

## NOTLARıNDA
Diğer ad: Set-AdlStoreItemExpiry

## ILGILI BAĞLANTıLAR

[Get-AzureRmDataLakeStoreItem](./Get-AzureRmDataLakeStoreItem.md)

