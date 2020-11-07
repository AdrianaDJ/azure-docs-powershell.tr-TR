---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: F3774658-A5E4-40BE-9A85-B33C70BC0A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupContainer.md
ms.openlocfilehash: e20276d8a2dfec8ffb39665e5122cfe4be74dc42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762492"
---
# Get-AzureRmBackupContainer

## SYNOPSIS
Yedekleme kapsayıcılarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmBackupContainer [-Name <String>] -Type <AzureBackupContainerType>
 [-ManagedResourceGroupName <String>] [-Status <AzureBackupContainerRegistrationStatus>]
 [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmBackupContainer** cmdlet 'ı Azure yedekleme kapsayıcılarını alır.
**AzureBackupContainer** , veri kaynaklarını, korumalı öğeleri ve kurtarma noktalarını saklar.
**AzureBackupContainer** aşağıdakilerden biri olabilir: 
- Windows Server bilgisayarı
- Sistem Merkezi veri koruma Yöneticisi (SCDPM) sunucusu 
- Azure alt yapısı (IaaS) sanal makinesi yedekleme bir veri kaynağını veya öğeyi yedekleyebilmeniz için, bunu Azure yedekleme hizmeti ile tutan kapsayıcıyı kaydettirmelidir.
Yedek verileri yedekleme kasasına göndermek için kapsayıcının kimliklerinin doğrulanması gerekir.
Windows Server bilgisayarları ve SCDPM sunucuları için kayıt, sunucunun tam nitelikli etki alanı adıyla tutulur.

## ÖRNEKLERDEN

### Örnek 1: kasaya kaydedilen tüm sunucuları görüntüleme
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type Windows
Name                         Type               Status
----                         ----               ------
SERVER01.CONTOSO.COM          Windows            Registered
SERVER02.CONTOSO.COM          Windows            Registered
```

İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.
İkinci komut $Vault Windows 'un tür kapsayıcılarından tüm kapsayıcıları alır.

### Örnek 2: belirli bir kapsayıcıyı alma
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type SCDPM -Name "DPMSERVER.CONTOSO.COM"
Name                         Type               Status
----                         ----               ------
DPMSERVER.CONTOSO.COM        SCDPM              Registered
```

Bu komut, DPMSERVER adlı kapsayıcıyı alır. CONTOSO.COM.
Komut $Vault ve kapsayıcının türünü belirtir.

### Örnek 3: Tüm kaydedilen Azure sanal makinelerini görüntüleme
```
PS C:\>Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered 
Name                         Type               Status
----                         ----               ------
co03-vm                      AzureVM            Registered
```

Bu komut, $Vault 'daki kasadan kaydedilen sanal makineleri alır.

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

### -ManagedResourceGroupName
Kapsayıcıyla ilişkili kaynak grubunun adını belirtir.
Bu ad, Register-AzureRmBackupContainer cmdlet 'inin *ServiceName* veya *resourcegroupname* parametresi için belirttiğiniz değerle aynıdır.

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
Bu cmdlet 'in aldığı kapsayıcının adını belirtir.

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

### -Durum
Bu cmdlet 'in aldığı kapsayıcıların geçerli durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- NotRegistered 
- Kaydedilemedi 
- Kaydedilmesi

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered, Registering, NotRegistered

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tür
Bu cmdlet 'in aldığı kapsayıcıların türünü belirtir.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupContainerType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, SCDPM, AzureVM, AzureBackupServer, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kasa
Bu cmdlet 'in kapsayıcıları aldığı bir yedek Kasası belirtir.
**Azurermbackupkasası** edinmek için Get-AzureRmBackupVault cmdlet 'ini kullanın.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
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

### Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupkasası
Parametreler: kasa (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupContainer

## NOTLARıNDA
* Yabilirsiniz

## ILGILI BAĞLANTıLAR

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)

[Unregister-AzureRmBackupContainer](./Unregister-AzureRmBackupContainer.md)


