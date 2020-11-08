---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105711"
---
# Add-AzureWebRole

## SYNOPSIS
Web çalışanı rolü ekler.

## INDEKI

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Add-AzureWebRole** cmdlet 'i Web çalışanı rolü ekler.

## ÖRNEKLERDEN

### Örnek 1: varsayılan rol ekleme
```
PS C:\> Add-AzureWebRole
```

Bu komut, ad olarak Webrole1 varsayılan yapılandırmasına sahip web rolü ekler ve tek bir örnek.

### Örnek 2: adı olan bir rol ekleme
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

Bu komut, geçerli uygulamaya MyWebRole adında tek bir Web rolü ekler.

### Örnek 3: ad ve örnek sayısına sahip bir rol ekleme
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

Bu komut, geçerli uygulamaya MyWebRole adlı bir Web rolü ekler.
Cmdlet 'in rol örneği sayısı 2 ' dir.

### Örnek 4: ad ve şablon içeren bir rol ekleme
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

Bu komut, geçerli uygulamaya MyWebRole adında tek bir Web rolü ekler.
Komut, scafkatlama şablonu olarak MyWebTemplateFolder adlı bir klasör belirtir.

## PARAMETRELERINE

### -Örnekler
Örneklerin sayısını belirtir.

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
Web rolünün adını belirtir.

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

### -TemplateFolder
Şablon klasörünü belirtir.

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

## ILGILI BAĞLANTıLAR

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)

[Yeni-AzureRoleTemplate](./New-AzureRoleTemplate.md)


