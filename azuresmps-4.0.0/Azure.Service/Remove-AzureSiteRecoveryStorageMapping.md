---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106109"
---
# Remove-AzureSiteRecoveryStorageMapping

## SYNOPSIS
Site kurtarma Kasası için depolama nesnesi eşlemesini kaldırır.

## INDEKI

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Remove-AzureSiteRecoveryStorageMapping** cmdlet 'i, geçerli Azure Site Recovery Kasası Için bir depolama nesnesi eşlemesini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: ağ ile kurtarma ağı arasındaki eşlemeyi kaldırma
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.
Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.

İkinci komut iki depolama nesnesi arasındaki eşlemeyi alır ve $StorageMapping değişkeninde depolar.
Komut, $Servers ilk öğesi olarak ağ eşlemesinin birincil sunucusunu belirtir.
Komut, kurtarma ağının sunucusunu $Servers ikinci öğesi olarak belirtir.

Son komut $StorageMapping olan eşlemeyi kaldırır.

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

### -StorageMapping
Ağ eşlemesini belirtir.
Bir **Asrstoragemapping** edinmek için **Get-AzureSiteRecoveryStorage** cmdlet 'ini kullanın.

```yaml
Type: ASRStorageMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)


