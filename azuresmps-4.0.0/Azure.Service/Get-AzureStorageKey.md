---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 35588231-CBAC-4411-9531-9A06BD298ACA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7fdcad4b3a0f41f0589e49d4b33a767b93267855
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105548"
---
# Get-AzureStorageKey

## SYNOPSIS
Azure depolama hesabı için birincil ve ikincil depolama hesabı anahtarlarını döndürür.

## INDEKI

```
Get-AzureStorageKey [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorageKey** cmdlet 'ı, Azure depolama hesabı adı, birincil hesap anahtarı ve belirtilen Azure depolama hesabının ikincil hesap anahtarını özellikler olarak döndürür.

## ÖRNEKLERDEN

### Örnek 1: birincil ve ikincil depolama anahtarlarını içeren bir nesne alma
```
PS C:\> Get-AzureStorageKey -StorageAccountName "ContosoStore01"
```

Bu komut, ContosoStore01 depolama hesabı için birincil ve ikincil depolama anahtarlarına sahip bir nesne alır.

### Örnek 2: birincil depolama hesabı anahtarını alma ve bir değişkende depolama
```
PS C:\> $ContosoStoreKey = (Get-AzureStorageKey -StorageAccountName "ContosoStore01").Primary
```

Bu komut, $ContosoStoreKey değişkenine ContosoStore01 depolama hesabı için birincil depolama hesabı anahtarını koyar.

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
Depolama hesabı adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA
* Node.js konusunda yardım almak için `help node-dev` komutu kullanın. PHP uzantıları ile ilgili yardım için, `help php-dev` komutu kullanın.

## ILGILI BAĞLANTıLAR

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Yeni-AzureStorageAccount](./New-AzureStorageAccount.md)

[New-AzureStorageKey](./New-AzureStorageKey.md)

[Remove-AzureStorageAccount](./Remove-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


