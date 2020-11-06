---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: c479869cb150633ca926542552fab2aa7dc80b90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588002"
---
# Enable-AzureRmBackupProtection

## SYNOPSIS
Bir öğeyi Azure yedekleme koruma ilkesiyle ilişkilendirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Enable-AzureRmBackupProtection** cmdlet 'i bir öğeyi Azure yedekleme koruma ilkesiyle ilişkilendirir.
Koruma ilkesini etkinleştirmek için, önce var olan bir yedekleme öğesine ve var olan ilkeye sahip olmanız gerekir.
Her ikisi de aynı yedek kasaya ait olmalıdır.
Yedekleme zamanlaması, öğenin ilk kopyasını ve sonraki yedeklemelerin artımlı kopyasını yapar.

## ÖRNEKLERDEN

### Örnek 1: Azure sanal makinesinde korumayı etkinleştirme
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.

İkinci komut $Vault içinde kasa için DefaultPolicy adındaki yedekleme koruma ilkesini alır.
Komut bu nesneyi $Policy değişkeninde depolar.

Final komutu, değerleri bir cmdlet 'ten sonrakine geçirmek için ardışık düzen işlecini kullanır.
Get-AzureRmBackupContainer cmdlet 'ini kullanarak bir kapsayıcı alır.
Komut, Get-AzureRmBackupItem cmdlet 'ini kullanarak bu kapsayıcıdaki yedekleme öğesini alır.
Geçerli cmdlet, komutun bu cmdlet 'e geçirdiği öğe için $Policy depolanan ilkenin kullanılmasını olanaklı kılar.

## PARAMETRELERINE

### -Öğe
Bu cmdlet 'in korumayı etkinleştirmesine yönelik yedekleme öğesini belirtir.
**Azurermbackupöğesi** almak için Get-AzureRmBackupItem cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -İlke
Bu cmdlet 'in bir öğeyle ilişkilenirse koruma ilkesini belirtir.
**Azurermbackupprotectionpolicy** nesnesi almak için Get-AzureRmBackupProtectionPolicy cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Azurermbackupıtem

## ÇıKıŞLAR

### AzureRmBackupJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Backup-Azurermbackupıtem](./Backup-AzureRmBackupItem.md)

[Get-Azurermbackupıtem](./Get-AzureRmBackupItem.md)

[Get-AzureRmBackupProtectionPolicy](./Get-AzureRmBackupProtectionPolicy.md)


