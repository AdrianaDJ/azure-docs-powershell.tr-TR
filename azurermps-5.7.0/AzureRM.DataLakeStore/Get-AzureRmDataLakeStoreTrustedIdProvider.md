---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D79080D5-2785-4C46-86FD-FDAA11117D17
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c387ebb089ab7f9dfddaee818f26596f34ed91e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594088"
---
# Get-AzureRmDataLakeStoreTrustedIdProvider

## SYNOPSIS
Belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını alır.
Sağlayıcı belirtilmezse, hesabın tüm sağlayıcılarını listeler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmDataLakeStoreTrustedIdProvider** cmdlet 'ı belirtilen veri Lake Store 'da belirtilen güvenilen kimlik sağlayıcısını alır.
Sağlayıcı belirtilmezse, hesabın tüm sağlayıcılarını listeler.

## ÖRNEKLERDEN

### Örnek 1: belirli bir güvenilen kimlik sağlayıcısını edinme
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

"ContosoADL" hesabından "MyProvider" adlı sağlayıcıyı döndürür

### Örnek 2: bir hesaptaki tüm sağlayıcıları listeleme
```
PS C:\> Get-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL"
```

"ContosoADL" hesabının altındaki tüm sağlayıcıları listeler

## PARAMETRELERINE

### -Hesap
, Güvenilir kimlik sağlayıcısını

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

### -Ad
Alınacak güvenilen kimlik sağlayıcısının adı

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Belirtilen hesabın belirtilen güvenilen kimlik sağlayıcısını almak istediğiniz kaynak grubunun adı.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### DataLakeStoreTrustedIdProvider
Belirtilen güvenilen kimlik sağlayıcısının ayrıntıları.

### 'Te<DataLakeStoreTrustedIdProvider>
Belirtilen hesaptaki güvenilen kimlik sağlayıcılarının listesi.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

