---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593033"
---
# Update-AzureRmRecoveryServicesAsrPolicy

## SYNOPSIS
Azure Site Recovery çoğaltma ilkesini güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Update-AzureRmRecoveryServicesAsrPolicy** cmdlet 'ı belirtilen Azure Site Recovery çoğaltma ilkesini güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

Belirtilen parametreleri kullanarak çoğaltmayı Güncelleştir ilkesini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

## PARAMETRELERINE

### -Applicationpotentın
Uygulamayla tutarlı kurtarma noktalarının oluşturulacağı sıklığı (saat) belirtir.

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

### -Kimlik doğrulama
Kullanılan kimlik doğrulama türünü belirtir.
Geçerli değerler:

- Sertifika
-  Kerberos

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Sıkıştırma
Sıkıştırmanın etkinleştirilip etkinleştirilmeyeceğini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Şifreleme
Şifrelemenin etkinleştirilip etkinleştirilmeyeceğini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Cmdlet için giriş nesnesi: güncelleştirilecek çoğaltma ilkesine karşılık gelen ASR çoğaltma ilkesi nesnesini belirtir.

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Numberofrecoverypointstokoru
Korunacak sayı kurtarma noktalarını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recoveryazurestorageaccountıd
Çoğaltma hedefinin Azure depolama hesabı KIMLIĞINI belirtir. New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet kullanılarak çoğaltmayı etkinleştirirken alternatif sağlanmadıysa, çoğaltma için hedef depolama hesabı olarak kullanılır.

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

### -Replicasilme
VMM yönetilen sitesinden diğerine çoğaltma devre dışı bırakılırken çoğaltma sanal makinesinin silinip silinmeyeceğini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationFrequencyInSeconds
Çoğaltma sıklığı aralığını saniye cinsinden belirtir.
Geçerli değerler:

- 30
- 300
- 900

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationMethod
Çoğaltma yöntemini belirtir.
Geçerli değerler:

- Medya
- Çalış

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationPort
Çoğaltma için kullanılan bağlantı noktasını belirtir.

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationStartTime
Çoğaltmanın başlangıç zamanını belirtir.
İşin başında 24 saatten sonra olmaması gerekir.

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy

## ÇıKıŞLAR

### System. Object

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

