---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105630"
---
# Get-AzureRemoteAppVmStaleAdObject

## SYNOPSIS
Azure Active Directory 'de, artık varolmayan Azure RemoteApp sanal makinelerle ilişkili nesneleri alır.

## INDEKI

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-Azureremoteappvmetradobject** cmdlet 'ı Azure Active Directory 'de, artık varolmayan Azure RemoteApp sanal makinelerle ilişkili nesneleri alır.
Bu cmdlet, aldığı her nesnenin adını görüntüler.

## ÖRNEKLERDEN

### Örnek 1: koleksiyon için eski nesneleri alma
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

Bu ikinci komut contoso adlı koleksiyonun eski nesnelerini alır.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Dizisi

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Temizle-Azureremoteappvmeleadobject](./Clear-AzureRemoteAppVmStaleAdObject.md)


