---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106274"
---
# Get-AzureWebsite

## SYNOPSIS
Geçerli abonelikteki Azure Web sitelerini alır.

## INDEKI

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureWebsite** cmdlet 'i geçerli abonelikteki Azure Web siteleri hakkında bilgi alır.

Varsayılan olarak **Get-AzureWebsite** , geçerli abonelikteki tüm Azure Web sitelerini alır ve siteler hakkında temel bilgiler sağlayan bir nesne döndürür.
*Name* parametresini kullandığınızda **Get-AzureWebsite** , yapılandırma ayrıntıları dahil kapsamlı bir bilgi içeren bir nesne döndürür.

Geçerli abonelik, "geçerli" olarak atanan aboneliğiniz. Geçerli aboneliği bulmak için [Get-Azuyeniden gönderme scripscripts](https://go.microsoft.com/fwlink/?LinkID=397623) cmdlet 'inin *Current* parametresini kullanın.
Geçerli aboneliği değiştirmek için, [Select-azuyeniden komut](https://go.microsoft.com/fwlink/?LinkID=397628) dosyası cmdlet 'ini kullanın.

Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

## ÖRNEKLERDEN

### Örnek 1: abonelikteki tüm Web sitelerini alma
```
PS C:\> Get-AzureWebsite
```

Bu komut geçerli abonelikteki tüm Azure Web sitelerini alır.

### Örnek 2: ada göre bir Web sitesi alma
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

Bu komut, yapılandırma bilgileri de içinde olmak üzere ContosoWeb Azure Web sitesi hakkında ayrıntılı bilgi alır.
*Name* parametresini kullandığınızda **Get-AzureWebsite** , Web sitesi hakkında genişletilmiş bilgilerin bulunduğu bir **sitewithconfig** nesnesi döndürür.

### Örnek 3: tüm Web siteleri hakkında ayrıntılı bilgi edinme
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

Bu komut, abonelikteki tüm Web siteleri hakkında ayrıntılı bilgi alır.
Tüm Web sitelerini almak için **Get-AzureWebsite** komutunu kullanır ve sonra her siteyi ada göre almak için **ForEach-Object** cmdlet 'ini kullanır.

### Örnek 4: dağıtım yuvası hakkında bilgi edinme
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

Bu komut, ContosoWeb sitesinin hazırlama dağıtım yuvasını alır.
Dağıtım yuvaları, Azure Web sitenizin farklı sürümlerini herkese bırakmadan test edebilirsiniz.

### Örnek 5: Web sitesi örneklerini alma
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

Bu örnekteki komutlar, çalışmakta olan Web sitesi örnekleri hakkında bilgi almak için bir Azure Web sitesinin örnekler özelliğini kullanır.
**Instances** özelliği, Azure modülünün sürüm 0.8.3 ' da **sitewithconfig** nesnesine eklenmiştir.

İlk komut, Web sitesinin şu anda çalışan tüm örneklerinin örnek kimliklerini alır.
İkinci komut, Web sitesinin çalışan örneklerinin sayısını alır.
**Count** özelliğini herhangi bir dizide kullanabilirsiniz.

## PARAMETRELERINE

### -Ad
Belirtilen Web sitesi hakkında ayrıntılı yapılandırma bilgilerini alır.
Abonelikteki bir Web sitesinin adını girin.
**Get-AzureWebsite** , varsayılan olarak geçerli abonelikteki tüm Web sitelerini alır.
*Ad* değeri joker karakterleri desteklemez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Yuvalı
Web sitesinin belirtilen dağıtım yuvasını alır.
"Hazırlama" veya "üretim" gibi yuva adını girin.
Dağıtım yuvaları hakkında daha fazla bilgi için Microsoft Azure Web sitelerinde aşamalı dağıtım konusuna bakın https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .
Var olan bir Azure Web sitesine dağıtım yuvası eklemek için Set-AzureWebsite cmdlet 'ini kullanın.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.

## ÇıKıŞLAR

### Microsoft. Windowsazve. Commands. Utilities. WebEntities. Services. WebEntities. site
**Get-AzureWebsite** , varsayılan olarak **site** nesnelerinin dizisini döndürür.

### Microsoft. Windowsazve. Commands. Utilities. WebEntities. Services. WebEntities. SiteWithConfig
*Name* parametresini kullandığınızda **Get-AzureWebsite** , bir **sitewithconfig** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)

[Stop-AzureWebsite](./Stop-AzureWebsite.md)

[Show-AzureWebsite](./Show-AzureWebsite.md)


