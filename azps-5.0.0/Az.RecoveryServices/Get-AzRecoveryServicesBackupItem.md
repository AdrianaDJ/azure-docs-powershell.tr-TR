---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323068"
---
# Get-AzRecoveryServicesBackupItem

## SYNOPSIS

Yedeklemede öğeleri bir kapsayıcıdan alır.

## INDEKI

### Getıtemsforcontainer (varsayılan)
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getıtemsforkasası
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getıtemsforpolicy
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım

**Get-Azrecoveryservicesbackupıtem** cmdlet 'i kapsayıcıdaki korumalı öğelerin listesini ve öğelerin koruma durumunu alır.
Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.
Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir yedekleme öğesi olabilir.
-VaultId parametresini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: yedekleme kapsayıcısından öğe alma

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

İlk komut AzureVM türünde kapsayıcıyı alır ve $Container değişkeninde depolar.
İkinci komut $Container V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.

### Örnek 2: FriendlyName 'dan bir Azure dosya paylaşımı öğesi alma

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

İlk komut AzureStorage türünde kapsayıcıyı alır ve $Container değişkeninde depolar.
İkinci komut, friendlyName FriendlyName parametresinde geçirilen değeri eşleştiren yedekleme öğesini alır ve $BackupItem değişkeninde depolar.
FriendlyName parametresi kullanmak birden fazla Azure dosya paylaşımı döndürmeye neden olabilir. Böyle durumlarda, $BackupItem sonuç kümesinde döndürülen Name özelliği olarak-name parametresini geçirerek cmdlet 'i yürütün.

## PARAMETRELERINE

### -BackupManagementType

Korunan kaynakların sınıfı. Bu parametre için kabul edilebilir değerler şunlardır:

- AzureVM
- MAB
- AzureStorage
- AzureWorkload

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Kapsayıcı

Bu cmdlet 'in yedekleme öğelerini aldığı bir kapsayıcı nesnesi belirtir.
**Azurermrecoveryservicesbackupcontainer** almak için **Get-azrecoveryservicesbackupcontainer** cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DeleteState
Öğenin DeleteState değerini belirtir; Bu parametre için kabul edilebilir değerler şunlardır:

- ToBeDeleted
- NotDeleted

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FriendlyName
Yedeklenen öğenin FriendlyName

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad

Yedekleme öğesinin adını belirtir. Dosya paylaşımı için, korumalı dosya paylaşımının benzersiz KIMLIĞINI belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İlke

Koruma ilkesi nesnesi.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionState

Korumanın durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Irtpending.
İlk eşitleme başlatılmadı ve henüz kurtarma noktası yok.
- Korunamaz.
Koruma devam etmektedir.
- ProtectionError.
Koruma hatası var.
- Protectiondurdurdu.
Koruma devre dışı bırakıldı.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionStatus

Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Sağlık
- Sağlıklı

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
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

### -WorkloadType

Kaynağın iş yükü türü. Bu parametre için kabul edilebilir değerler şunlardır:

- AzureVM
- AzureFiles
- KLASÖRÜNÜN

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Backup-Azrecoveryservicesbackupıtem](./Backup-AzRecoveryServicesBackupItem.md)

[Disable-AzRecoveryServicesBackupProtection](./Disable-AzRecoveryServicesBackupProtection.md)

[Get-AzRecoveryServicesBackupRecoveryPoint](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[Restore-Azrecoveryservicesbackupıtem](./Restore-AzRecoveryServicesBackupItem.md)
