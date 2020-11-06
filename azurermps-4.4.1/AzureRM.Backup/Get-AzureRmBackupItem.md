---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 543aa3e28d7f3dee20065a0d20f2429b3fd6d4f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588000"
---
# Get-AzureRmBackupItem

## SYNOPSIS
Yedeklemede bir kapsayıcının altındaki öğeleri alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermbackupıtem** cmdlet 'ı Azure Backup 'daki bir kapsayıcıdaki öğeleri ve öğelerin koruma durumunu alır.
Enable-AzureRmBackupProtection cmdlet 'ini kullanarak öğeleri koruma için etkinleştirin.

Yedek kasaya kaydedilen bir kapsayıcı, korunabilir bir veya birden çok öğe içerebilir.
Azure sanal makinelerinde, sanal makine kapsayıcısında yalnızca bir öğe olabilir.

## ÖRNEKLERDEN

### Örnek 1: kapsayıcıdaki öğeleri alma
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.

İkinci komut, **Get-AzureRmBackupContainer** cmdlet 'ini kullanarak $Vault kasada belirtilen ada sahip bir kapsayıcı alır.
Komut bu nesneyi $Container değişkeninde depolar.

Son komutu $Container kapsayıcısındaki yedekleme öğesini alır.

### Örnek 2: öğenin tüm özelliklerini görüntüleme
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

Bu komut, $Container kapsayıcısındaki yedekleme öğesini alır ve Select-Object cmdlet 'ine geçirir.
Bu cmdlet yedek öğesinin tüm özelliklerini döndürür.
Daha fazla bilgi için yazın `Get-Help Select-Object` .

## PARAMETRELERINE

### Kapsayıcı
Bu cmdlet 'in yedekleme öğelerini aldığı kapsayıcı nesnesini belirtir.
**Azurermbackupcontainer** almak için Get-AzureRmBackupContainer cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionStatus
Kapsayıcıdaki bir öğenin genel koruma durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Korunamaz 
- Bilgilerinizin  
- NotProtected

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Durum
Öğenin yedekleme durumunu belirtir.
Bu parametre için kabul edilebilir değerler: ırpending, protected, ProtectionError ve Protectiondurdurdu.
*Protectionstatus* parametresinde değer varsa, öğeleri filtrelemek için *durum* parametre değerini kullanabilirsiniz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tür
Bu cmdlet 'in aldığı öğenin türünü belirtir.
Şu anda desteklenen tek değer AzureVM.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
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

### AzureRmBackupContainer

## ÇıKıŞLAR

### Azurermbackupıtem

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Backup-Azurermbackupıtem](./Backup-AzureRmBackupItem.md)

[Disable-AzureRmBackupProtection](./Disable-AzureRmBackupProtection.md)

[Enable-AzureRmBackupProtection](./Enable-AzureRmBackupProtection.md)

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Restore-Azurermbackupıtem](./Restore-AzureRmBackupItem.md)


