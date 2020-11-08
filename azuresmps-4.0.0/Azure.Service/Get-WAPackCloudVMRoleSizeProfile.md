---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106508"
---
# Get-WAPackCloudVMRoleSizeProfile

## SYNOPSIS
Bulut VM rolü boyut profili nesnelerini alır.

## INDEKI

### Boş (varsayılan)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-Wapackmrdvmrolesizeprofile** cmdlet 'i sanal MAKINELERIN bulut VM rolü boyut profili nesnelerini alır.

## ÖRNEKLERDEN

### Örnek 1: ad kullanarak bulut VM rolü boyut profili alma
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

Bu komut, küçük olan boyut profilini alır.

### Örnek 2: tüm bulut VM rolü
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

Bu komut, tüm boyut profillerini alır.

## PARAMETRELERINE

### -Ad
Bulut VM rol boyutu profilinin adını belirtir.

```yaml
Type: String
Parameter Sets: FromName
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

[Get-WAPackVM](./Get-WAPackVM.md)


