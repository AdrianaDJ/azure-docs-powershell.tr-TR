---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105537"
---
# Get-AzureSubscription

## SYNOPSIS
Azure hesabındaki Azure aboneliklerini alır.

## INDEKI

### ByName (varsayılan)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Byıd
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Varsayýlan
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Son
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-azuyeniden gönderme Scription** cmdlet 'i Azure hesabınızdaki abonelikleri alır.
Bu cmdlet 'i abonelik hakkında bilgi almak ve aboneliği diğer cmdlet 'lere boru yapmak için kullanabilirsiniz.

**Get-azuyeniden gönderme betikte** Azure hesaplarınıza erişim gerekir.
**Get-Azuyeniden gönderme komut** **dosyasına başlamadan** önce, **Add-AzureAccount** cmdlet 'Ini veya yayımlama ayarları dosyasını ( **Get-azuyeniden yayımdosyası**

Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

## ÖRNEKLERDEN

### Örnek 1: tüm abonelikleri al
```
C:\PS>Get-AzureSubscription
```

Bu komut, hesaptaki tüm abonelikleri alır.

### Örnek 2: ada göre abonelik alma
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

Bu komut yalnızca "MyProdSubsciption" aboneliğini alır.

### Örnek 3: varsayılan aboneliği edinin
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

Bu komut yalnızca varsayılan aboneliğin adını alır.
Komut öncelikle aboneliği alır ve ardından aboneliğin **subscriptionName** özelliğini almak için dot yöntemini kullanır.

### Örnek 4: seçili abonelik özelliklerini alma
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

Bu komut, geçerli aboneliğin adını ve sertifikasını içeren bir liste döndürür.
Geçerli aboneliği almak için **Get-Azuyeniden gönderme** komut dosyası kullanır.
Ardından, aboneliği listedeki seçili özellikleri görüntüleyen **Biçim listesi** komutuna yöneltin.

### Örnek 5: alternatif bir abonelik veri dosyası kullanın
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

Bu komut, C:\Temp\MySubscriptions.xml aboneliği veri dosyasından abonelikleri alır.
**Add-AzureAccount** veya **Import-publishsettingsfile** cmdlet 'lerini çalıştırdığınızda alternatif bir abonelik verileri dosyası belirttiyseniz, **subscriptionveri** dosyası parametresini kullanın.

## PARAMETRELERINE

### -Geçerli
Yalnızca geçerli aboneliği (yani, "geçerli" olarak belirlenen aboneliği) alır. Varsayılan olarak **Get-Azuyeniden gönderme komut** dosyası, Azure hesaplarınızda tüm abonelikleri alır.
Aboneliği "geçerli" olarak belirlemek için, **Select-azuyeniden gönderme scripscripts** cmdlet 'inin **geçerli** parametresini kullanın.

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Varsayılan
Yalnızca varsayılan aboneliği (yani, "varsayılan" olarak belirlenen aboneliği) alır. Varsayılan olarak **Get-Azuyeniden gönderme komut** dosyası, Azure hesaplarınızda tüm abonelikleri alır.
Aboneliği "varsayılan" olarak belirlemek için, **Select-azuyeniden gönderme scripscripts** cmdlet 'inin **varsayılan** parametresini kullanın.

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
Standart ayarlara ek olarak aboneliğin kota bilgilerini döndürür.

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

### -SubscriptionID
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Yalnızca belirtilen aboneliği alır.
Abonelik adını girin.
Değer büyük/küçük harfe duyarlıdır.
Joker karakterler desteklenmez.
Varsayılan olarak **Get-Azuyeniden gönderme komut** dosyası, Azure hesaplarınızda tüm abonelikleri alır.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Girişi, **subscriptionName** özelliğine göre değil, ad ile kanal olarak kullanabilirsiniz.

## ÇıKıŞLAR

### Microsoft. windowsazma. Commands. Utilities. Common. windowsazuyeniden gönderme komutları

## NOTLARıNDA
* Get-AzureSubscription, **Add-AzureAccount** ve **Import-publishsettingsfile** cmdlet 'lerinin oluşturulduğu abonelik verileri dosyasından verileri alır.

## ILGILI BAĞLANTıLAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-Azuikinci dosyayı](./Get-AzurePublishSettingsFile.md)

[Import-Azuyeniden yayımlayan ayarları dosyası](./Import-AzurePublishSettingsFile.md)

[Remove-Azuyeniden gönderiliyor](./Remove-AzureSubscription.md)

[Set-Azuyeniden gönderiliyor](./Set-AzureSubscription.md)


