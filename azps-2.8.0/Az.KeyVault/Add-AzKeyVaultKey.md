---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: f7447725e63634642f285b6a796a2b59b4d1d301
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751701"
---
# Add-AzKeyVaultKey

## SYNOPSIS
Anahtar Kasası içinde bir anahtar oluşturur veya anahtar kasasına anahtar aktarır.

## INDEKI

### Interactivecoluştur (varsayılan)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Interactiveımport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Inputobjectcreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Inputobjectimport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Resourceıdcreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Resourceidmport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Add-Azanahtarvaultkey** cmdlet 'ı Azure Anahtar Kasası 'ndaki bir Anahtar Kasası içinde bir anahtar oluşturur veya bir anahtarı anahtar kasasına aktarır.
Aşağıdaki yöntemlerden herhangi birini kullanarak anahtar eklemek için bu cmdlet 'i kullanın:
- Anahtar Kasası hizmetinde donanım güvenlik modülünde (HSM) bir anahtar oluşturun.
- Temel kasa hizmetinde yazılımda bir anahtar oluşturun.
- Anahtar Kasası hizmetinde kendi donanım güvenlik modülünden (HSM) bir anahtarı içe aktarın.
- Bilgisayarınızdaki. pfx dosyasından bir anahtar içeri aktarın.
- Bilgisayarınızdaki. pfx dosyasındaki bir anahtarı Anahtar Kasası hizmetindeki donanım güvenlik modüllerine (HSMs) aktarın.
Bu işlemlerden herhangi biri için, anahtar öznitelikleri sağlayabilir veya varsayılan ayarları kabul edebilirsiniz.
Anahtar kasasındaki varolan bir anahtarla aynı ada sahip bir anahtar oluşturabilir veya içeri aktarırsanız, özgün anahtar yeni anahtar için belirttiğiniz değerlerle güncelleştirilir. Anahtarın söz konusu sürümü için sürüme özgü URI 'yi kullanarak önceki değerlere erişebilirsiniz. Anahtar sürümleri ve URI yapısı hakkında bilgi edinmek için, Anahtar Kasası REST API belgelerinde [anahtarlar ve gizlilikler hakkında](https://go.microsoft.com/fwlink/?linkid=518560) konusuna bakın.
Not: bir anahtarı kendi donanım güvenlik modülünden içeri aktarmak Için, önce Azure Key kasa BYOK araç takımını kullanarak bir BYOK paketi (. bYok dosya adı uzantılı bir dosya) oluşturmanız gerekir. Daha fazla bilgi için [HSM-Protected anahtarları oluşturma ve aktarma](https://go.microsoft.com/fwlink/?LinkId=522252)
En iyi uygulama olarak, Backup-AzKeyVaultKey cmdlet 'ini kullanarak, oluşturulduktan veya güncelleştirildikten sonra anahtarınızı yedekleyin. Silmeyi geri alma işlevi yapılmaz, bu nedenle anahtarınızı yanlışlıkla sildiğiniz veya silerseniz ve ardından fikir olarak değiştirirseniz, geri yükleyebileceğiniz bir yedeğiniz yoksa anahtar kurtarılamaz.

## ÖRNEKLERDEN

### Örnek 1: anahtar oluşturma
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Bu komut, contoso adlı Anahtar Kasası 'nda ıtsoftware adlı bir yazılım korumalı anahtar oluşturur.

### Örnek 2: HSM korumalı anahtar oluşturma
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Bu komut, contoso adlı anahtar kasasına bir HSM korumalı anahtar oluşturur.

### Örnek 3: varsayılan olmayan değerlerle anahtar oluşturma
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

İlk komut, değerleri çözme ve $KeyOperations değişkeninde doğrulama değerlerini depolar.
İkinci komut, **Get-Date** cmdlet 'INI kullanarak UTC 'de tanımlanmış bir **DateTime** nesnesi oluşturur.
Bu nesne gelecek yıl iki yıl belirtir. Komut bu tarihi $Expires değişkeninde depolar. Daha fazla bilgi için yazın `Get-Help Get-Date` .
Üçüncü komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur. Bu nesne geçerli UTC zamanını belirtir. Komut bu tarihi $NotBefore değişkeninde depolar.
Final komutu, bir HSM korumalı anahtar olan Ithsmvarsayıladı adlı bir anahtar oluşturur. Komut $KeyOperations depolanan izin verilen anahtar işlemlerinin değerlerini belirtir. Komut, önceki komutlarda oluşturulan *son* ve *notöncesi* parametrelerinin zamanlarını ve yüksek önem düzeyi ve etiket etiketlerini belirtir. Yeni anahtar devre dışı bırakıldı. **Set-Azanahtarvaultkey** cmdlet 'ini kullanarak etkinleştirebilirsiniz.

### Örnek 4: HSM korumalı bir anahtarı Içeri aktarma
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Bu komut, *Keyfilepath* parametresinin belirttiği konumdan ityok adındaki anahtarı içeri aktarır. İçeri aktarılan anahtar, HSM korumalı bir anahtardır.
Kendi donanım güvenlik modülünden anahtar içeri aktarmak için, önce Azure Key kasa BYOK araç takımını kullanarak bir BYOK paketi (. bYok dosya adı uzantılı bir dosya) oluşturmanız gerekir.
Daha fazla bilgi için [HSM-Protected anahtarları oluşturma ve aktarma](https://go.microsoft.com/fwlink/?LinkId=522252)

### Örnek 5: Yazılım korumalı bir anahtarı Içeri aktarma
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Password değişkeninde depolar. Daha fazla bilgi için yazın `Get-Help
ConvertTo-SecureString` .
İkinci komut contoso tuş Kasası 'nda bir yazılım parolası oluşturur. Komut, anahtarın konumunu ve $Password depolanan parolayı belirtir.

### Örnek 6: anahtarı Içeri aktarma ve öznitelikleri atama
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

İlk komut, **ConvertTo-SecureString** cmdlet 'ini kullanarak dizgiyi güvenli dizeye dönüştürür ve bu dizeyi $Password değişkeninde depolar.
İkinci komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur ve bu nesneyi $Expires değişkeninde depolar.
Üçüncü komut yüksek önem düzeyi ve etiket ayarlamak için $tags değişkenini oluşturur.
Son komutu, anahtarı belirtilen konumdan HSM anahtarı olarak içeri aktarır. Komut $Password içinde depolanan $Expires ve parola ile saklanan son kullanma süresini belirtir ve $tags depolanan etiketleri uygular.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Hedef
Anahtarın anahtar kasası hizmetine yazılım korumalı anahtar mı yoksa HSM korumalı anahtar mı ekleneceğini belirtir.
Geçerli değerler: HSM ve yazılım.
Not: hedef olarak HSM 'yi kullanmak Için, HSMs 'yi destekleyen bir Anahtar Kasası olmalıdır. Azure Anahtar Kasası hizmet katmanları ve özellikleri hakkında daha fazla bilgi için, [Azure Anahtar Kasası fiyatlandırma web sitesine](https://go.microsoft.com/fwlink/?linkid=512521)bakın.
Yeni bir anahtar oluşturduğunuzda bu parametre gereklidir. Anahtarı anahtar *FilePath* parametresini kullanarak içeri aktarırsanız, bu parametre isteğe bağlıdır:
- Bu parametreyi belirtmezseniz ve bu cmdlet. bYok dosya adı uzantısına sahip bir anahtar aldığında, bu anahtarı HSM korumalı anahtar olarak alır. Cmdlet bu anahtarı yazılım korumalı anahtar olarak alamaz.
- Bu parametreyi belirtmezseniz ve bu cmdlet. pfx dosya adı uzantısına sahip bir anahtar aldığında, anahtarı yazılım korumalı anahtar olarak alır.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Devre dışı bırak
Eklediğiniz anahtarın başlangıçtaki durumuna ayarlı olduğunu gösterir. Anahtarı kullanma girişimleri başarısız olur. Daha sonra etkinleştirmeyi düşündüğünüz anahtarları önceden yüklüyorsanız, bu parametreyi kullanın.

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

### -Süre sonu
Bu cmdlet 'in eklediği anahtar için, **TarihSaat** nesnesi olarak sona erme zamanını belirtir. Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır. **TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın. Daha fazla bilgi için yazın `Get-Help Get-Date` . Bu parametreyi belirtmezseniz, anahtar sona ermez.

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
Kasa.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Anahtardosyasıparolası
Alınan dosyanın parolasını **SecureString** nesnesi olarak belirtir. **SecureString** nesnesi edinmek Için, **ConvertTo-SecureString** cmdlet 'ini kullanın. Daha fazla bilgi için yazın `Get-Help ConvertTo-SecureString` . Dosya adı uzantısı. pfx olan dosyayı içeri aktarmak için bu parolayı belirtmeniz gerekir.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Bu cmdlet 'in içeri aktardığından kullanılan anahtar malzemesini içeren yerel dosyanın yolunu belirtir.
Geçerli dosya adı uzantıları. bYok ve. pfx.
- Dosya bir. bYok dosyası ise, içeri aktarma sonrasında anahtar HSMs tarafından otomatik olarak korunur ve bu varsayılanı geçersiz kılamazsınız.
- Dosya. pfx dosyası ise, içeri aktarma işleminden sonra anahtar yazılım tarafından otomatik olarak korunur. Bu varsayılanı geçersiz kılmak için, anahtar HSM korumalı olacak şekilde *hedef* parametreyi HSM 'ye ayarlayın.
Bu parametreyi belirttiğinizde, *hedef* parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Keyolar
Bu cmdlet 'in eklediği anahtar kullanılarak gerçekleştirilebilen işlemlerin dizisini belirtir.
Bu parametreyi belirtmezseniz, tüm işlemler gerçekleştirilebilir.
Bu parametre için kabul edilebilir değerler, [JSON Web anahtarı (JWK) belirtiminde](https://go.microsoft.com/fwlink/?LinkID=613300)tanımlanan, virgülle ayrılmış anahtar işlemleri listesidir:
- Şifre
- Çözmeye
- 02
- Kaydırmamak
- ISS
- Ayarlandığını

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Anahtar kasasına eklenecek anahtarın adını belirtir. Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur. Ad, yalnızca 0-9, a-z, A-Z ve-(kesik çizgi simgesi) içeren 1 ila 63 karakter uzunluğunda olmalıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Bir **Tarih** saat nesnesi olarak, anahtarın kullanılamaz olduğunu belirtir. Bu parametre UTC kullanır. **TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın. Bu parametreyi belirtmezseniz, tuş hemen kullanılabilir.

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

### -RESOURCEID
Kasa kaynak kimliği.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Boyut
RSA anahtar boyutu, bit cinsinden. Belirtilmezse, hizmet güvenli bir varsayılan olacaktır.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Karma tablo biçiminde anahtar-değer çiftleri. Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}

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
Bu cmdlet 'in anahtarı eklediği Anahtar Kasası adını belirtir. Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
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

### Microsoft. Azure. Commands. Keykasa. modeller. Pskeykasa

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yedek-Aztuş Vaultkey](./Backup-AzKeyVaultKey.md)

[Get-Azanahtarvaultkey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Set-Azanahtarvaultkeyattribute](./Set-AzKeyVaultKeyAttribute.md)
