---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 860e87063810251075341cd1eddd013870734384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588691"
---
# Set-AzureRmStorageAccount

## SYNOPSIS
Depolama hesabını değiştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### StorageEncryption (varsayılan)
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### KeyvaultEncryption
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmStorageAccount** cmdlet 'ı Azure Depolama hesabını değiştirir.
Bu cmdlet 'i hesap türünü değiştirmek, müşteri etki alanını güncelleştirmek veya depolama hesabında etiketleri ayarlamak için kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: depolama hesabı türünü ayarlama
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

Bu komut depolama hesabı türünü Standard_RAGRS olarak ayarlar.

### Örnek 2: depolama hesabı için özel etki alanı ayarlama
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

Bu komut, bir depolama hesabı için özel bir etki alanı ayarlar.

### Örnek 3: blob ve dosya hizmetlerinde şifrelemeyi etkinleştirme
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

Bu komut, depolama hesabı için blob ve dosyada depolama hizmeti şifrelemesini etkinleştirilir.

### Örnek 4: erişim katmanı değerini ayarlama
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

Komut, erişim katmanı değerini Cool olarak ayarlar.

### Örnek 4: özel etki alanı ve etiketleri ayarlama
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

Komut, erişim katmanı değerini Cool olarak ayarlar.

### Örnek 5: Anahtar Kasası ile blob hizmetlerinde şifrelemeyi etkinleştirme
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

Bu komut, blob 'taki yeni oluşturulmuş bir Keykasası ile depolama hizmeti şifrelemesini etkinleştirmiştir.

### Örnek 6: anahtar kaynağı "Microsoft. Storage" olarak ayarlanmış dosya hizmetlerinde şifrelemeyi devre dışı bırakma
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

Bu komut, anahtar kaynağı "Microsoft. Storage" olarak ayarlanmış dosya hizmetlerindeki şifrelemeyi devre dışı bırakır

## PARAMETRELERINE

### -AccessTier
Bu cmdlet 'in değiştirdiği depolama hesabının erişim katmanını belirtir.
Bu parametre için kabul edilebilir değerler: kolay ve serin.

Erişim katmanını değiştirirseniz, ek ücretler ortaya çıkabilir.
Daha fazla bilgi için, bkz https://go.microsoft.com/fwlink/?LinkId=786482 https://go.microsoft.com/fwlink/?LinkId=786482) .
Depolama hesabı türü depolama ise, bu parametreyi belirtmeyin.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Atama kimliği
Azure Keykasa gibi temel yönetim hizmetleriyle kullanmak üzere bu depolama hesabı için yeni bir depolama hesabı kimliği oluşturup atayın.

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

### -Custometkialanıadı
Özel etki alanının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableEncryptionService
Bu cmdlet 'in depolama hizmeti için depolama hizmeti şifrelemesini devre dışı bırakıp bırakmadığını gösterir.
Azure Blob ve Azure dosya hizmetleri destekleniyor.

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEncryptionService
Bu cmdlet 'in depolama hizmeti için depolama hizmeti şifrelemesini etkinleştirilip etkinleştirilmediğini gösterir.
Azure Blob ve Azure dosya hizmetleri destekleniyor.

```yaml
Type: EncryptionSupportServiceEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Depolama hesabının https trafiğinin yalnızca etkinleştirilip etkinleştirilmediğini gösterir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Erişim katmanını değiştirirseniz, ek ücretler ortaya çıkabilir.
Daha fazla bilgi için, bkz https://go.microsoft.com/fwlink/?LinkId=786482 https://go.microsoft.com/fwlink/?LinkId=786482) .
Depolama hesabı türü depolama ise, bu parametreyi belirtmeyin.

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

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AnahtarAdı
Depolama hesabı şifrelemesi tuş kaynağı tuş Kasası anahtar

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyvaultEncryption
Depolama hesabı şifreleme KeySource 'un Microsoft. Keykasa olarak ayarlanması veya olmaması.
KeyName, KeyVersion ve KeyvaultUri belirtirseniz, depolama hesabı şifrelemesi tuş kaynağı da Microsoft 'a ayarlanır. tuş Kasası Hava durumu bu parametre ayarlandı veya yok.
```yaml
Type: SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultUri
Depolama hesabı şifrelemesi tuş kaynağı tuş Kasası tuş

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVersion
Depolama hesabı şifrelemesi tuş kaynağı tuş Kasası tuş sürümü

```yaml
Type: String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Değiştirilecek depolama hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Depolama hesabının değiştirileceği kaynak grubunun adını belirtir.

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

### -SkuName
Depolama hesabının SKU adını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Standard_LRS.
Yerel olarak yedekli depolama.
- Standard_ZRS.
Bölge ile yedekli depolama.
- Standard_GRS.
Coğrafi olarak yedekli depolama.
- Standard_RAGRS.
Okuma erişimi coğrafi depolama.
- Premium_LRS.
Premium yerel olarak yedekli depolama.

Standard_ZRS ve Premium_LRS türlerini diğer hesap türleriyle değiştiremezsiniz.
Diğer hesap türlerini Standard_ZRS veya Premium_LRS olarak değiştiremezsiniz.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEncryption
Depolama hesabı şifrelemesi anahtar kaynağının Microsoft. Storage olarak ayarlanması gerekip gerekmediği.

```yaml
Type: SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
New-AzureRmStorageAccount cmdlet 'inin *tür* parametresinde blobstorage değeri belirtirseniz, *accesstier* parametresi için bir değer belirtmeniz gerekir.

Bu *tür* parametre Için bir depolama alanı değeri belirtirseniz, *accesstier* parametresini belirtmeyin.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Usealt etki alanı
Dolaylı CName doğrulamasının etkinleştirilip etkinleştirilmeyeceğini gösterir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Yeni-AzureRmStorageAccount](./New-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)
