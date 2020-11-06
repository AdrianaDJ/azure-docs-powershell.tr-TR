---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/backup-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: e87ab3ec04378dc97e144d2b444ee5398ff4f4f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593324"
---
# Backup-AzureRmBackupItem

## SYNOPSIS
Yedekleme öğesi için yedekleme başlatır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Backup-Azurermbackupıtem** cmdlet 'i, yedekleme zamanlamasına bağlı olmayan korumalı bir Azure yedekleme öğesi için yedekleme başlatır.
Zamanlanmış bir yedekleme başarısız olduktan sonra, korumayı etkinleştirdikten veya yedekleme başlattıktan sonra bir ilk yedekleme yapabilirsiniz.
Var olan bir yedekleme işi çalışıyorsa, bu cmdlet başarısız olur.

## ÖRNEKLERDEN

### Örnek 1: sanal makineyi Yedeklemeyi başlatma
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.
İkinci komut, Get-AzureRmBackupContainer cmdlet 'ini kullanarak $Vault belirtilen ada sahip bir kapsayıcı alır.
Komut bu nesneyi $Container değişkeninde depolar.
Son komut, Get-AzureRmBackupItem cmdlet 'ini kullanarak $Container yedekleme öğelerini alır.
Komut, ardışık düzen işlecini kullanarak öğeleri geçerli cmdlet 'e geçirir.
Geçerli cmdlet, kapsayıcıdaki sanal makineyi yedeklemeye başlar.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Öğe
Bu cmdlet 'in yedekleme işlemini başlattığı yedekleme öğesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupıtem
Parametreler: Item (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermbackupıtem](./Get-AzureRmBackupItem.md)

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Restore-Azurermbackupıtem](./Restore-AzureRmBackupItem.md)


