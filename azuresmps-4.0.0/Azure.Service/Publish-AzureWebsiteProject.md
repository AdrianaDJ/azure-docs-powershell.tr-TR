---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105877"
---
# Publish-AzureWebsiteProject

## SYNOPSIS
Visual Studio Web projesini WebDeploy kullanarak bir Microsoft Azure Web sitesinde yayımlayın.

## INDEKI

### ProjectFile
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Paketini
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Visual Studio Web projesini WebDeploy kullanarak bir Microsoft Azure Web sitesinde yayımlayın.
Bir WebDeploy paketi alabilir ve doğrudan yayımlayabilir ya da Visual Studio Web projesi alabilir, projeyi oluşturabilir ve yayımlayabilirsiniz.
Ayrıca, yayımlama sırasında Web.config bağlantı dizelerini de değiştirebilir.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

"Debug" yapılandırması (yani Web.Debug.config) ile bir Visual Studio Web projesi geliştirin ve WebDeploy kullanarak bir Microsoft Azure Web sitesinde yayımlayın.

### Örnek 2
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

WebDeploy Package. zip dosyasını, WebDeploy kullanarak bir Microsoft Azure Web sitesine yayımlayın.

### Örnek 3
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

WebDeploy paketi klasörünü WebDeploy kullanarak Microsoft Azure Web sitesine yayımlayın.

### Örnek 4
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

Visual Studio Web projesi oluşturma, Web.config 'da "DefaultConnection" bağlantı dizesinin üzerine yazın ve WebDeploy kullanarak bir Microsoft Azure Web sitesine yayımlayın.

### Örnek 5
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

Visual Studio Web projesi oluşturma, Web.config 'da "DefaultConnection" bağlantı dizesinin üzerine yazın ve WebDeploy kullanarak bir Microsoft Azure Web sitesine yayımlayın.
-DefaultConnection 'ın Web.config ayrıştırarak eklediği dinamik bir parametre olduğuna dikkat edin.

## PARAMETRELERINE

### -Yapılandırma
Visual Studio Web uygulaması projesini oluşturmak için kullanılan yapılandırma.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConnectionString
Dağıtım için kullanılacak bağlantı dizeleri.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DoNotDelete
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
Web sitesi adı.

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

### -Package
Yayımlanacak Visual Studio Web uygulaması projesinin zip dosyasının WebDeploy Package klasörü.

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
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

### -ProjectFile
Yayımlanacak Visual Studio Web uygulaması projesi.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SetParametersFile
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAppData
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

### Yuvalı
Web sitesi yuva adı.

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

### -Belirteçler
```yaml
Type: String
Parameter Sets: Package
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

[Get-AzureWebsite](./Get-AzureWebsite.md)

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Set-AzureWebsite](./Set-AzureWebsite.md)


