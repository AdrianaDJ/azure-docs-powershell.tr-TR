---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4522E93F-6AC9-4A37-88B8-CCCCE15A5879
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcfc41e06f6847612c275817560e8593b76f6bac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105471"
---
# Reset-AzureRemoteAppVpnSharedKey

## SYNOPSIS
Azure RemoteApp VPN paylaşılan anahtarını sıfırlar.

## INDEKI

```
Reset-AzureRemoteAppVpnSharedKey [-VNetName] <String> [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Reset-AzureRemoteAppVpnSharedKey** cmdlet 'ı, Azure RemoteApp sanal özel ağ (VPN) paylaşılan anahtarını sıfırlar.

## ÖRNEKLERDEN

### Örnek 1: sanal ağdaki paylaşılan anahtarı sıfırlama
```
PS C:\> Reset-AzureRemoteAppVpnSharedKey -VNetName "ContosoVNet"
```

Bu komut, ContosoVNet adlı sanal ağdaki paylaşılan anahtarı sıfırlar.
VPN cihazında yeni paylaşılan anahtar yapılandırılmadığı sürece Şirket içi ağa VPN bağlantısı çevrimdışı kalır.
VPN aygıtını yapılandırmak için, VPN aygıtınızın doğru kodunu veya yapılandırma dosyasını almak üzere **Get-Azureremoteappvpndeviceconfigscrıpt** cmdlet 'ini kullanın, ardından bu komut dosyasını veya yapılandırma dosyasını VPN aygıtına yükleyin.

## PARAMETRELERINE

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

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
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

### System. String

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRemoteAppVNet](./Get-AzureRemoteAppVNet.md)

[Get-Azureremoteappvpndeviceconfigscrıpt](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


