---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106110"
---
# Remove-AzureSiteRecoveryNetworkMapping

## SYNOPSIS
Site kurtarma kasasından Ağ eşlemesini kaldırır.

## INDEKI

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Remove-AzureSiteRecoveryNetworkMapping** cmdlet 'i, geçerli Azure Site Recovery kasasından bir ağ eşlemesini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: ağ ile kurtarma ağı arasındaki eşlemeyi kaldırma
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.
Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.

İkinci komut birincil ağla kurtarma ağı arasındaki eşlemeyi alır ve $NetworkMapping değişkeninde depolar.
Komut, $Servers ilk öğesi olarak ağ eşlemesinin birincil sunucusunu belirtir.
Komut, kurtarma ağının sunucusunu $Servers ikinci öğesi olarak belirtir.

Son komut $NetworkMapping Ağ eşlemesini kaldırır.

### Örnek 2: ağ ile Azure sanal makine ağı arasındaki eşlemeyi kaldırma
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

İlk komut cmdlet 'i, geçerli site kurtarma Kasası için sunucuları alır.
Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.

İkinci komut birincil ağ ile Azure sanal makine ağı arasındaki eşlemeyi alır ve $NetworkMapping değişkeninde depolar.
Komut, $Servers ilk öğesi olarak ağın birincil sunucusunu belirtir.
Komut, *Azure* parametresini belirtir.
Bu nedenle, komut bir Azure sanal makine ağının eşlemesini alır.

Son komut $NetworkMapping Ağ eşlemesini kaldırır.

## PARAMETRELERINE

### -NetworkMapping
Kaldırılacak ağ eşlemesini belirtir.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[New-AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


