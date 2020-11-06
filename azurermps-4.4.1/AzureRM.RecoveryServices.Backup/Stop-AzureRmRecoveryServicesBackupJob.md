---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 63d90aa5f98f6710702a70e9609c7625626e34c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594195"
---
# Stop-AzureRmRecoveryServicesBackupJob

## SYNOPSIS
Çalışan işi iptal eder.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### JobFilterSet (varsayılan)
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Idfilterset
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Stop-AzureRmRecoveryServicesBackupJob** cmdlet 'i mevcut bir Azure yedekleme işini iptal eder.
Çok uzun süren ve diğer etkinlikleri engelleyen bir işi durdurmak için bu cmdlet 'i kullanın.

Yalnızca yedekleme ve geri yükleme işi türlerini iptal edebilirsiniz.

Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: yedekleme işini durdurma
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

İlk komut bir yedekleme işi alır ve işi $Job değişkeninde depolar.

Son komut $Job uygulamasında yedekleme işinin örnek KIMLIĞINI belirterek işi durdurur.

## PARAMETRELERINE

### -Job
Bu cmdlet 'in iptal olduğu bir iş belirtir.
**Backupjob** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupJob cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
İptal edilecek işin KIMLIĞINI belirtir.
ID, **Backupjob** nesnesinin InstanceId özelliğidir.
**Backupjob** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupJob seçeneğini kullanın.

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmRecoveryServicesBackupJob](./Get-AzureRmRecoveryServicesBackupJob.md)

[Wait-AzureRmRecoveryServicesBackupJob](./Wait-AzureRmRecoveryServicesBackupJob.md)


