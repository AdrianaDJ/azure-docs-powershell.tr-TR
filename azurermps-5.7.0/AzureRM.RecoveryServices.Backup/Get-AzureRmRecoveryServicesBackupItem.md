---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587501"
---
# Get-AzureRmRecoveryServicesBackupItem

## SYNOPSIS
Yedeklemede öğeleri bir kapsayıcıdan alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Getıtemsforcontainer (varsayılan)
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Getıtemsforkasası
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermrecoveryservicesbackupıtem** cmdlet 'i bir kapsayıcıdaki öğeleri veya Azure Backup 'daki bir değeri ve öğelerin koruma durumunu alır.

Azure kurtarma hizmetleri kasasına kaydedilen bir kapsayıcının korunabilir bir veya birden çok öğe olabilir.
Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir yedekleme öğesi olabilir.

Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: yedekleme kapsayıcısından öğe alma
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

İlk komut AzureVM türünde kapsayıcıyı alır ve $Container değişkeninde depolar.

İkinci komut $Container V2VM adındaki yedekleme öğesini alır ve $BackupItem değişkeninde depolar.

## PARAMETRELERINE

### -BackupManagementType
Yedekleme yönetim türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- AzureVM 
- MARS 
- SCDPM 
- AzureBackupServer AzureSQL

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Kapsayıcı
Bu cmdlet 'in yedekleme öğelerini aldığı bir kapsayıcı nesnesi belirtir.
**Azurermrecoveryservicesbackupcontainer** almak için Get-AzureRmRecoveryServicesBackupContainer cmdlet 'ini kullanın.

```yaml
Type: ContainerBase
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Kapsayıcının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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
Type: ItemProtectionState
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
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkloadType
İş yükü türünü belirtir. Bu parametre için kabul edilebilir değerler şunlardır:

- AzureVM 
- Azuressqldatabase

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. Itembase

### System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. modeller. ItemBase]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Backup-Azurermrecoveryservicesbackupıtem](./Backup-AzureRmRecoveryServicesBackupItem.md)

[Disable-AzureRmRecoveryServicesBackupProtection](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[Get-AzureRmRecoveryServicesBackupRecoveryPoint](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[Restore-Azurermrecoveryservicesbackupıtem](./Restore-AzureRmRecoveryServicesBackupItem.md)


