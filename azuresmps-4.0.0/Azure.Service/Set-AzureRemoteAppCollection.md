---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106053"
---
# Set-AzureRemoteAppCollection

## SYNOPSIS
RemoteApp koleksiyonunun özelliklerini ayarlar.

## INDEKI

### Yalnızca Description(varsayılan)
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Yalnızca plan
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Etkialanıbirleştirilmiş
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Yalnızca rdpproperty
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Yalnızca acllevel
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Set-AzureRemoteAppCollection** cmdlet 'i, bir Azure RemoteApp koleksiyonunun özelliklerini ayarlar.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -AclLevel
Koleksiyonun erişim denetim listesi (ACL) düzeyini belirtir.
Bu parametre için kabul edilebilir değerler: koleksiyon ve uygulama.

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Credential
Azure RemoteApp sunucularına etki alanınıza katılma izni olan bir hizmet hesabının kimlik bilgilerini belirtir.
**PSCredential** nesnesi almak için **Get-Credential** cmdlet 'ini kullanın.

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Customrdpözelliği
Sürücü yeniden yönlendirmeyi ve diğer ayarları yapılandırmak için kullanılabilecek özel Uzak Masaüstü Protokolü (RDP) özelliklerini belirtir. Ayrıntılar için [Windows Server 'Daki Uzak Masaüstü Hizmetleri 'Ndeki RDP ayarlarına](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) bakın `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Açıklama
Koleksiyon için kısa bir açıklama belirtir.

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Plan
Kullanım sınırlarını tanımlayan Azure RemoteApp koleksiyonu planını belirtir.
Planları görmek için **Get-AzureRemoteAppPlan** 'ı kullanın.

```yaml
Type: String
Parameter Sets: PlanOnly
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRemoteAppCollection](./Get-AzureRemoteAppCollection.md)

[New-AzureRemoteAppCollection](./New-AzureRemoteAppCollection.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


