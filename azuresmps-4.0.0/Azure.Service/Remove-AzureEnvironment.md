---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106477"
---
# Remove-AzureEnvironment

## SYNOPSIS
Windows PowerShell 'den bir Azure ortamını siler.

## INDEKI

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Remove-AzureEnvironment** cmdlet 'i, gezici profilinizden bir Azure ortamı siler, böylece Windows PowerShell bunu bulamaz.
Bu cmdlet, Microsoft Azure 'dan ortamı silmez veya gerçek ortamı hiçbir şekilde değiştirmez.

Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.
Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.
Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

## ÖRNEKLERDEN

### Örnek 1: bir ortamı silme
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

Bu komut, Windows PowerShell 'den ContosoEnv ortamını siler.

### Örnek 2: birden çok ortamı silme
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

Bu komut, adları Windows PowerShell 'den "contoso" ile başlayan ortamları siler.

## PARAMETRELERINE

### -Force
Onay istemini bastırır.

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
Kaldırılacak ortamın adını belirtir.
Bu parametre gereklidir.
Bu parametre değeri büyük/küçük harfe duyarlıdır.
Joker karakterler kullanılamaz.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.

## ÇıKıŞLAR

### None veya System. Boolean
*Passin* parametresini kullanıyorsanız, bu cmdlet bir Boole değeri döndürür.
Aksi takdirde hiçbir çıkış döndürmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


