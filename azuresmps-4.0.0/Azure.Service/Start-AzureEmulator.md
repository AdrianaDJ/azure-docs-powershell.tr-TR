---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A1815E7F-720E-4526-A779-106C181B840D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22b04496d9ce310b58662c62b70a195e8cfa8878
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106031"
---
# Start-AzureEmulator

## SYNOPSIS
Hesaplama ve depolama öykünücüsünü başlatır.

## INDEKI

```
Start-AzureEmulator [-Launch] [-Mode <ComputeEmulatorMode>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Start-AzureEmulator** cmdlet 'i hem COMPUTE hem de depolama öykünücüsünü başlatır ve işlem öykünücüsünde geçerli hizmeti barındırır.

## ÖRNEKLERDEN

### Örnek 1: öykünücüyü başlatma ve Tarayıcıyı başlatma
```
PS C:\> Start-AzureEmulator -L
```

Bu örnek, hizmeti Azure öykünücüsü 'nde çalıştırır ve öykünülmüş hizmette yeni bir tarayıcı penceresi başlatır.

## PARAMETRELERINE

### -Başlat
Hizmette barındırdıktan sonra hizmette yeni bir tarayıcı penceresi açar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mod
Öykünücü modunu belirtir.
Geçerli değerler: Full ve Express.
Varsayılan değer,

```yaml
Type: ComputeEmulatorMode
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureServiceProject](./New-AzureServiceProject.md)

[Yayımla-AzureServiceProject](./Publish-AzureServiceProject.md)

[Stop-AzureEmulator](./Stop-AzureEmulator.md)


