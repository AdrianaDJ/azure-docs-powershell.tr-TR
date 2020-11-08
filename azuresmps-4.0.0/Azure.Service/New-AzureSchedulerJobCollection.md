---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105980"
---
# New-AzureSchedulerJobCollection

## SYNOPSIS
Zamanlayıcı iş koleksiyonu oluşturur.

## INDEKI

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**New-AzureSchedulerJobCollection** cmdlet 'i bir zamanlayıcı iş koleksiyonu oluşturur.
*Plan* parametresi için bir değer belirtmezseniz, cmdlet standart iş koleksiyonu oluşturur.

## ÖRNEKLERDEN

### Örnek 1: varsayılan değerleri içeren bir zamanlayıcı iş koleksiyonu oluşturma
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

Bu komut, JobCollection01 adlı standart bir zamanlayıcı iş koleksiyonu oluşturur.
Yeni koleksiyonda standart zamanlayıcı iş koleksiyonu için varsayılan iş sayısı ve maksimum yinelenme değerleri vardır.

### Örnek 2: belirtilen değerlerle bir zamanlayıcı iş koleksiyonu oluşturma
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

Bu komut, JobCollection02 adlı standart bir zamanlayıcı iş koleksiyonu oluşturur.
Yeni koleksiyonun en fazla 30 iş sayısı ve saat başına 12 en fazla yinelemesi vardır.

## PARAMETRELERINE

### Frekans
Bu Zamanlayıcı iş koleksiyonundaki herhangi bir işte belirtien yüksek frekansı belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aralık
*Sıklık* parametresini kullanarak belirtilen sıklıkta yinelenme aralığını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobCollectionName
Yeni zamanlayıcı iş koleksiyonunun adını belirtir.

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxJobCount
Zamanlayıcı iş koleksiyonunda oluşturulabilecek en fazla iş sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Plan
Zamanlayıcı işi koleksiyonu planını belirtir.

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

[Remove-AzureSchedulerJobCollection](./Remove-AzureSchedulerJobCollection.md)

[Set-AzureSchedulerJobCollection](./Set-AzureSchedulerJobCollection.md)


