---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 7612a816db41e3befb58cc739bcc78e2d27ec8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587473"
---
# Unregister-AzureRmRecoveryServicesBackupManagementServer

## SYNOPSIS
Bir SCDPM sunucusunun veya yedek sunucunun kasasından kaydını siler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet 'ı bir System Center Data Protection Manager (SCDPM) sunucusunun veya kasadan bir Azure yedekleme sunucusunun kaydını siler.
Bu cmdlet, kasadaki kaydedilmemiş sunuculara yapılan başvuruları kaldırır.

Bir kapsayıcının kaydını silebilmek için, bu kapsayıcıyla ilişkili tüm korumalı verileri silmeniz gerekir.

Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: kasadan SCDPM sunucusunun kaydını silme
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

İlk komut dpmserver01.contoso.com adındaki yedekleme yönetim sunucusunu alır ve $BMS değişkeninde depolar.

İkinci komut, listeden SCDPM sunucusunu siler.

## PARAMETRELERINE

### -AzureRmBackupManagementServer
Kaydı kaldırmak için bir SCDPM sunucu nesnesi belirtir.
**Backupmanagementserver** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupManagementServer cmdlet 'ini kullanın.

```yaml
Type: BackupEngineBase
Parameter Sets: (All)
Aliases: 

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

### -Geçiş
Silinecek yedekleme yönetim sunucusunu döndür.

```yaml
Type: SwitchParameter
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmRecoveryServicesBackupManagementServer](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


