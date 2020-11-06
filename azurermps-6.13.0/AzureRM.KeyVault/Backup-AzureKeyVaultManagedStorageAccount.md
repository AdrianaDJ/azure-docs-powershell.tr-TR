---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 1520acb94ffe587fb96eaa9c2ba565bcf31cc87e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594017"
---
# Backup-AzureKeyVaultManagedStorageAccount

## SYNOPSIS
Anahtar Kasası yönetimli depolama hesabını yedekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByStorageAccountName (varsayılan)
```
Backup-AzureKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByStorageAccount
```
Backup-AzureKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Backup-AzureKeyVaultManagedStorageAccount** cmdlet 'i, bu yönetilen depolama hesabını indirip bir dosyada saklayarak bir anahtar kasada yedekler.
İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.
Bir yedeklenen depolama hesabını yedeklediğiniz abonelikteki herhangi bir anahtar kasaya geri yükleyebilirsiniz; böylece kasa aynı Azure Coğrafya 'da yer alabilir.
Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır: 
- Kasayı yanlışlıkla yanlışlıkla silmeniz durumunda depolama hesabının çevrimdışı bir kopyasını tutmak istiyorsunuz.
 
- Anahtar Kasası kullanarak yönetilen depolama hesabı oluşturdunuz ve şimdi nesneyi başka bir Azure bölgesine kopyalamak istiyor; böylece bu uygulamayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.
**Backup-AzureKeyVaultManagedStorageAccount** cmdlet 'ini kullanarak yönetilen depolama hesabını şifreli biçimde alın ve ardından **restore-AzureKeyVaultManagedStorageAccount** cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.

## ÖRNEKLERDEN

### Örnek 1: yönetilen depolama hesabını otomatik olarak oluşturulan dosya adıyla yedekleme
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

Bu komut Mykeykasası adlı anahtar kasasından MyMSAK adlı yönetilen depolama hesabını alır ve bu yönetilen depolama hesabının yedeğini sizin için otomatik olarak adlandırılmış bir dosyaya kaydeder ve dosya adını görüntüler.

### Örnek 2: yönetilen depolama hesabını belirtilen dosya adına yedekleme
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Bu komut Mykeykasası adındaki anahtar kasasından MyMSAK adlı yönetilen depolama hesabını alır ve bu yönetilen depolama hesabının yedeğini Backup. blob adlı bir dosyaya kaydeder.

### Örnek 3: önceden alınmış bir yönetilen depolama hesabını belirtilen dosya adına yedekleyin, hedef dosyanın üzerine sormadan dosyaya yazılır.
```powershell
PS C:\> $msak = Get-AzureKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzureKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Bu komut $msak adlı yönetilen depolama hesabının yedeğini oluşturur. $Msak adlı kasada ad. VaultName, yedek. blob adlı bir dosyaya, zaten varsa dosyanın üzerine yazılır.

## PARAMETRELERINE

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

### -Force
Varsa, verilen dosyanın üzerine yaz

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Yedeklenecek depolama hesabı paketi, bir geri alma çağrısının çıkışından alınan ardışık düzen.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Gizli ad.
Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı ve gizli adı oluşturur.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ÇıktıDosyası
Çıktı dosyası.
Depolama hesabı yedeğinin depolanacağı çıkış dosyası.
Belirtilmezse, varsayılan bir dosya adı oluşturulur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Kasa adı.
Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultmanagedstorageaccountidentityıtem
Parametreler: InputObject (ByValue)

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
