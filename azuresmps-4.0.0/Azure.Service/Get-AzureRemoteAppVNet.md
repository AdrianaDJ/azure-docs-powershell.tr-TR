---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106570"
---
# Get-AzureRemoteAppVNet

## SYNOPSIS
Azure 'daki Azure RemoteApp sanal ağları hakkında bilgi getirir.

## INDEKI

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRemoteAppVNet** cmdlet 'ı, Microsoft Azure 'Daki Azure RemoteApp sanal ağları hakkında bilgi alır.
Bu cmdlet, belirtilen sanal ağ hakkında bilgi içeren bir nesne döndürür.
Sanal ağ belirtilmezse, bu cmdlet geçerli abonelikteki tüm sanal ağlarla ilgili bilgileri döndürür.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ hakkında bilgi alma
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

Bu komut, ContosoVNet adındaki sanal ağ hakkında bilgi alır.

## PARAMETRELERINE

### -Includesharedkey
Bu cmdlet 'in sanal ağ hakkında aldığı bilgilerde paylaşılan anahtar değerini içerdiğini gösterir.

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

### -Vağ adı
Azure RemoteApp sanal ağının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


