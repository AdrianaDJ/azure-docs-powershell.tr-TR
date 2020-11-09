---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 9992c4232bd93e9653f0723911f539b1204ce538
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323026"
---
# New-AzRecoveryServicesAsrRecoveryPlan

## SYNOPSIS
ASR kurtarma planı oluşturur.

## INDEKI

### EnterpriseToEnterprise (varsayılan)
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -RecoveryFabric <ASRFabric>
 -ReplicationProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### EnterpriseToAzure
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> [-Azure]
 -FailoverDeploymentModel <String> -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureZoneToZone
```
New-AzRecoveryServicesAsrRecoveryPlan -Name <String> -PrimaryFabric <ASRFabric> -PrimaryZone <String>
 -RecoveryZone <String> [-AzureZoneToZone] -ReplicationProtectedItem <ASRReplicationProtectedItem[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Byrpfıle
```
New-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzRecoveryServicesAsrRecoveryPlan** cmdlet 'ı, kurtarma hizmetleri Kasası 'Nda bir Azure Site Recovery, kurtarma planı oluşturur.

Kurtarma planı, bir uygulamaya ait sanal makineleri bir birime ekleyerek bir birimde kurtarılmasına olanak tanır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -RecoveryFabric $RecoveryFabric -ReplicationProtectedItem $RPI
```

Belirtilen parametrelerle kurtarma planı oluşturma işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

### Örnek 2
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrRecoveryPlan -Name $RPName -PrimaryFabric $PrimaryFabric -PrimaryZone $pZone-RecoveryZone $rZone -ReplicationProtectedItem $RPI
```

Azure bölgesi için kurtarma planı oluşturma işlemini bölge çoğaltılmış öğelerine başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

## PARAMETRELERINE

### -Azure
Switch parametresi Azure 'dan Azure olağanüstü durum kurtarması, kurtarma planı oluşturma senaryosunu belirtir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureZoneToZone
Switch parametresi, Azure bölgesinde çoğaltılmış öğeyi bölge senaryosuna oluşturmayı belirtir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailoverDeploymentModel
Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin yük devretme dağıtım modelini (Classic veya Kaynak Yöneticisi) belirtir.

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases:
Accepted values: Classic, ResourceManager

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Kurtarma planının adı.

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yol
Kurtarma planı tanımı JSON dosyasının yolunu belirtir. Kurtarma planı oluşturmak için bir kurtarma planı tanımı JSON kullanılabilir.

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryFabric
Bu kurtarma planının parçası olacak çoğaltma korumalı öğelerinin birincil ASR yapısı için ASR doku nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryZone
Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin birincil kullanılabilirlik bölgesini belirtir.

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryFabric
Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin kurtarma ASR yapısı için ASR doku nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryZone
Bu kurtarma planının parçası olacak şekilde, çoğaltma korumalı öğelerin birincil kullanılabilirlik bölgesini belirtir.

```yaml
Type: System.String
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Replicationkorunabilir
Kurtarma planının ilk grubuna eklenecek çoğaltma korumalı öğelerin listesi.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AzureZoneToZone
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir. Asrreplicationkorunabilir. Asrreplicationkorunabilir

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzRecoveryServicesAsrRecoveryPlan](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[Remove-AzRecoveryServicesAsrRecoveryPlan](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[Güncelleştirme-AzRecoveryServicesAsrRecoveryPlan](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


