---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 394500DB-D2BB-4793-8D9F-2CAF4D892A55
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/register-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Register-AzureRmBackupContainer.md
ms.openlocfilehash: 71c7d883994897e4dc4b450391fb50949a125c77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592951"
---
# Register-AzureRmBackupContainer

## SYNOPSIS
Kapsayıcıyı yedek kasası ile kaydeder.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### V1VM
```
Register-AzureRmBackupContainer -Name <String> -ServiceName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### V2VM
```
Register-AzureRmBackupContainer -Name <String> -ResourceGroupName <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Register-AzureRmBackupContainer** cmdlet 'ı bir Azure Yedekleme Kasası ile kaydeder.
Azure yedekleme 'yi kullanarak yedeklemeyi yapılandırmak için, önce sunucunuzu veya sanal makinenizi bir yedek kasası ile kaydettirin.
Bu cmdlet, bir altyapıyı belirtilen kasaya sahip bir hizmet (IaaS) sanal makinesi olarak kaydeder.
Register işlemi, Azure sanal makinesini yedek kasası ile ilişkilendirir ve sanal makineyi yedekleme yaşam döngüsü aracılığıyla izler.

## ÖRNEKLERDEN

### Örnek 1: yedekleme kasasına sanal makine kaydettirme
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Register-AzureRmBackupContainer -Vault $Vault -Name "Contoso03Vm" -ServiceName "ContosoService27"
```

İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.
Komut $Vault değişkeninde kasayı depolar.

İkinci komut, Contoso03Vm adındaki sanal makineyi $Vault kasaya kaydeder.
Bu sanal makine, ContosoService27 adlı hizmete aittir.

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

### -Ad
Bu cmdlet 'in kaydettiğinde kullandığı sanal makinenin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makine için kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: V2VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HizmetAdı
Bu cmdlet 'in kaydettiğinde kullandığı sanal makinenin hizmet adını belirtir.

Genellikle, bir bulut hizmeti adının soneki vardır. cloudapp.net.
Bu parametreyi belirttiğinizde sonek eklemeyin.

Sanal makine hakkında bilgi edinmek için Get-AzureRMVM cmdlet 'ini kullanın.
Hizmet adı, sanal makine nesnesinin **DeploymentName** özelliğidir.

```yaml
Type: String
Parameter Sets: V1VM
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kasa
Bu cmdlet 'in sanal makineyi kaydettiğinde Yedekleme Kasası 'nı belirtir.
**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Azurermbackupkasası

## ÇıKıŞLAR

### AzureRmBackupJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)


