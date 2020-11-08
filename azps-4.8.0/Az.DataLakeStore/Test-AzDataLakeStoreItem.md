---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: 1629e987386998e642df1390ec391444500a6c44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267776"
---
# Test-AzDataLakeStoreItem

## SYNOPSIS
Data Lake Store 'da bir dosya veya klasörün varlığını sınar.

## INDEKI

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Test-AzDataLakeStoreItem** cmdlet 'ı Data Lake Store 'da bir dosya veya klasörün varlığını sınar.

## ÖRNEKLERDEN

### Örnek 1: dosyayı test etme
```powershell
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

Bu komut, Test.csv dosyasının ContosoADL hesabında bulunup bulunmadığını sınar.

### Örnek 2

Data Lake Store 'da bir dosya veya klasörün varlığını sınar. oluşturulmuş

<!-- Aladdin Generated Example -->
```powershell
Test-AzDataLakeStoreItem -Account 'ContosoADL' -Path '/MyFiles/Test.csv' -PathType Any
```

## PARAMETRELERINE

### -Hesap
Data Lake Store hesabının adını belirtir.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yol
Kök dizinle (/) başlayarak sınanacak olan öğenin veri Lake Store yolunu belirtir.

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

### -PathType
Sınanacak öğenin türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Tüm 
- Dosyasý 
- Klasörler

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

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

### Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStorePathInstance

### Microsoft. Azure. Commands. DataLakeStore. modeller. DataLakeStoreEnums + PathType

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Dışarı aktarma-AzDataLakeStoreItem](./Export-AzDataLakeStoreItem.md)

[Get-AzDataLakeStoreItem](./Get-AzDataLakeStoreItem.md)

[İçeri aktarma-AzDataLakeStoreItem](./Import-AzDataLakeStoreItem.md)

[Katıl-AzDataLakeStoreItem](./Join-AzDataLakeStoreItem.md)

[Taşı-AzDataLakeStoreItem](./Move-AzDataLakeStoreItem.md)

[Remove-AzDataLakeStoreItem](./Remove-AzDataLakeStoreItem.md)


