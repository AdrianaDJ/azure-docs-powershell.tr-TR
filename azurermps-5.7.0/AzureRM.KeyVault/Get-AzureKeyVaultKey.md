---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592491"
---
# Get-AzureKeyVaultKey

## SYNOPSIS
Önemli kasa anahtarlarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ByVaultName (varsayılan)
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyName
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKeyVersions
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectVaultName
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByInputObjectKeyName
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByKInputObjecteyVersions
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureKeyVaultKey** cmdlet 'ı Azure Key kasa anahtarlarını alır.
Bu cmdlet, belirli bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** veya Anahtar Kasası veya sürüme göre tüm **anahtar paketi** nesnelerinin bir listesini alır.

## ÖRNEKLERDEN

### Örnek 1: anahtar kasasındaki tüm anahtarları alma
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

Bu komut, contoso adlı anahtar kasasındaki tüm anahtarları alır.

### Örnek 2: anahtarın geçerli sürümünü alma
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

Bu komut, contoso adlı anahtar kasasına ITPfx adlı anahtarın geçerli sürümünü alır.

### Örnek 3: anahtarın tüm sürümlerini alma
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

Bu komut, contoso adındaki anahtar vaultile ıpfx adındaki anahtarın tüm sürümlerini alır.

### Örnek 4: anahtarın belirli bir sürümünü alma
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

Bu komut, contoso adlı anahtar kasasına ITPfx adlı anahtarın belirli bir sürümünü alır.
Bu komutu çalıştırdıktan sonra, $Key nesnesinde gezinerek anahtarın çeşitli özelliklerini inceleyebilirsiniz.

### Örnek 5: silinmiş ancak bu Anahtar Kasası için temizlenmiş tüm anahtarları edinin.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

Bu komut, contoso adlı tuş kasasına önceden silinen ancak temizlenmemayan tüm anahtarları alır.

### Örnek 6: silinen, ancak bu Anahtar Kasası için temizlenmiş olan anahtar ıpfx 'i alır.
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

Bu komut, contoso adlı Anahtar Kasası 'nda, daha önce silinmiş ancak temizlenmemişti olan anahtar.
Bu komut, silme tarihi gibi meta verileri ve bu silinmiş anahtarın zamanlanan Temizleme tarihini döndürür.

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

### -Includeversions
Bu cmdlet 'in bir anahtarın tüm sürümlerini aldığını gösterir.
Anahtarın geçerli sürümü listedeki ilk sürümdür.
Bu parametreyi belirtirseniz, *Name* ve *vaultname* parametrelerini de belirtmeniz gerekir.

*Includeversions* parametresini belirtmezseniz, bu cmdlet anahtarın belirtilen *ada* sahip geçerli sürümünü alır.

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Tuş Kasası nesnesi.

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Inremovevseçstate
Çıktıda önceden silinen anahtarların gösterilip gösterilmeyeceğini belirtir

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Alınacak anahtar paketi adını belirtir.

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
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
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
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
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Dizisi

## ÇıKıŞLAR

### Liste<Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultkeyıdentityıtem>, Microsoft. Azure. Commands. Keykasa. modeller. PSKeyVaultKey, liste<Microsoft.Azure.Commands.KeyVault.Models.PSDEletedkeyvaultkeyıdentityıtem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureKeyVaultKey](./Add-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Geri al-AzureKeyVaultKeyRemoval](./Undo-AzureKeyVaultKeyRemoval.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)

