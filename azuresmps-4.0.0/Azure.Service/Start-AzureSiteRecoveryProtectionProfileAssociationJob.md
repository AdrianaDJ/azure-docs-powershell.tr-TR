---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: CB5E1419-C4C7-4524-ACCC-13C9D9CCA621
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4955bfa121d6742903dd2ca99721186c7c860004
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105848"
---
# Start-AzureSiteRecoveryProtectionProfileAssociationJob

## SYNOPSIS
Site kurtarma çoğaltması ilkesi ilişki işini başlatır.

## INDEKI

### EnterpriseToAzure (varsayılan)
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnterpriseToEnterprise
```
Start-AzureSiteRecoveryProtectionProfileAssociationJob -ProtectionProfile <ASRProtectionProfile>
 -PrimaryProtectionContainer <ASRProtectionContainer> -RecoveryProtectionContainer <ASRProtectionContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Start-AzureSiteRecoveryProtectionProfileAssociationJob** cmdlet 'i bir çoğaltma Ilkesini Azure Site Recovery koruma konteyneriyle ilişkilendirmek için bir ilişkilendirme işi başlatır.

## ÖRNEKLERDEN

### Örnek 1: koruma profilini Ilişkilendirme
```
PS C:\> $ProtectionContainer01 = Get-AzureSiteRecoveryProtectionContainer -Id "5ba2ea95-856d-4033-9ca3-91e3e2c080b9"
PS C:\> $ProtectionProfile = New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
PS C:\> $ProtectionContainer02 = Get-AzureSiteRecoveryProtectionContainer -Id "cf011f2a-aa19-443c-9f60-357f6b8afb77"
PS C:\> Start-AzureSiteRecoveryProtectionProfileAssociationJob -PrimaryProtectionContainer $ProtectionContainer01 -ProtectionProfile $ProtectionProfile -RecoveryProtectionContainer $ProtectionContainer02
Name             : MyProtectionProfile
ID               : 51978b0f-9241-4153-9171-2e19344f0805
ClientRequestId  : bb6f3200-b7c6-4c6f-bcbc-a70bb9946f03-2015-01-27 22:55:55Z-P
State            : InProgress
StateDescription : InProgress
StartTime        : 1/27/2015 10:56:01 PM
EndTime          : 
AllowedActions   : 
Tasks            : {Adding the protection group, Configuring Windows Server 2012 R2 Hyper-V hosts for Azure}
Errors           : {}
```

İlk komut **Get-AzureSiteRecoveryProtectionContainer** cmdlet 'ini kullanarak bir koruma kapsayıcısı alır ve bu kapsayıcıyı $ProtectionContainer 01 değişkeninde depolar.

İkinci komut, **New-AzureSiteRecoveryProtectionProfileObject** cmdlet 'ini kullanarak bir koruma profili oluşturur ve bu koruma profilini $ProtectionProfile değişkeninde depolar.

Üçüncü komut bir koruma kapsayıcısı alır ve $ProtectionContainer 02 değişkeninde depolar.

Son komutu $ProtectionProfile 'da depolanan koruma profilini, $ProtectionContainer 01 ' de depolanan kapsayıcıya birincil koruma kapsayıcısı olarak ilişkilendirir.
Komut $ProtectionContainer 02 ' de depolanan kapsayıcıyı kurtarma koruma kapsayıcısı olarak ilişkilendirir.

## PARAMETRELERINE

### -PrimaryProtectionContainer
Koruma profili ayarlarının uygulanacağı birincil koruma kapsayıcısını belirtir.

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
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

### -ProtectionProfile
Koruma kapsayıcılarına uygulanacak koruma profili ayarlarını belirtir.
Bir **Asrprotectionprofile** nesnesi edinmek için New-AzureSiteRecoveryProtectionProfileObject cmdlet 'ini kullanın.

```yaml
Type: ASRProtectionProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryProtectionContainer
Koruma profili ayarlarının uygulanacağı kurtarma koruması kapsayıcısını belirtir.

```yaml
Type: ASRProtectionContainer
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
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

[Get-AzureSiteRecoveryProtectionContainer](./Get-AzureSiteRecoveryProtectionContainer.md)

[New-AzureSiteRecoveryProtectionProfileObject](./New-AzureSiteRecoveryProtectionProfileObject.md)

[Start-AzureSiteRecoveryProtectionProfileDissociationJob](./Start-AzureSiteRecoveryProtectionProfileDissociationJob.md)


