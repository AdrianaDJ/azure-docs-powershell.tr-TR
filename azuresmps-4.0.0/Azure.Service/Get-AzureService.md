---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106309"
---
# Get-AzureService

## SYNOPSIS
Geçerli aboneliğin bulut hizmetleri hakkında bilgi içeren bir nesne döndürür.

## INDEKI

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Get-AzureService** cmdlet 'i geçerli abonelikle Ilişkilendirilmiş tüm Azure bulut hizmetlerini içeren bir liste nesnesi döndürür.
*HizmetAdı* parametresini belirtirseniz, **Get-AzureService** yalnızca eşleşen hizmette bilgi döndürür.

## ÖRNEKLERDEN

### Örnek 1: tüm hizmetler hakkında bilgi edinme
```
PS C:\> Get-AzureService
```

Bu komut, geçerli abonelikle ilişkilendirilmiş tüm Azure hizmetleri hakkında bilgi içeren bir nesne döndürür.

### Örnek 2: belirtilen hizmet hakkında bilgi alma
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

Bu komut $MySvc hizmeti hakkında bilgi döndürür.

### Örnek 3: kullanılabilir yöntemleri ve özellikleri görüntüleme
```
PS C:\> Get-AzureService | Get-Member
```

Bu komut **Get-AzureService** cmdlet 'inde sağlanan özellikleri ve yöntemleri görüntüler.

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

### -HizmetAdı
Bilgilerin geri döndürülmesi gereken hizmetin adını belirtir.

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

### HostedServiceContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureService](./New-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


