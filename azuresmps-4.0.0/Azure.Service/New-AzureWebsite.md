---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f83489d21fba97bb50145de1fedc1ac9a7195a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106184"
---
# New-AzureWebsite

## SYNOPSIS
Azure 'da çalıştırmak için yeni bir Web sitesi oluşturun.

## INDEKI

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GithubCredentials <PSCredential>] [-GithubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

Cmdlet, Azure 'da çalıştırmak için yeni bir Web sitesi oluşturur ve GitHub aracılığıyla dağıtıma hazırlar.

## ÖRNEKLERDEN

### Örnek 1: git ile yeni bir Web sitesi oluşturma
```
PS C:\> New-AzureWebsite mySite -Git
```

Bu örnek, Azure 'da yeni bir Web sitesi ve dosyaları yeni Web sitesine dağıtmak için yerel bir git deposu oluşturur.

### Örnek 2: GitHub ile tümleştirilmiş Web sitesi oluşturma
```
PS C:\> New-AzureWebsite mysite -Github -GithubRepository myaccount/myrepo
```

Bu örnek, myaccount/myrepo adlı GitHub havuzuna bağlı yeni bir Web sitesi oluşturur.
GitHub deposundaki işlemeler Azure 'daki Web sitesine gönderilir.

## PARAMETRELERINE

### -Git
Yerel bir git deposu kurar ve Web sitesine bağlar.
Belirtilmişse, bu parametre yerel dizinde bir git deposu ayarlar ve Azure 'daki Web sitesine bağlayan ' Azure ' adlı uzak bir depo ekler.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHub
Bu cmdlet 'in yeni Web sitesini varolan bir GitHub deposuna göndereceğini gösterir.
Gıuthub havuzuna yapılan işlemeler, Azure 'daki Web sitesine gönderilir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GithubCredentials
GitHub 'ya bağlanmak için Kullanıcı adı ve parola kimlik bilgilerini belirtir.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GithubRepository
Bu Web sitesine bağlanacak GitHub deposunun tam adını belirtir.
Örneğin, `myaccount/myrepo` .

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

### -Ana bilgisayar adı
Yeni Web sitesi için alternatif bir ana bilgisayar adı belirtir.

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

### -Konum
Web sitesini dağıtmak istediğiniz veri merkezinin konumunu belirtir.

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

### -Ad
Web sitesi için bir ad belirtir.

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

### -Publishingkullanıcıadı
Git dağıtımının Azure portalında belirttiğiniz kullanıcı adını belirtir.

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

### Yuvalı
Web sitesi için bir yuva adı belirtir.

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

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Set-AzureWebsite](./Set-AzureWebsite.md)


