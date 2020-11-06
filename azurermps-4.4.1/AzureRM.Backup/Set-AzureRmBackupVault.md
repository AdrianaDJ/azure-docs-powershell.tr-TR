---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: 82e86d27c5ef628e6cd6122fa024ac72788e79db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592673"
---
# Set-AzureRmBackupVault

## SYNOPSIS
Yedek kasanın depolama türünü değiştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-Azurermbackupkasa** cmdlet 'i, bir Azure Yedekleme Kasası depolama türünü değiştirir.
Kasanın diğer özelliklerini değiştiremezsiniz.

## ÖRNEKLERDEN

### Örnek 1: var olan bir kasanın deposunu değiştirme
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

Bu komut, **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı Azure Yedekleme Kasası 'nı alır.
Bu komut, ardışık düzen işlecini kullanarak bu kasayı geçerli cmdlet 'e geçirir.
Geçerli cmdlet depolama türünü Locallyyedekli olarak değiştirir.

## PARAMETRELERINE

### -Depolama
Yedekleme verileri için depolama türünü belirtir.
Bu parametre için kabul edilebilir değerler: Locallyyedekli ve Geoyedekli.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kasa
Bu cmdlet 'in değiştirdiği bir yedek Kasası belirtir.
**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.

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

### Azurermbackupkasası

## ÇıKıŞLAR

### Yabilirsiniz

## NOTLARıNDA
* Kasanın ilk sunucusunu veya sanal makinesini kaydettiğinizde, depolama türü kilitlenir. Ardından depolama türünü değiştiremezsiniz.

## ILGILI BAĞLANTıLAR

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Yeni-Azurermbackupkasası](./New-AzureRmBackupVault.md)

[Remove-Azurermbackupkasası](./Remove-AzureRmBackupVault.md)


