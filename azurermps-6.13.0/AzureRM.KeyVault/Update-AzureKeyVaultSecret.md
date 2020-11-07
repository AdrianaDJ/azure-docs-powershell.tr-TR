---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultSecret.md
ms.openlocfilehash: d895485354c33daa4eac57b699358ee0335905be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764648"
---
# Update-AzureKeyVaultSecret

## SYNOPSIS
Anahtar kasasındaki gizli öznitelikleri güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Varsayılan (varsayılan)
```
Update-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Update-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Update-AzureKeyVaultSecret** cmdlet 'i anahtar kasasındaki bir gizli kod öğesinin düzenlenebilir özniteliklerini günceller.

## ÖRNEKLERDEN

### Örnek 1: parolayı değiştirme
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

İlk dört komut son kullanma tarihi, Notöncesi tarihi, etiketleri ve bağlam türü özniteliklerini tanımlar ve öznitelikleri değişkenlere depolar.
Son komutu, depolanan değişkenleri kullanarak, Contosokasası adlı anahtar kasasına ık adlı parola ile ilgili öznitelikleri değiştirir.

### Örnek 2: gizli için etiketleri ve içerik türünü silme
```
PS C:\> Update-AzureKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Bu komut, contoso adlı anahtar kasasına HR adlı parola adlı gizli sürümün etiketlerini ve içerik türünü siler.

### Örnek 3: adı bununla başlayan gizli kod sürümlerini devre dışı bırakma
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzureKeyVaultSecret -Enable $False
```

İlk komut $Vault değişkeninde contoso dize değerini depolar.
İkinci komut, $Prefix değişkeninde dize değerini depolar.
Üçüncü komut, Get-AzureKeyVaultSecret cmdlet 'ini kullanarak belirtilen anahtar kasasındaki gizlilikleri alır ve bu gizlilikleri **WHERE-Object** cmdlet 'ine geçirir. **WHERE-Object** cmdlet 'i, adlarla başlayan adlarla ilgili gizli kod dizelerini süzer. Komut, filtreyle eşleşen gizli kod dizelerini devre dışı bırakan Update-AzureKeyVaultSecret cmdlet 'ine göre yöneltme içerir.

### Örnek 4: tüm gizli sürümleri için ContentType 'ı ayarlama
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzureKeyVaultSecret -ContentType $ContentType
```

İlk üç komut, *Vaultname* , *Name* ve *ContentType* parametrelerinde kullanılacak dize değişkenlerini tanımlar. Dördüncü komut, Get-AzureKeyVaultKey cmdlet 'ini kullanarak belirtilen tuşları alır ve içerik türlerini XML olarak ayarlamak için anahtarları Update-AzureKeyVaultSecret cmdlet 'ine kullanır.

## PARAMETRELERINE

### -ContentType
Gizli içerik türü.
Belirtilmezse, parola türünün varolan değeri değişmeden kalır.
Boş dize belirterek var olan içerik türü değerini kaldırın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Enable
Varsa, değer true ise parolayı etkinleştirin.
Değer yanlışsa parolayı devre dışı bırakın.
Belirtilmezse, parolanın etkin/devre dışı durumu değeri değişmeden kalır.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Süre sonu
UTC zamanında bir parolanın son kullanma tarihi.
Belirtilmemişse, parola süre sonu değeri değişmeden kalır.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Gizli nesne

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

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
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Parolanın kullanılmadığı UTC saati.
Belirtilmezse, parolanın Notöncesi özniteliğinin mevcut değeri değişmeden kalır.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Cmdlet, varsayılan olarak nesne döndürmez.
Bu anahtar belirtilmişse, gizli nesnesi döndürür.

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

### Etiketli
Gizli etiketleri temsil eden bir Hashtable.
Belirtilmezse, parolanın var olan etiketleri değişmeden kalır.
Boş bir Hashtable belirterek etiketi kaldırın.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Kasa adı.
Cmdlet, ad ve seçili durumdaki ortamı temel alan bir kasanın FQDN 'sini oluşturur.

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Gizli sürüm.
Cmdlet, kasa adının gizliliğini, seçili durumdaki ortamı, gizli adı ve gizli sürümü oluşturur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
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

### Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultsecretidentityıtem
Parametreler: InputObject (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultSecret

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
