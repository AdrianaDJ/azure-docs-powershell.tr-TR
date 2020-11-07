---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: c11170e6bee80b9eaa19135ad604d8bf70e1baab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763475"
---
# Get-AzureRmBackupVault

## SYNOPSIS
Yedek Kasası alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermbackupkasa** cmdlet 'ı Azure yedek Kasası alır.
Bu cmdlet diğer cmdlet 'ler için **Azurermbackupkasa** nesneleri döndürür.

## ÖRNEKLERDEN

### Örnek 1: tüm yedekleme örneklerini görüntüleme
```
PS C:\>Get-AzureRmBackupVault
```

Bu komut tüm Azure yedekleme yerlerini alır.

### Örnek 2: Batı ABD 'de oluşturulan tüm kasa görünümü
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

Bu komut tüm yedekleme yerlerini alır.
Komut, ardışık düzen işlecini kullanarak bunları Where-Object cmdlet 'ine geçirir.
Bu cmdlet, **bölgeyi bölge** özelliğine göre filtreler.
Daha fazla bilgi için yazın `Get-Help Where-Object` .

### Örnek 3: belirli bir kasa alma
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

Bu komut Vault03 adındaki kasayı alır.

### Örnek 4: yerel olarak yedekli depolama alanı olan kasa sayısını sayma
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

Bu komut tüm Azure yedekleme yerlerini alır.
Bu komut, sonuçları **depolama** özelliğine dayalı olarak filtreleyen **yere** geçirir.
Komut, Locallyyedekli değeri olan Measure-Object cmdlet 'ine sahip olan sonuçları sayar.
Daha fazla bilgi için yazın `Get-Help Measure-Object` .

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

### -Ad
Bu cmdlet 'in aldığı yedek kasanın adını belirtir.
Birden fazla yedek Kasası aynı ada sahipse, bu cmdlet bunları döndürür.
Benzersiz bir kasa almak için *Resourcegroupname* parametresini belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in yedek Kasası aldığı Azure Kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AzureBackup. modeller. Azurermbackupkasası

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBackupContainer](./Get-AzureRmBackupContainer.md)

[Yeni-Azurermbackupkasası](./New-AzureRmBackupVault.md)

[Remove-Azurermbackupkasası](./Remove-AzureRmBackupVault.md)

[Set-Azurermbackupkasası](./Set-AzureRmBackupVault.md)


