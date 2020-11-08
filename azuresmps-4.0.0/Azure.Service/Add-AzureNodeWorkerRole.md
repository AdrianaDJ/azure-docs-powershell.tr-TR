---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106389"
---
# Add-AzureNodeWorkerRole

## SYNOPSIS
node.exe üzerinden bulutta barındırılmak için Node.js uygulamasının gerekli dosyalarını ve klasörlerini oluşturur

## INDEKI

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Add-AzureNodeWorkerRole** cmdlet 'i, bir Node.js uygulamasının node.exe ile bulutta barındırılması için, bazen scafkatlama olarak da adlandırılır.

## ÖRNEKLERDEN

### Örnek 1: tek örnekli işçi rolü
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

Bu örnek, geçerli uygulamaya **Myworkerrole** adlı tek bir çalışan rolü için scafkatlama ekler.

### Örnek 2: birden çok örnek çalışanı rolü
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

Bu örnek, geçerli uygulamaya **Myworkerrole** adlı tek bir çalışan rolü için, rol örneği sayısı 2 olan bir scafkatlama ekler.

## PARAMETRELERINE

### -Örnekler
Bu çalışan rolünün rol örneklerinin sayısını belirtir.
Varsayılan değer 1 ' dir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Çalışan rolünün adını belirtir.
Değer, çalışan rolünde barındırılan node.js hizmetinin scaflesi içeren klasör adını belirler.
Varsayılan WorkerRole1.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

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

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[New-AzureServiceProject](./New-AzureServiceProject.md)


