---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105884"
---
# Publish-AzureRemoteAppProgram

## SYNOPSIS
Bir Azure RemoteApp programı yayımlar.

## INDEKI

### Uygulama kimliği (varsayılan)
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Uygulama yolu
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Publish-AzureRemoteAppProgram** cmdlet 'ı, Azure RemoteApp koleksiyonunun kullanıcılarına uygun kılan bir Azure RemoteApp programı yayımlar.

## ÖRNEKLERDEN

### Örnek 1: bir program derleme içinde Yayınlanın
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

Bu komut, programı Başlat menüsüne eklemek için belirtilen *Startmenuappıd* Ile contosoapps koleksiyonunda yayımlar.
Yayınlanan uygulama "Finans uygulaması" görünen adına sahip olacaktır.

## PARAMETRELERINE

### -CollectionName
Azure RemoteApp koleksiyonunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CommandLine
Bu cmdlet 'in yayımladığı programın komut satırı bağımsız değişkenlerini belirtir.

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

### -DisplayName
Azure RemoteApp programının kullanımı kolay görünen adını belirtir.
Kullanıcılar bunu uygulamanın adı olarak görür.

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

### -FileVirtualPath
Programın şablon görüntüsü içindeki programın yolunu belirtir.

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
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

### -Startmenuappıd
Programı Başlat menüsüne eklemek için bu cmdlet 'in kullandığı GUID 'YI belirtir.

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
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

[Get-AzureRemoteAppProgram](./Get-AzureRemoteAppProgram.md)

[Yayımdan kaldırma-AzureRemoteAppProgram](./Unpublish-AzureRemoteAppProgram.md)


