---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106454"
---
# Remove-AzureVMImage

## SYNOPSIS
Görüntü deposundaki bir işletim sistemi yansımasını kaldırır.

## INDEKI

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Remove-AzureVMImage** cmdlet 'i, görüntü deposundaki bir işletim sistemi yansımasını kaldırır.
Varsayılan olarak, bu cmdlet, ilişkili fiziksel görüntü blob 'unu depolama hesabından silmez.
İlişkili sanal sabit sürücüyü (VHD) silmek için **Deletevhd** parametresini kullanın.

## ÖRNEKLERDEN

### Örnek 1: resim deposundaki bir resmi kaldırma
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

Bu komut, Image001 adındaki resmi görüntü deposundan kaldırır.

### Örnek 2: resim deposundaki bir resmi ve ayrıca VHD 'yi kaldırma
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

Bu komut, Image001 adındaki resmi görüntü deposundan kaldırır ve fiziksel VHD görüntüsünü depolama hesabından siler.

### Örnek 3: abonelik bağlamını ayarlayın ve tüm resimleri kaldırın
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

Bu komut, abonelik bağlamını ayarlar ve resim deposundaki, etiketine Beta adını içeren tüm resimleri kaldırır.

## PARAMETRELERINE

### -DeleteVHD
Bu cmdlet 'in depolama hesabından fiziksel VHD görüntü blob 'unu sildiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GörüntüAdı
Görüntü deposundan kaldırılacak işletim sistemini veya sanal makine yansımasını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Save-AzureVMImage](./Save-AzureVMImage.md)

[Güncelleştirme-AzureVMImage](./Update-AzureVMImage.md)


