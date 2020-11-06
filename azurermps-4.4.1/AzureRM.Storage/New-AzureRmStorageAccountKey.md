---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 76b7ea9eb4a248071025ef359d6bf0877b35fe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594982"
---
# New-AzureRmStorageAccountKey

## SYNOPSIS
Azure depolama hesabı için depolama anahtarını yeniden oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmStorageAccountKey** cmdlet 'ı Azure depolama hesabı için depolama anahtarını yeniden oluşturur.

## ÖRNEKLERDEN

### Örnek 1: depolama anahtarını yeniden oluşturma
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

Bu komut belirtilen depolama hesabının depolama anahtarını yeniden oluşturur.

## PARAMETRELERINE

### -AnahtarAdı
Hangi tuşun yeniden yeniden kullanılacağını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- anahtar 
- anahtar2

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Depolama anahtarının yeniden oluşturulacak depolama hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Depolama hesabını içeren kaynak grubunun adını belirtir.

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

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-azurermstorageın](./Get-AzureRmStorageAccountKey.md)


