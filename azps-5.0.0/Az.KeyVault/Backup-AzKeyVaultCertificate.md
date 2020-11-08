---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280231"
---
# Backup-AzKeyVaultCertificate

## SYNOPSIS
Bir Anahtar Kasası içinde bir sertifikayı yedekler.

## INDEKI

### ByRef (varsayılan)
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Sertifika
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Backup-Azanahtarvaultcertificate** cmdlet 'i, bu sertifikayı indirip bir dosyada saklayarak bir anahtar kasasına yedekler.
Sertifikada birden çok sürüm varsa, tüm sürümleri yedeğe dahil edilir.
İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.
Bir yedeklenen sertifikayı yedeklediğiniz abonelikteki herhangi bir anahtar kasaya geri yükleyebilirsiniz; böylece kasa aynı Azure Coğrafya 'da yer alabilir.
Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır: 
- Kasayı yanlışlıkla eski bir şekilde silmeniz durumunda sertifikanın çevrimdışı bir kopyasını tutmak istiyorsunuz.
 
- Anahtar Kasası kullanarak bir sertifika oluşturdunuz ve şimdi nesneyi başka bir Azure bölgesine kopyalamak istiyor; böylece bu uygulamayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz.
Şifrelenen **-azanahtarvaultcertificate** cmdlet 'ini kullanarak sertifikayı şifreli biçimde alın ve ardından **restore-AzKeyVaultCertificate** cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin.

## ÖRNEKLERDEN

### Örnek 1: otomatik olarak oluşturulan dosya adıyla sertifikayı yedekleme
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

Bu komut Mykeykasası adındaki anahtar kasasından MyCert adlı sertifikayı alır ve bu sertifikanın yedeğini sizin için otomatik olarak adlandırılan bir dosyaya kaydeder ve dosya adını görüntüler.

### Örnek 2: sertifikayı belirtilen dosya adına yedekleme
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

Bu komut Mykeykasası adındaki anahtar kasasından MyCert adlı sertifikayı alır ve bu sertifikanın yedeğini Backup. blob adlı bir dosyaya kaydeder.

### Örnek 3: daha önce alınan bir sertifikayı belirtilen dosya adına yedekleyin, hedef dosyanın üzerine sormadan dosyaya yazılır.
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

Bu komut, $cert adlı sertifikanın yedeğini oluşturur. $Cert adlı kasada ad. VaultName, yedek. blob adlı bir dosyaya, zaten varsa dosyanın üzerine yazılır.

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
Yedeklenecek gizli, bir geri alma çağrısının çıkışından alınan ardışık düzen.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

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
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ÇıktıDosyası
Çıktı dosyası.
Sertifikanın yedeğinin depolanacağı çıkış dosyası.
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
Parameter Sets: ByCertificateName
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultcertificateıdentityıtem

## ÇıKıŞLAR

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
