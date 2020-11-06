---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: 4aac9e7079451eebda0c77ae663666fbd55dc9e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586687"
---
# Set-AzureKeyVaultCertificateAttribute

## SYNOPSIS
Sertifikanın düzenlenebilir özniteliklerini değiştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByName (varsayılan)
```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByInputObject
```
Set-AzureKeyVaultCertificateAttribute [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureKeyVaultCertificateAttribute** cmdlet 'i, bir sertifikanın düzenlenebilir özniteliklerini değiştirir.

## ÖRNEKLERDEN

### Örnek 1: sertifikayla ilişkili etiketleri değiştirme
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

İlk komut $Tags değişkenine anahtar/değer çiftleri dizisi atar.

İkinci komut, TestCert01 adındaki sertifikanın etiket değerini $Tags olarak ayarlar.

Final komutu, işlemi doğrulamak için Get-AzureKeyVaultCertificate cmdlet 'ini kullanarak TestCert01 sertifikasını görüntüler.

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

### -Enable
Sertifikanın etkinleştirilip etkinleştirilmeyeceğini gösterir.
Etkinleştirmek $False veya devre dışı bırakmak için $True belirtin.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Sertifika nesnesi

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Değiştirilecek sertifikanın adını belirtir. Bu cmdlet, bir sertifikanın FQDN 'sini Anahtar Kasası adına, şu anda seçtiğiniz ortama, sertifika adına ve sertifika sürümüne göre oluşturur.

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin:

@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Bu cmdlet 'in sertifikayı değiştirdiği tuş Kasası adını belirtir.
Bu cmdlet, ad ve seçili durumdaki ortamı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Sertifikanın sürümünü belirtir.
Bu cmdlet, bir sertifikanın FQDN 'sini Anahtar Kasası adına, şu anda seçtiğiniz ortama, sertifika adına ve sertifika sürümüne göre oluşturur.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultCertificate

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureKeyVaultCertificate](./Add-AzureKeyVaultCertificate.md)
