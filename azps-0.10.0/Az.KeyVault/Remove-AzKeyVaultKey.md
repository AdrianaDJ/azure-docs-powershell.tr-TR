---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: 15470f18e457f31deec66554c955890b52e26e83
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935774"
---
# Remove-AzKeyVaultKey

## SYNOPSIS
Anahtar kasasındaki bir anahtarı siler.

## INDEKI

```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Remove-AzKeyVaultKey cmdlet 'i anahtar kasadaki bir anahtarı siler.
Anahtar yanlışlıkla silinmişse anahtar, özel ' Recover ' izinlerine sahip bir kullanıcı tarafından Undo-AzKeyVaultKeyRemoval kullanılarak kurtarılabilir.
Bu cmdlet 'in **ConfirmImpact** özelliği için yüksek değeri vardır.

## ÖRNEKLERDEN

### Örnek 1: anahtar kasasından anahtar kaldırma
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı kaldırır.

### Örnek 2: Kullanıcı onayı olmadan bir anahtarı kaldırma
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı kaldırır.
Komut *Force* ve *Onayla* parametrelerini belirtir ve bu nedenle cmdlet sizden onay için istemde bulunmaz.

### Örnek 3: silinen anahtarı anahtar kasasından kalıcı olarak Temizleme
```
PS C:\>Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

Bu komut, contoso adlı anahtar kasasından ITSoftware adındaki anahtarı temizler.
Bu cmdlet 'i çalıştırmak için, bu Anahtar Kasası için önceden kullanıcıya önceden atanmış olması gereken ' Temizle ' izni gerekir.

### Örnek 4: ardışık düzen işlecini kullanarak anahtarları kaldırma
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

Bu komut contoso adlı anahtar kasasındaki tüm anahtarları alır ve ardışık düzen işlecini kullanarak bunları **nesne** cmdlet 'ine geçirir.
Bu cmdlet geçerli cmdlet 'e **Enabled** özniteliği için $false değeri olan anahtarları geçirir.
Bu cmdlet bu tuşları kaldırır.

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
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -Inremovevseçstate
Önceden silinen anahtarı kalıcı olarak kaldırın.

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

### -Ad
Kaldırılacak anahtarın adını belirtir.
Bu cmdlet, bu parametrenin belirttiği adı, Anahtar Kasası adını ve geçerli ortamınızı belirten bir anahtarın tam etki alanı adını (FQDN) oluşturur.

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

### -Geçiş
Bu cmdlet 'in bir **Microsoft. Azure. Commands. Keykasa. model. Keydemeti** nesnesi döndürmediğini gösterir.
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

### -VaultName
Anahtarın kaldırılacağı Anahtar Kasası adını belirtir.
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
Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.
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

### Dizisi

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. Deletedkeydemeti
Bu cmdlet yalnızca *geçiş parametresini belirttiğinizde* bir değer döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azanahtarvaultkey](./Add-AzKeyVaultKey.md)

[Get-Azanahtarvaultkey](./Get-AzKeyVaultKey.md)

[Set-Azanahtarvaultkeyattribute](./Set-AzKeyVaultKeyAttribute.md)

[Geri al-Aztuş Vaultkeykaldırması](./Undo-AzKeyVaultKeyRemoval.md)

