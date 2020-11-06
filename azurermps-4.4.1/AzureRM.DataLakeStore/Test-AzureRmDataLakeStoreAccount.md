---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 613DE097-65E0-4F08-839D-F9B53F772382
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 8aeb682b270de821a6944c619d7933148b2855e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594735"
---
# Test-AzureRmDataLakeStoreAccount

## SYNOPSIS
Veri Lake Store hesabının varlığını sınar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Test-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Test-AzureRmDataLakeStoreAccount** cmdlet 'ı Data Lake Store hesabının varlığını sınar.

## ÖRNEKLERDEN

### Örnek 1: hesabı test etme
```
PS C:\>Test-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

Bu komut, ContosoADL adlı hesabın var olup olmadığını sınar.

## PARAMETRELERINE

### -Ad
Sınanacak veri Lake Store hesabının adını belirtir.

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

### -ResourceGroupName
Sınanacak hesabı içeren kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

### bool
Belirtilen hesabın varlığını belirten doğru veya yanlış.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmDataLakeStoreAccount](./Get-AzureRmDataLakeStoreAccount.md)

[New-AzureRmDataLakeStoreAccount](./New-AzureRmDataLakeStoreAccount.md)

[Remove-AzureRmDataLakeStoreAccount](./Remove-AzureRmDataLakeStoreAccount.md)

[Set-AzureRmDataLakeStoreAccount](./Set-AzureRmDataLakeStoreAccount.md)


