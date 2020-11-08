---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105703"
---
# Clear-AzureRemoteAppVmStaleAdObject

## SYNOPSIS
Azure Active Directory 'de, artık varolmayan Azure RemoteApp sanal makinelerle ilişkili nesneleri kaldırır.

## INDEKI

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Clear-Azureremoteappvmetradobject** cmdlet 'ı, Azure Active Directory 'de artık varolmayan Azure RemoteApp sanal makinelerle ilişkili nesneleri kaldırır.
Azure Active Directory nesnelerini kaldırma hakkına sahip kimlik bilgilerini kullanmalısınız.
*Ayrıntılı* ortak parametreyi belirtirseniz, bu cmdlet sildiği her nesnenin adını görüntüler.

## ÖRNEKLERDEN

### Örnek 1: koleksiyon için eski nesneleri Temizleme
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

İlk komut, **Get-Credential** kullanarak bir Kullanıcı adı ve parola ister.
Komut sonuçları $AdminCredentials değişkeninde depolar.

İkinci komut contoso adlı koleksiyon için eski nesneleri temizler.
Komut $AdminCredentials değişkeninde depolanan kimlik bilgilerini kullanır.
Komutun başarılı olabilmesi için, bu kimlik bilgilerinin uygun haklara sahip olmaları gerekir.

## PARAMETRELERINE

### -CollectionName
Azure RemoteApp koleksiyonunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Bu eylemi gerçekleştirme hakkına sahip bir kimlik bilgisi belirtir.
**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.
Bu parametreyi belirtmezseniz, bu cmdlet geçerli kullanıcı kimlik bilgilerini kullanır.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

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

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azureremoteappvmeleadobject](./Get-AzureRemoteAppVmStaleAdObject.md)


