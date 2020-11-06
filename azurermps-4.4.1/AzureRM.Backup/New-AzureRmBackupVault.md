---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: a6415d941646f335ba7cae4fc2aab39d75000ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591163"
---
# New-AzureRmBackupVault

## SYNOPSIS
Yedek Kasası oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-Azurermbackupkasa** cmdlet 'ı bir Azure Yedekleme Kasası oluşturur.
Bu cmdlet, kasa varlığına başvuru olarak davranan bir **Azurermbackupkasa** nesnesi döndürür.

## ÖRNEKLERDEN

### Örnek 1: yedek Kasası oluşturma
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Bu komut, Vault03 adında bir Azure Yedekleme Kasası oluşturur.
Kasa, Batı ABD bölgesindeki ResourceGroup01 adlı kaynak grubudur.
Kasa, varsayılan Geoyedekli depolama türünü kullanır.

### Örnek 2: yerel olarak yedekli depolama kullanan bir yedek Kasası oluşturma
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

Bu komut, Vault03 adında bir Azure Yedekleme Kasası oluşturur.
Kasa, Batı ABD bölgesindeki ResourceGroup02 adlı kaynak grubudur.
Kasa, Locallyyedekli depolama türünü kullanır.

## PARAMETRELERINE

### -Ad
Azure Yedekleme Kasası için bir ad belirtir.
Ad, kaynak grubunda benzersiz olmalıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bölge
Yedek kasanın olduğu bir Azure bölgesi belirtir.
Karma yedekleme senaryolarında, gecikme süresini azaltmak için bir bölgede şirket içi sunucusuna bir kasa oluşturmanızı öneririz.
Azure altyapısının hizmet (IaaS) sanal makineleri yedeklemesi için, kasa yerel sanal makinelerin keşif noktası olur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in yedek Kasası oluşturduğu mevcut bir Azure Kaynak grubunun adını belirtir.
Kaynak grubu oluşturmak için New-AzureRMResourceGroup cmdlet 'ini kullanın.
Kaynak grubunun ve Azure yedekleme kasasındaki aynı bölgede olması gerekmez.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Depolama
Yedekleme verileri için depolama türünü belirtir.
Bu parametre için kabul edilebilir değerler: Locallyyedekli ve Geoyedekli.
Varsayılan değer Geoyedekli değeridir.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
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

### Yabilirsiniz

## ÇıKıŞLAR

### Azurermbackupkasası

## NOTLARıNDA
* Yabilirsiniz

## ILGILI BAĞLANTıLAR

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Remove-Azurermbackupkasası](./Remove-AzureRmBackupVault.md)

[Set-Azurermbackupkasası](./Set-AzureRmBackupVault.md)


