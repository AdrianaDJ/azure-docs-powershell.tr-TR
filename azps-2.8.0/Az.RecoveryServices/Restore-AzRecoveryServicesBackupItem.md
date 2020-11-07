---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F49FA524-28BC-464F-BD0A-F898E99C83D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/restore-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restore-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 87051d6e8c5dabe5a5e5c5138e06eda0de961219
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932964"
---
# Restore-AzRecoveryServicesBackupItem

## SYNOPSIS

Yedekleme öğesinin verilerini ve yapılandırmasını kurtarma noktasına geri yükler.

## INDEKI

### AzureVMParameterSet (varsayılan)

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 [-StorageAccountName] <String> [-StorageAccountResourceGroupName] <String>
 [[-TargetResourceGroupName] <String>] [-UseOriginalStorageAccount] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureFileParameterSet

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-RecoveryPoint] <RecoveryPointBase>
 -ResolveConflict <RestoreFSResolveConflictOption> [-SourceFilePath <String>]
 [-SourceFileType <SourceFileType>] [-TargetStorageAccountName <String>] [-TargetFileShareName <String>]
 [-TargetFolder <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### AzureWorkloadParameterSet

```
Restore-AzRecoveryServicesBackupItem [-VaultLocation <String>] [-WLRecoveryConfig] <RecoveryConfigBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım

**Restore-Azrecoveryservicesbackupıtem** cmdlet 'i, bir Azure yedekleme öğesinin verilerini ve yapılandırmasını belirtilen kurtarma noktasına geri yükler.
Bu cmdlet geri yüklemeyi, kurtarma hizmetleri kasasından müşterinin depolama hesabına başlatır.
Geri yükleme işlemi tam sanal makineyi geri yüklemez.
Disk verilerini ve yapılandırma bilgilerini geri yükler.
Geri yükleme işlemi bittikten sonra, sanal makineyi oluşturmalı ve başlatmalısınız.
-VaultId parametresini kullanarak kasa bağlamını ayarlayın.

Not:-VaultId parametresine ek olarak bu cmdlet 'i başarıyla yürütmek Için-VaultLocation parametresi de kullanılmalıdır.

## ÖRNEKLERDEN

### Örnek 1: öğeyi kurtarma noktasına geri yükleme

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -ContainerType AzureVM -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $StartDate = (Get-Date).AddDays(-7)
PS C:\> $EndDate = Get-Date
PS C:\> $RP = Get-AzRecoveryServicesBackupRecoveryPoint -Item $BackupItem -StartDate $StartDate.ToUniversalTime() -EndDate $EndDate.ToUniversalTime() -VaultId $vault.ID
PS C:\> $RestoreJob = Restore-AzRecoveryServicesBackupItem -RecoveryPoint $RP[0] -StorageAccountName "DestAccount" -StorageAccountResourceGroupName "DestRG" -VaultId $vault.ID -VaultLocation $vault.Location
    WorkloadName    Operation       Status          StartTime              EndTime
    ------------    ---------       ------          ---------              -------
    V2VM            Restore         InProgress      26-Apr-16 1:14:01 PM   01-Jan-01 12:00:00 AM
```

İlk komut AzureVM türünün yedek kapsayıcısını alır ve $Container değişkeninde depolar.
İkinci komut, V2VM adındaki yedekleme öğesini $Container alır ve $BackupItem değişkeninde depolar.
Üçüncü komut yedi günden önceki tarihi alır ve $StartDate değişkeninde depolar.
Dördüncü komut geçerli tarihi alır ve $EndDate değişkeninde depolar.
Beşinci komut, $StartDate ve $EndDate tarafından filtrelenmiş belirli bir yedekleme öğesinin kurtarma noktaları listesini alır.
Belirtilen tarih aralığı son 7 gündür.
Son komut, diskleri DestRG kaynak grubundaki hedef depolama hesabına geri yükler.

## PARAMETRELERINE

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

### -RecoveryPoint

Sanal makinenin geri yükleneceği kurtarma noktasını belirtir.
**Azurermrecoveryservicesbackuprecoverypoint** nesnesi almak için **Get-azrecoveryservicesbackuprecoverypoint** cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: AzureVMParameterSet, AzureFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResolveConflict

Geri yüklenen öğenin hedefte da bulunması durumunda, üzerine yazılıp yazılmayacağını belirtmek için bunu kullanın.
Bu parametre için kabul edilebilir değerler şunlardır:

- İne
- Git

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RestoreFSResolveConflictOption
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: Overwrite, Skip

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilePath

Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır. Dosya paylaşımı içinde geri yüklenecek öğenin yolu.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sourcedosyatürü

Dosya paylaşımından belirli bir öğe geri yükleme için kullanılır. Dosya paylaşımı içinde geri yüklenecek öğenin türü.
Bu parametre için kabul edilebilir değerler şunlardır:

- Dosyasý
- Directory

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SourceFileType]
Parameter Sets: AzureFileParameterSet
Aliases:
Accepted values: File, Directory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName

Aboneliğinizdeki hedef depolama hesabının adını belirtir.
Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountResourceGroupName

Aboneliğinizdeki hedef depolama hesabını içeren kaynak grubunun adını belirtir.
Geri yükleme işleminin bir parçası olarak bu cmdlet, bu depolama hesabındaki diskleri ve yapılandırma bilgilerini depolar.

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Targetfilepaylaşımadı

Dosya paylaşımının geri yüklenmesi gereken dosya paylaşımı.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetFolder

Dosya paylaşımının altındaki Targetfilepaylaşımadı içinde geri yüklenmesi gereken klasör. Yedeklenen içeriğin kök klasöre geri yüklenebilmesi için, hedef klasör değerlerini boş dize olarak verin.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName

Yönetilen disklerin geri yüklendiği kaynak grubu. Yönetilen disklerle VM yedeklemesi için geçerlidir

```yaml
Type: System.String
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStorageAccountName

Dosya paylaşımının geri yüklenmesi gereken depolama hesabı.

```yaml
Type: System.String
Parameter Sets: AzureFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseOriginalStorageAccount

Kurtarma noktasındaki disklerin orijinal depolama hesaplarına geri yüklenebilmesi durumunda bu anahtarı kullanın.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId

Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VaultLocation

Kurtarma Hizmetleri kasasındaki konum.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WLRecoveryConfig

Kurtarma Yapılandırması

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase
Parameter Sets: AzureWorkloadParameterSet
Aliases:

Required: True
Position: 0
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

### -CommonParameters

Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. RecoveryPointBase

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Backup-Azrecoveryservicesbackupıtem](./Backup-AzRecoveryServicesBackupItem.md)

[Get-Azrecoveryservicesbackupıtem](./Get-AzRecoveryServicesBackupItem.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)
