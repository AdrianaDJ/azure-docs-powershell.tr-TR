---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274242"
---
# Wait-AzRecoveryServicesBackupJob

## SYNOPSIS

Yedekleme işinin bitmesini bekler.

## INDEKI

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım

**Wait-AzRecoveryServicesBackupJob** cmdlet 'ı bir Azure yedekleme işinin bitmesini bekler.
Yedekleme işleri uzun zaman alabilir.
Bir yedekleme işini bir komut dosyasının parçası olarak çalıştırırsanız, diğer görevlere devam etmeden önce bu komut dosyasının işin bitmesini beklemeye zorlamak isteyebilirsiniz.
Bu cmdlet 'i içeren bir komut dosyası, iş durumu için yedekleme hizmetini yoklayıp birden kolay olabilir.
-VaultId parametresini kullanarak kasa bağlamını ayarlayın.

## ÖRNEKLERDEN

### Örnek 1: işin bitmesini bekle

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

Bu komut dosyası, iş tamamlanana kadar devam eden ilk işi yoklar veya zaman aşımı süresi 1 saattir.

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

### -Job

Bekleme işini belirtir.
**Backupjob** nesnesi edinmek için **Get-AzRecoveryServicesBackupJob** cmdlet 'ini kullanın.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Timeout

Bu cmdlet işin bitmesini beklediği en uzun süreyi saniye cinsinden belirtir.
Zaman aşımı değeri belirtmeniz önerilir.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. Object

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzRecoveryServicesBackupJob](./Get-AzRecoveryServicesBackupJob.md)
