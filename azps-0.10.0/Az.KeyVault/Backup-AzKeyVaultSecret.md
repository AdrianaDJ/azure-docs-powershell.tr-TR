---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: b1f26123579589c15ac4eff6b577706270a7e15a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935808"
---
# Backup-AzKeyVaultSecret

## SYNOPSIS
Bir Anahtar Kasası içinde gizliliği yedekler.

## INDEKI

### BySecretName (varsayılan)
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BySecret
```
Backup-AzKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Backup-Azanahtarvaultsecret** cmdlet 'i, anahtarı indirip bir dosyada saklayarak, bir Anahtar Kasası 'nda belirtilen gizliliği yedekler.
Gizlilik 'in birden çok sürümü varsa, tüm sürümler yedeğe dahil edilir.
İndirilen içerik şifreli olduğundan, Azure Anahtar Kasası dışında kullanılamaz.
Yedeklenmiş bir parolayı, yedeklediğiniz abonelikteki herhangi bir anahtar kasasına geri yükleyebilirsiniz.

Bu cmdlet 'i kullanmanın tipik nedenleri şunlardır:

- Gizli bir kopyasını, anahtar kasasına yanlışlıkla silmeniz olasılığına karşı çevrimdışı bir kopya oluşturmak istiyorsunuz.
- Bir anahtar kasaya gizli eklediniz ve şimdi parolayı başka bir Azure bölgesine kopyalamak istiyorsunuz, böylece bu parolayı dağıtılmış uygulamanızın tüm örneklerinden kullanabilirsiniz. Parolayı şifreli biçimde almak için Backup-AzKeyVaultSecret cmdlet 'ini kullanın ve Restore-AzKeyVaultSecret cmdlet 'ini kullanın ve ikinci bölgede bir Anahtar Kasası belirtin. (Bölgelerin aynı coğrafya 'ya ait olması gerektiğini unutmayın.)

## ÖRNEKLERDEN

### Örnek 1: otomatik olarak oluşturulan bir dosya adıyla parolayı yedekleme
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

Bu komut Mykeykasası adlı anahtar kasasından MySecret adındaki parolayı alır ve bu gizli dosyanın bir yedeğini sizin için otomatik olarak adlandırılan bir dosyaya kaydeder ve dosya adını görüntüler.

### Örnek 2: parolayı belirli bir dosya adına yedekleme
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

Bu komut Mykeykasası adındaki anahtar vaultmysecret adlı parolayı alır ve bu gizli dosyanın bir yedeğini Backup. blob adlı bir dosyaya kaydeder.

### Örnek 3: daha önce belirli bir dosya adına alınan bir parolayı yedekleme
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

Bu komut, parolayı almak için $secret nesnenin kasa adını ve adını kullanır ve yedeklemesini Backup. blob adlı bir dosyaya kaydeder.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Varsa, çıkış dosyasının üzerine yazmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Yedekleme için parola adını belirtir.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ÇıktıDosyası
Yedekleme bloonun depolandığı çıkış dosyasını belirtir.
Bu parametreyi belirtmezseniz, bu cmdlet sizin için bir dosya adı oluşturur.
Var olan bir çıkış dosyasının adını belirtirseniz, işlem tamamlanmıştır ve yedekleme dosyasının zaten var olduğunu belirten bir hata iletisi döndürür.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parola
Yedekleme işlemi için adı ve Kasası kullanılması gereken nesneyi belirtir.

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Yedekleme için parolayı içeren Anahtar Kasası adını belirtir.

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Dizisi
Cmdlet, anahtarın yedeğini içeren çıkış dosyasının yolunu döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-Azanahtarvaultsecret](./Set-AzKeyVaultSecret.md)

[Get-Azanahtarvaultsecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)

[Restore-Azanahtarvaultsecret](./Restore-AzKeyVaultSecret.md)

