---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
ms.openlocfilehash: 719f0676b87cf785785b0adfbfde71ad2a6b965b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935768"
---
# Set-AzKeyVaultSecretAttribute

## SYNOPSIS
Anahtar kasasındaki gizli öznitelikleri güncelleştirir.

## INDEKI

```
Set-AzKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-Azanahtarvaultsecretattribute** cmdlet 'i, bir anahtar kasasındaki gizli kod niteliklerini günceller.

## ÖRNEKLERDEN

### Örnek 1: parolayı değiştirme
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

İlk dört komut son kullanma tarihi, Notöncesi tarihi, etiketleri ve bağlam türü özniteliklerini tanımlar ve öznitelikleri değişkenlere depolar.

Son komutu, depolanan değişkenleri kullanarak, Contosokasası adlı anahtar kasasına ık adlı parola ile ilgili öznitelikleri değiştirir.

### Örnek 2: gizli için etiketleri ve içerik türünü silme
```
PS C:\>Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

Bu komut, contoso adlı anahtar kasasına HR adlı parola adlı gizli sürümün etiketlerini ve içerik türünü siler.

### Örnek 3: adı bununla başlayan gizli kod sürümlerini devre dışı bırakma
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzKeyVaultSecretAttribute -Enable $False
```

İlk komut $Vault değişkeninde contoso dize değerini depolar.

İkinci komut, $Prefix değişkeninde dize değerini depolar.

Üçüncü komut, Get-AzKeyVaultSecret cmdlet 'ini kullanarak belirtilen anahtar kasasındaki gizlilikleri alır ve bu gizlilikleri **WHERE-Object** cmdlet 'ine geçirir. **WHERE-Object** cmdlet 'i, adlarla başlayan adlarla ilgili gizli kod dizelerini süzer. Komut, filtreyle eşleşen gizli kod dizelerini devre dışı bırakan Set-AzKeyVaultSecretAttribute cmdlet 'ine göre yöneltme içerir.

### Örnek 4: tüm gizli sürümleri için ContentType 'ı ayarlama
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzKeyVaultSecretAttribute -ContentType $ContentType
```

İlk üç komut, *Vaultname* , *Name* ve *ContentType* parametrelerinde kullanılacak dize değişkenlerini tanımlar. Dördüncü komut, Get-AzKeyVaultKey cmdlet 'ini kullanarak belirtilen tuşları alır ve içerik türlerini XML olarak ayarlamak için anahtarları Set-AzKeyVaultSecretAttribute cmdlet 'ine kullanır.

## PARAMETRELERINE

### -ContentType
Parolanın içerik türünü belirtir. Bu parametreyi belirtmezseniz, geçerli parolanın içerik türünde bir değişiklik olmaz. Var olan içerik türünü kaldırmak için boş bir dize belirtin.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Enable
Parolayı etkinleştirip etkinleştirmeyeceğinizi gösterir. Parolayı etkinleştirmek için $False veya parolayı etkinleştirmek için $True belirtin. Bu parametreyi belirtmezseniz, geçerli gizliliğin etkin veya devre dışı durumunda olan bir değişiklik yoktur.

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

### -Süre sonu
Gizli bir tarih ve saat değerini belirtir.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Parolanın adını belirtir. Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir gizli etki alanı adı (FQDN) oluşturur.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Parolanın kullanılmadığı en evrensel saat (UTC) değerini belirtir.
Bu parametreyi belirtmezseniz, geçerli gizliliğin NotBefore özniteliğindeki bir değişiklik yoktur.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Değiştirilecek Anahtar Kasası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği adı ve seçili olan ortamı belirten bir Anahtar Kasası FQDN 'sini oluşturur.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Gizli sürümü belirtir.
Bu cmdlet, Anahtar Kasası adına, şu anda seçili ortama, gizli adına ve gizli sürüme göre gizli bir FQDN oluşturur.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. Secret
Geçiş belirtildiyse Microsoft. Azure. Commands. Keykasa. model. gizli nesnesi döndürür. Aksi takdirde hiçbir şey geri döner.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azanahtarvaultkey](./Get-AzKeyVaultKey.md)

[Get-Azanahtarvaultsecret](./Get-AzKeyVaultSecret.md)

[Remove-AzKeyVaultSecret](./Remove-AzKeyVaultSecret.md)
