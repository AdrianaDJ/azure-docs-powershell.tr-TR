---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105992"
---
# New-AzureRoleTemplate

## SYNOPSIS
Web ve çalışan rolü şablonları oluşturur.

## INDEKI

### WebRole
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### WorkerRole
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Yeni-AzureRoleTemplate** cmdlet 'i Web ve işçi rol şablonları oluşturur.

## ÖRNEKLERDEN

### Örnek 1: Web rolü şablonu oluşturma
```
PS C:\> New-AzureRoleTemplate -Web
```

Bu örnek, geçerli dizindeki WebRoleTemplate adlı klasörde yeni bir Web rolü şablonu oluşturur.

### Örnek 2: çalışan rolü şablonu oluşturma
```
PS C:\> New-AzureRoleTemplate -Worker
```

Bu örnek, geçerli dizindeki WebRoleTemplate adlı klasörde yeni bir çalışan rolü şablonu oluşturur.

### Örnek 3: özel bir dizinde rol şablonu oluşturma
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

Bu örnek, geçerli dizin yerine MyWebRoleTemplate adlı dizinde yeni bir Web rolü şablonu oluşturur.

## PARAMETRELERINE

### -Çıktı
Oluşturulan şablonun çıkış yolunu belirtir.

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

### -Web
Web rolü şablonu oluşturmak istediğinizi belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Çalışan
Bir çalışan rolü oluşturmak istediğinizi belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
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

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Add-AzureWorkerRole](./Add-AzureWorkerRole.md)


