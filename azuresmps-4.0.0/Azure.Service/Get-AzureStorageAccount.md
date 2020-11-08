---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105549"
---
# Get-AzureStorageAccount

## SYNOPSIS
Geçerli Azure aboneliğinin depolama hesaplarını alır.

## INDEKI

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorageAccount** cmdlet 'i, geçerli aboneliğin depolama hesapları hakkında bilgi içeren bir nesne döndürür.
*StorageAccountName* parametresi belirtilmişse, yalnızca belirtilen depolama hesabı hakkında bilgi verilir.

## ÖRNEKLERDEN

### Örnek 1: tüm depolama hesaplarını döndürme
```
PS C:\> Get-AzureStorageAccount
```

Bu komut, geçerli abonelikle ilişkilendirilmiş tüm depolama hesaplarını içeren bir nesne döndürür.

### Örnek 2: belirli bir hesabın hesap bilgilerini döndürme
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

Bu komut, yalnızca ContosoStore01 hesap bilgilerini içeren bir nesne döndürür.

### Örnek 3: depolama hesapları tablosunu görüntüleme
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

Bu komut geçerli abonelikle ilişkilendirilmiş tüm depolama hesaplarını içeren bir nesne döndürür ve bunları hesap adını, hesap etiketini ve depolama konumunu gösteren bir tablo olarak verir.

## PARAMETRELERINE

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Depolama hesabının adını belirtir.
Belirtilmişse, bu cmdlet yalnızca belirtilen depolama hesabı nesnesini döndürür.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### ManagementOperationContext

## NOTLARıNDA
* `help node-dev`Geliştirmeyle ilgili yardım almak için Node.js geliştirme ile ilgili yardım alın. `help php-dev`Php geliştirmeyle ilgili yardım almak için yazın.

## ILGILI BAĞLANTıLAR

[Yeni-AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


