---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105536"
---
# Get-AzureTrafficManagerProfile

## SYNOPSIS
Traffic Manager profilinin ayrıntılarını alır.

## INDEKI

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureTrafficManagerProfile** cmdlet 'ı Microsoft Azure Traffic Manager profilinin ayrıntılarını alır.
*Name* parametresini belirtmezseniz cmdlet, geçerli abonelikteki Traffic Manager profillerini listeler.

## ÖRNEKLERDEN

### Örnek 1: abonelikteki Traffic Manager profillerinin listesini alma
```
PS C:\>Get-AzureTrafficManagerProfile
```

Bu komut aboneliğinizdeki Traffic Manager profillerinin listesini alır.

### Örnek 2: Traffic Manager profili alma
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

Bu komut Myprofıle adlı Traffic Manager profilini alır.

### Örnek 3: Traffic Manager profiline uç nokta ekleme
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

Bu komut bir Traffic Manager profiline uç nokta ekler ve ardından profili kaydeder.

## PARAMETRELERINE

### -Ad
Alınacak Traffic Manager profilinin adını belirtir.

```yaml
Type: String
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition
Bu cmdlet, Traffic Manager profil nesnesi veya nesneleri oluşturur.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


