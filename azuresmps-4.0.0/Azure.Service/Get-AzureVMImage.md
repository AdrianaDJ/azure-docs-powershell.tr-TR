---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E712421A-FA69-46E7-A0DE-F2734D767F2D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8355e0a1d36a6c1dc5b2ca8172cde5bf94480bbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106532"
---
# Get-AzureVMImage

## SYNOPSIS
Görüntü deposundaki bir veya birden çok işletim sistemi veya sanal makine görüntüsünün özelliklerini alır.

## INDEKI

```
Get-AzureVMImage [[-ImageName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Get-AzureVMImage** cmdlet 'i, görüntü deposundaki bir veya bir işletim sistemi veya sanal makine görüntüsünün özelliklerini alır.
Cmdlet, depodaki tüm resimler için veya resim adı sağlanmışsa belirli bir görüntüyle ilgili bilgileri döndürür.

## ÖRNEKLERDEN

### Örnek 1: geçerli görüntü deposundaki belirli bir resim nesnesini edinin.
```
PS C:\> Get-AzureVMImage -ImageName Image001
```

Bu komut, Image001 adındaki resim nesnesini geçerli görüntü deposundan alır.

### Örnek 2: geçerli görüntü deposundaki tüm resimleri alma
```
PS C:\> Get-AzureVMImage
```

Bu komut, geçerli görüntü deposundaki tüm resimleri alır.

### Örnek 3: abonelik bağlamını ayarlayın ve tüm resimleri alın
```
PS C:\> $SubsId = <MySubscriptionID>
C:\PS>$Cert = Get-AzureCertificate cert:\LocalMachine\MY\<CertificateThumbprint>
C:\PS>$MyOSImages = Get-AzureVMImage
```

Bu komut, abonelik bağlamını ayarlar ve resim deposundaki tüm resimleri alır.

## PARAMETRELERINE

### -GörüntüAdı
Görüntü deposundaki işletim sisteminin veya sanal makine görüntüsünün adını belirtir.
Bu parametreyi belirtmezseniz, tüm resimler döndürülür.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Remove-AzureVMImage](./Remove-AzureVMImage.md)

[Save-AzureVMImage](./Save-AzureVMImage.md)

[Güncelleştirme-AzureVMImage](./Update-AzureVMImage.md)


