---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E3D405D-69FB-42C2-8A5B-BDBD27B63088
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503c2e0a076be3f31b6435a30dc658af9b45835a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106167"
---
# Remove-AzureCertificate

## SYNOPSIS
Azure hizmetinden sertifika kaldırır.

## INDEKI

```
Remove-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm] <String> [-Thumbprint] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Tanım
**Remove-Azurecercertificate** 'in cmdlet 'ı bir Azure hizmetinden sertifikayı kaldırır.

## ÖRNEKLERDEN

### Örnek 1: hizmetten sertifikayı kaldırma
```
PS C:\> Remove-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

Bu komut, belirtilen parmak izine sahip sertifika nesnesini bulut hizmetinden kaldırır.

### Örnek 2: hizmetten tüm sertifikaları kaldırma
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" | Remove-AzureCertificate
```

Bu komut, **Get-Azurecercertificate** adlı hizmetten contososervice adındaki tüm sertifikaları alır.
Komut, ardışık düzen işlecini kullanarak her sertifikayı geçerli cmdlet 'e geçirir.
Bu cmdlet bulut hizmetinden her sertifikayı kaldırır.

### Örnek 3: belirli bir parmak izi algoritmasını kullanan bir hizmetten tüm sertifikaları kaldırma
```
PS C:\> Get-AzureCertificate -ServiceName "ContosoService" -ThumbprintAlgorithm "sha1" | Remove-AzureCertificate
```

Bu komut, SHA1 parmak izi algoritmasını kullanan ContosoService adındaki tüm sertifikaları alır.
Komut her sertifikayı geçerli cmdlet 'e geçirir ve her sertifikayı çıkarır.

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
Bu cmdlet 'in sertifikayı kaldırdığı Azure hizmetinin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parmak izi
Bu cmdlet 'in kaldırdığı sertifikanın parmak izini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ThumbprintAlgorithm
Sertifika parmak izini oluşturmak için kullanılan algoritmayı belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

## ILGILI BAĞLANTıLAR

[Add-Azurecercertificate](./Add-AzureCertificate.md)

[Get-Azurecercertificate](./Get-AzureCertificate.md)

[New-Azurecercertificate Atesetting](./New-AzureCertificateSetting.md)


