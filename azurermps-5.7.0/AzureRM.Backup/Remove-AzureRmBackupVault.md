---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 4b8098889cbec7bd313ffb2ed70c5384a7e24ef0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592972"
---
# Remove-AzureRmBackupVault

## SYNOPSIS
Yedek Kasası siler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-Azurermbackupkasa** cmdlet 'ı bir Azure Yedekleme Kasası siler.

Yedek bir kasayı silebilmek için önce bu, boş olmalıdır.
Altyapıyı bir hizmet (IaaS) sanal makine yedekleme verileri olarak kaldırmak için **Remove-AzureRmBackupContainer** cmdlet 'ini kullanın.
Diğer kaydedilmiş sunucuları ve yedekleme verilerini kaldırmak için **delete-registeredserver** cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: Azure Yedekleme Kasası silme
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

Bu komut, **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı Azure Yedekleme Kasası 'nı alır.
Bu komut, ardışık düzen işlecini kullanarak bu kasayı geçerli cmdlet 'e geçirir.
Geçerli cmdlet Kasası kaldırır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Force
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kasa
Bu cmdlet 'in kaldırıldığı bir yedek Kasası belirtir.
**Azurermbackupkasası** edinmek için Get-AzureRmBackupVault cmdlet 'ini kullanın.

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Azurermbackupkasası

## ÇıKıŞLAR

### Yabilirsiniz

## NOTLARıNDA
* Yabilirsiniz

## ILGILI BAĞLANTıLAR

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Yeni-Azurermbackupkasası](./New-AzureRmBackupVault.md)

[Set-Azurermbackupkasası](./Set-AzureRmBackupVault.md)


