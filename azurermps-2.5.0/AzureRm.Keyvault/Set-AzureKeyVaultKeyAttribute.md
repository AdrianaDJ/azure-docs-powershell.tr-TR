---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultkeyattribute
schema: 2.0.0
ms.openlocfilehash: e7daafc147775b128351a7fa9ffb7b4d807bfe17
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939546"
---
# Set-AzureKeyVaultKeyAttribute

## SYNOPSIS
Anahtar kasasındaki bir anahtarın özniteliklerini güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureKeyVaultKeyAttribute** cmdlet 'i anahtar kasasındaki bir anahtarın düzenlenebilir özniteliklerini günceller.

## ÖRNEKLERDEN

### Örnek 1: etkinleştirmek için anahtarı değiştirme ve son kullanma tarihi ve etiketleri ayarlama
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

İlk komut **Get-Date** cmdlet 'ini kullanarak bir **DateTime** nesnesi oluşturur. Bu nesne gelecek yıl iki yıl belirtir. Komut bu tarihi $Expires değişkeninde depolar.
Daha fazla bilgi için yazın `Get-Help Get-Date` .

İkinci komut, yüksek önem düzeyi ve hesap oluşturma etiket değerlerini depolamak için bir değişken oluşturur.

Son komutu ITSoftware adındaki bir anahtarı değiştirir. Komut, anahtarı belirler, kullanım süresi sonunu $Expires depolanan saate göre ayarlar ve $Tags depolanan etiketleri ayarlar.

### Örnek 2: tüm etiketleri silmek için anahtarı değiştirme
```
PS C:\>Set-AzureKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

Bu komut, bir anahtarın ıtsoftware adındaki belirli bir sürümünün tüm etiketlerini siler.

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
Bir tuşun etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir. Anahtarı $True değeri etkinleştirilir. $False değeri devre dışı bırakılır. Bu parametreyi belirtmezseniz, bu cmdlet anahtarın durumunu değiştirmez.

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
Bu cmdlet 'in güncelleştirdiği anahtar için **DateTime** nesnesi olarak süre sonu belirtir. Bu parametre Eşgüdümlü Evrensel Saat (UTC) kullanır. **TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın. Daha fazla bilgi için yazın `Get-Help Get-Date` .

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

### -Keyolar
Bu cmdlet 'in eklediği anahtar kullanılarak gerçekleştirilebilen işlemlerin dizisini belirtir.
Bu parametreyi belirtmezseniz, tüm işlemler gerçekleştirilebilir.

Bu parametre için kabul edilebilir değerler, JSON Web anahtar belirtiminde tanımlanan, virgülle ayrılmış anahtar işlemleri listesidir. Bu değerler (büyük/küçük harf duyarlı):

- şifre
- çözmeye
- 02
- kaydırmamak
- ISS
- ayarlandığını
- yedeğinin
- Kurtarma

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Güncelleştirilecek anahtarın adını belirtir. Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotBefore
Bir **Tarih** saat nesnesi olarak, anahtarın kullanılamaz olduğunu belirtir.
Bu parametre UTC kullanır.
**TarihSaat** nesnesi almak için **Get-Date** cmdlet 'ini kullanın.

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
Bu cmdlet 'in anahtarı değiştirdiği Anahtar Kasası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği adı ve geçerli ortamınızı temel alan bir Anahtar Kasası FQDN 'sini oluşturur.

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
Anahtar sürümü belirtir.
Bu cmdlet, Anahtar Kasası adına, şu anda seçtiğiniz ortama, anahtar adına ve anahtar sürümüne bağlı olarak bir anahtarın FQDN 'sini oluşturur.

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

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

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. Keydemeti

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)
