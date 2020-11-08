---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106128"
---
# Remove-AzureSchedulerJobCollection

## SYNOPSIS
Zamanlayıcı iş koleksiyonunu siler.

## INDEKI

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Remove-AzureSchedulerJobCollection** cmdlet 'i, bir zamanlayıcı iş koleksiyonunu ve bu koleksiyonun altındaki işleri siler.

## ÖRNEKLERDEN

### Örnek 1: bir konum için iş koleksiyonunu silme
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

Bu komut, Kuzey merkezi JobCollection01 adındaki zamanlayıcı iş koleksiyonunu siler.
Komut JobCollection01 altındaki işleri de siler.

### Örnek 2: bir iş konumunu silme
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

Bu komut, JobCollection02 adındaki zamanlayıcı iş koleksiyonunu siler.
Komut JobCollection02 altındaki işleri de siler.

## PARAMETRELERINE

### -Force
Bu cmdlet 'in zamanlayıcı iş koleksiyonunu onaylamanızı istemeden kaldırmadığını gösterir.

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

### -JobCollectionName
Silinecek zamanlayıcı iş koleksiyonunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Bulut hizmetini barındıran konumun adını belirtir.
Geçerli değerler: 

- Her yerde Asya
- Her yerde
- Her yerde
- Doğu Asya
- Doğu ABD
- Kuzey Orta ABD
- Kuzey Avrupa
- Güney Orta ABD
- Güneydoğu Asya
- Batı Avrupa
- Batı ABD

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

[Get-AzureSchedulerJobCollection](./Get-AzureSchedulerJobCollection.md)

[New-AzureSchedulerJobCollection](./New-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


