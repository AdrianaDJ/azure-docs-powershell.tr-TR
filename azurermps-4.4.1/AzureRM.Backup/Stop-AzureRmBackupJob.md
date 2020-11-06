---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d502596b8c5ddde576b5fd22ee31398b2c4e869a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594314"
---
# Stop-AzureRmBackupJob

## SYNOPSIS
Var olan yedekleme işini iptal eder.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Idfiltersset
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### İş Filtreleriayarla
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Stop-AzureRmBackupJob** cmdlet 'i mevcut bir Azure yedekleme işini iptal eder.
Çok uzun süren ve diğer etkinlikleri engelleyen bir işi durdurmak için bu parametreyi kullanın.

Yalnızca aşağıdaki iş türlerini iptal edebilirsiniz: 

- Yedeğinin
- Kurtarma

## ÖRNEKLERDEN

### Örnek 1: iş KIMLIĞI kullanarak yedekleme işini durdurma
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.

İkinci komut, **Get-AzureRmBackupJob** cmdlet 'ini kullanarak $Vault kasadan bir yedekleme işi alır.
Komut, işi $Job değişkeninde depolar.
Bu örnekte, belirtilen kasada yalnızca bir yedekleme işlemi vardır.

Son komutu belirtilen KIMLIĞE sahip işi durdurur.

### Örnek 2: tüm geri yükleme işlemlerini durdurma
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

Bu komut $Vault kasadaki tüm geri yükleme işlemlerini alır ve ardından bunları geçerli cmdlet 'e geçirerek ardışık düzen işlecini kullanın.
Geçerli cmdlet her işi durdurur.

## PARAMETRELERINE

### -Job
Bu cmdlet 'in iptal olduğu bir iş belirtir.
**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Bu cmdlet 'in iptal olduğu bir iş belirtir.
**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kasa
Bu cmdlet 'in işi iptal ettiğinde yedek kasayı belirtir.
**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
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

### AzureRmBackupJob

## ÇıKıŞLAR

### Yabilirsiniz

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


