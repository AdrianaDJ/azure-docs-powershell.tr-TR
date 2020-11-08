---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105676"
---
# Get-AzureAccount

## SYNOPSIS
Azure PowerShell tarafından sağlanan Azure hesaplarını alır.

## INDEKI

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureAccount** cmdlet 'ı Windows PowerShell tarafından sağlanan Azure hesaplarını alır.
Hesaplarınızı Windows PowerShell 'in kullanımına sunmak için **Add-AzureAccount** veya **Import-publishsettingsfıle** cmdlet 'lerini kullanın.

## ÖRNEKLERDEN

### Örnek 1: tüm hesapları alma
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

Bu komut belirtilen kullanıcıyla ilişkili tüm hesapları alır.

### Örnek 2: ada göre bir hesap alma
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

Bu komut, ContosoAdmin hesabını alır.

## PARAMETRELERINE

### -Ad
Yalnızca belirtilen hesabı alır.
Varsayılan, Windows PowerShell 'in kullanabildiği tüm hesaplardır.
Hesap adını girin.
**Ad** büyük/küçük harfe duyarlıdır.
Joker karakterlere izin verilmez.

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

### Yabilirsiniz
Bu cmdlet 'e giriş kanalı oluşturamazsınız.

## ÇıKıŞLAR

### Yabilirsiniz
Bu cmdlet hiçbir çıkış döndürmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-Azuikinci dosyayı](./Get-AzurePublishSettingsFile.md)

[Import-Azuyeniden yayımlayan ayarları dosyası](./Import-AzurePublishSettingsFile.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


