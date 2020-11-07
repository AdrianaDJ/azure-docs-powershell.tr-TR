---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935792"
---
# Get-AzKeyVaultKey

## SYNOPSIS
Önemli kasa anahtarlarını alır.

## INDEKI

### ByVaultName (varsayılan)
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByDeletedKey
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azanahtarvaultkey** cmdlet 'ı Azure Anahtar Kasası anahtarlarını alır.
Bu cmdlet, belirli bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** veya Anahtar Kasası veya sürüme göre tüm **anahtar paketi** nesnelerinin bir listesini alır.

## ÖRNEKLERDEN

### Örnek 1: anahtar kasasındaki tüm anahtarları alma
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

Bu komut, contoso adlı anahtar kasasındaki tüm anahtarları alır.

### Örnek 2: anahtarın geçerli sürümünü alma
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

Bu komut, contoso adlı anahtar kasasına ITPfx adlı anahtarın geçerli sürümünü alır.

### Örnek 3: anahtarın tüm sürümlerini alma
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

Bu komut, contoso adındaki anahtar vaultile ıpfx adındaki anahtarın tüm sürümlerini alır.

### Örnek 4: anahtarın belirli bir sürümünü alma
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

Bu komut, contoso adlı anahtar kasasına ITPfx adlı anahtarın belirli bir sürümünü alır.
Bu komutu çalıştırdıktan sonra, $Key nesnesinde gezinerek anahtarın çeşitli özelliklerini inceleyebilirsiniz.

### Örnek 5: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm anahtarları edinin.
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

Bu komut, contoso adlı tuş kasasına önceden silinen ancak temizlenmemayan tüm anahtarları alır.

### Örnek 6: silinen, ancak bu Anahtar Kasası için temizlenmiş olan anahtar ıpfx 'i alır.
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

Bu komut, contoso adlı Anahtar Kasası 'nda, daha önce silinmiş ancak temizlenmemişti olan anahtar.
Bu komut, silme tarihi gibi meta verileri ve bu silinmiş anahtarın zamanlanan Temizleme tarihini döndürür.

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

### -Includeversions
Bu cmdlet 'in bir anahtarın tüm sürümlerini aldığını gösterir.
Anahtarın geçerli sürümü listedeki ilk sürümdür.
Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.

*Includeversions* parametresini belirtmezseniz, bu cmdlet anahtarın belirtilen *ada* sahip geçerli sürümünü alır.

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inremovevseçstate
Çıktıda önceden silinen anahtarların gösterilip gösterilmeyeceğini belirtir

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Alınacak anahtar paketi adını belirtir.

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VaultName
Bu cmdlet 'in anahtarları aldığı Anahtar Kasası adını belirtir.
Bu cmdlet, bu parametrenin belirttiği adı ve seçtiğiniz ortamı belirten bir Anahtar Kasası tam etki alanı adını (FQDN) oluşturur.

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
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Dizisi

## ÇıKıŞLAR

### Liste<Microsoft. Azure. Commands. Keykasa. modeller. Keyıdentityıtem>, Microsoft. Azure. Commands. keykasa. modeller., liste<Microsoft. Azure. Commands. keykasa. modeller>.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azanahtarvaultkey](./Add-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

[Geri al-Aztuş Vaultkeykaldırması](./Undo-AzKeyVaultKeyRemoval.md)

[Set-Azanahtarvaultkeyattribute](./Set-AzKeyVaultKeyAttribute.md)

