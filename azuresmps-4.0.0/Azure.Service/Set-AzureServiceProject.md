---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D0A2B454-7BFF-4D4D-8A85-FDB47249758F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f4d1598f17629d178e1feff1b5549631be48c60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105819"
---
# Set-AzureServiceProject

## SYNOPSIS
Geçerli hizmet için varsayılan konumu, aboneliği, yuvayı ve depolama hesabını ayarlar.

## INDEKI

```
Set-AzureServiceProject [-Location <String>] [-Slot <String>] [-Storage <String>] [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureServiceProject** cmdlet 'i geçerli hizmet için dağıtım konumunu, yuvayı, depolama hesabını ve aboneliği ayarlar.
Bu değerler, hizmet bulutta yayımlandığında kullanılır.

## ÖRNEKLERDEN

### Örnek 1: temel ayarlar
```
PS C:\> Set-AzureServiceProject -Location "North Central US" -Slot Production -Storage myStorageAccount -Subscription myAzureSubscription
```

Hizmetin dağıtım konumunu Kuzey Merkezi ABD bölgesine ayarlar.
Dağıtım yuvasını üretime ayarlar. Hizmet tanımını myStorageAccount olarak hazırlamak için kullanılacak depolama hesabını ayarlar.
Hizmeti mySubscription 'a barındıracak aboneliği ayarlar.
Hizmet buluta yayımlandığında, bu, Kuzey Merkezi ABD bölgesindeki bir veri merkezinde barındırılır, dağıtım yuvasını güncelleştirecek ve belirtilen aboneliği ve depolama hesabını kullanacaktır.

## PARAMETRELERINE

### -Konum
Hizmetin barındırıldığı bölge.
Hizmet buluta yayımlandığında bu değer kullanılır.
Olası değerler: tüm Asya, Avrupa, ABD, Doğu Asya, Doğu ABD, Kuzey Merkezi ABD, Kuzey Avrupa, Güney Merkez ABD, Güneydoğu Asya, Batı Avrupa, Batı ABD.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Bu cmdlet 'in, üzerinde işlem yaptığı öğeyi temsil eden bir nesne döndürdüğü anlamına gelir.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

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

### Yuvalı
Hizmetin barındırıldığı yuva (üretim veya hazırlama).
Hizmet buluta yayımlandığında bu değer kullanılır.
Olası değerler: üretim, aşamalandırma.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Depolama
Hizmet paketi buluta yüklenirken kullanılacak depolama hesabı.
Depolama hesabı yoksa, hizmet buluta yayımlandığında oluşturulur.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA
* düğüm-dev, php-dev, Python-dev

## ILGILI BAĞLANTıLAR

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Yayımla-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


