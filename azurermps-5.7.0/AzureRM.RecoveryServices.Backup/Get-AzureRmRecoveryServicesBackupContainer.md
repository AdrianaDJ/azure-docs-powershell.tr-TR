---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c861c9f18f2fb91838b8e527e2c3ee637098c00a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587503"
---
# Get-AzureRmRecoveryServicesBackupContainer

## SYNOPSIS
Yedekleme kapsayıcılarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmRecoveryServicesBackupContainer** cmdlet 'i bir yedekleme kapsayıcısını alır.
Yedekleme kapsayıcısı, yedek öğeler olarak modelli veri kaynaklarını saklar.

Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: belirli bir kapsayıcıyı alma
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

Bu komut, AzureVM türünde V2VM adlı kapsayıcıyı alır.

### Örnek 2: belirli bir türdeki tüm kapsayıcıları alma
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

Bu komut, Azure Yedekleme aracısı tarafından korunan tüm Windows kapsayıcılarını alır.
*Backupmanagementtype* parametresi yalnızca Windows kapsayıcıları için gereklidir.

## PARAMETRELERINE

### -BackupManagementType
Yedekleme yönetim türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- AzureVM
- MARS
- AzureSQL

Bu parametre, MARS Aracısı veya diğer yedekleme altyapıları kullanılarak yedeklenen Windows makinelerini ayırt etmek için kullanılır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerType
Yedekleme kapsayıcısı türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- AzureVM 
- WINDOWS
- AzureSQL

```yaml
Type: ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
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

### -FriendlyName
Alınacak kapsayıcının kolay adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Alınacak kapsayıcının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.
Bu parametre yalnızca Azure sanal makinelerinde kullanılır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Durum
Kapsayıcı kayıt durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Kaydedilemedi

```yaml
Type: ContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered

Required: False
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

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase

### System. Koleksiyonlar. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermrecoveryservicesbackupıtem](./Get-AzureRmRecoveryServicesBackupItem.md)

[Get-AzureRmRecoveryServicesBackupManagementServer](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[Unregister-AzureRmRecoveryServicesBackupContainer](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


