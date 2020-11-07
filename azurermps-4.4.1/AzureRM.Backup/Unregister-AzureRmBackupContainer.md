---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 41209f3790b7520c50e3105f9ca7c4a5a0e79dfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764908"
---
# Unregister-AzureRmBackupContainer

## SYNOPSIS
Yedek kasasından kapsayıcıyı silme.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Unregister-AzureRmBackupContainer** cmdlet 'i, bir Azure yedekleme kasasından Windows sunucusunun veya Azure sanal makinesinin kaydını siler.
Bu cmdlet, yedek kasasından gelen başvuruları kaldırır.
Bir kapsayıcının kaydını silebilmek için, bu kapsayıcıyla ilişkili tüm korumalı verileri silmeniz gerekir.

## ÖRNEKLERDEN

### Örnek 1: Windows sunucusunun kaydını silme
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.

İkinci komut, Get-AzureRmBackupContainer cmdlet 'ini kullanarak $Vault belirtilen ada sahip bir kapsayıcı alır.
Komut bu nesneyi $Container değişkeninde depolar.

Son komutu, belirtilen Windows sunucusunun Azure yedekleme kasasından kaydını siler.

### Örnek 2: onaysız bir Windows sunucusunun kaydını silme
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

Bu komut, ilk örnekte olduğu gibi, belirtilen Windows Server 'ın Azure yedekleme kasasından kaydını siler.
Bu komut *Force* parametresini belirtir.
Bu nedenle, komut sizden onay istemez.

## PARAMETRELERINE

### Kapsayıcı
Bu cmdlet 'in kaydını belirttiği Windows Server veya Azure sanal makinesini belirtir.
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

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.
Bu parametre yalnızca Windows türündeki **AzureBackupContainer** nesnelerinde ilgilidir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### AzureBackupContainer

## ÇıKıŞLAR

### AzureBackupJob
Kapsayıcı türü Windows Server olduğunda, bu cmdlet $Null döndürür.

## NOTLARıNDA
* Yabilirsiniz

## ILGILI BAĞLANTıLAR

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Register-AzureRmBackupContainer](./Register-AzureRmBackupContainer.md)


