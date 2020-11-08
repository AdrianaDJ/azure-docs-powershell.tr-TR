---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106218"
---
# New-AzureServiceProject

## SYNOPSIS
Yeni bir hizmet için gerekli dosyaları ve yapılandırmayı oluşturur.

## INDEKI

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**New-AzureServiceProject** cmdlet 'i geçerli dizindeki yeni bir Azure hizmeti için gerekli dosyaları ve yapılandırmayı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: hizmet için scafkatlama oluşturma
```
PS C:\> New-AzureServiceProject MyService1
```

Bu örnek, geçerli dizindeki MyService1 adlı yeni bir Azure hizmeti için scafkatlama oluşturur.

## PARAMETRELERINE

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
Hizmetin adını belirtir.
Hizmetinizin ana bilgisayar adının ilk bölümünü (örneğin, name.cloudapp.net) ve hizmetinizi içerecek dizini belirler.
Ad yalnızca harf, rakam ve tire karakterini (-) içerebilir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureNodeWebRole](./Add-AzureNodeWebRole.md)

[Add-AzureNodeWorkerRole](./Add-AzureNodeWorkerRole.md)

[Yayımla-AzureServiceProject](./Publish-AzureServiceProject.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)

[Set-AzureServiceProjectRole](./Set-AzureServiceProjectRole.md)


