---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105870"
---
# Remove-AzureAccount

## SYNOPSIS
Windows PowerShell 'den bir Azure hesabını siler.

## INDEKI

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Remove-AzureAccount** cmdlet 'i, gezici kullanıcı profilinizdeki abonelik verileri dosyasındaki bir Azure hesabını ve aboneliğini siler.
Hesabı Microsoft Azure 'dan silmez veya fiili hesabı hiçbir şekilde değiştirmez.

Bu cmdlet 'i kullanmak, Azure hesabınızda oturum açmak gibi çok kullanışlıdır.
Ve hesapta yeniden oturum açmak istiyorsanız, **Add-AzureAccount** veya **Import-Azuyeniden yayımlayan ayarları dosyasını** kullanarak hesabı Windows PowerShell 'e yeniden ekleyin.

Ayrıca **Remove-AzureAccount** cmdlet 'ini kullanarak Azure PowerShell cmdlet 'lerinin Azure hesabınızda oturum açma şeklini değiştirebilirsiniz.
Hesabınızda hem **Import-azubir yeniden yayımcıya** da **Add-AzureAccount** ' a ait bir yönetim sertifikası varsa, Azure PowerShell cmdlet 'leri yalnızca erişim belirtecini kullanır; yönetim sertifikasını yoksayar.
Yönetim sertifikasını kullanmak için, **Remove-AzureAccount** ' ı kullanın.
**Remove-AzureAccount** hem yönetim sertifikasını hem de bir erişim belirtecini bulduğunda, hesabı silmek yerine yalnızca erişim belirtecini siler.
Yönetim sertifikası hala orada olduğundan hesap yine Windows PowerShell için kullanılabilir.

Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

## ÖRNEKLERDEN

### Örnek 1: hesap kaldırma
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

Bu komut, admin@contoso.com abonelik veri dosyanızı kaldırır.
Komut tamamlandığında, hesap artık Windows PowerShell tarafından kullanılamaz.

## PARAMETRELERINE

### -Force
Onay istemini bastırır.
Varsayılan olarak, **Remove-AzureAccount** , hesabı Windows PowerShell 'den kaldırmadan önce sorar.

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
Kaldırılacak hesabın adını belirtir.
Parametre değeri büyük/küçük harfe duyarlıdır.
Joker karakterler desteklenmez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Komut başarılı olduysa $True ve başarısız olursa $False döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış döndürmez.

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

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir. Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.

## ÇıKıŞLAR

### None veya System. Boolean
*Passin* parametresini kullanıyorsanız, bu cmdlet bir Boole değeri döndürür.
Aksi takdirde hiçbir çıkış döndürmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


