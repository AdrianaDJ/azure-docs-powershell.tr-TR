---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105883"
---
# Publish-AzureServiceProject

## SYNOPSIS
Geçerli hizmeti Windows Azure 'a yayımlayın.

## INDEKI

### PublishFromServiceDefinition (varsayılan)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Publish-AzureServiceProject** cmdlet 'i geçerli hizmeti buluta yayımlar.
Komut satırında yayımlama yapılandırması ( **abonelik** , **storageAccountName** , **konum** , **yuva** ) veya **set-AzureServiceProject** cmdlet aracılığıyla yerel ayarlarda belirtebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: varsayılan değerlerle bir hizmet projesi yayımlama
```
PS C:\> Publish-AzureServiceProject
```

Bu örnek geçerli hizmeti, geçerli hizmet ayarlarını ve geçerli Azure yayımlama profilini kullanarak yayımlar.

### Örnek 2: dağıtım paketi oluşturma
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

Bu örnekte, hizmet dizininde dağıtım paketi (. cspkg) dosyası oluşturulur ve Windows Azure 'da yayınlanmaz.

## PARAMETRELERINE

### -AffinityGroup
Hizmetin kullanmasını istediğiniz benzeşim grubunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yapılandırma
Hizmet yapılandırma dosyasını belirtir.
Bu parametreyi belirtirseniz, *paket* parametresini belirtin.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentName
Dağıtım adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Başlat
Uygulamayı dağıtıldıktan sonra bir tarayıcı penceresi açar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Uygulamanın barındırıldığı bölge.
Olası değerler: 
  
- Her yerde Asya
- Her yerde
- Her yerde
- Doğu Asya
- Doğu ABD
- Kuzey Orta ABD
- Kuzey Avrupa
- Güney Orta ABD
- Güneydoğu Asya
- Batı Avrupa
- Batı ABD
 
Konum belirtilmezse, ayarlanacak son çağrıda belirtilen konum **-AzureServiceProject** kullanılır. Hiçbir konum belirtilmemişse, konum, ' Kuzey Merkezi ABD ' ve ' Güney Merkezi ' konumlarından rastgele seçilir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Package
Dağıtılacak paket dosyasını belirtir.
. Cspkg dosya adı uzantısına sahip yerel bir dosya veya paketi içeren bir blob URI 'SI belirtin.
Bu parametreyi belirtirseniz, *ServiceName* parametresini belirtmeyin.

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

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

### -HizmetAdı
Windows Azure 'a yayımlarken hizmet için kullanılacak adı belirtir.
Bu ad, Windows Azure 'da ( **ad**. cloudapp.net) barındırılan hizmeti adresleyip hizmeti adresleyebilir.
Hizmet yayımlandığında belirtilen ad, hizmet oluşturulduğunda verilen adı geçersiz kılar.
( **New-AzureServiceProject** cmdlet 'ine bakın).

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Yuvalı
Bu hizmet için kullanılacak dağıtım yuvası.
Olası değerler ' hazırlama ' ve ' üretim '.
Bir yuva belirtilmemişse, Set-AzureDeploymentSlot son çağrıda sağlanan yuva kullanılır.
Hiçbir yuva belirtilmemişse ' üretim ' yuvası kullanılır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Hizmet yayımlanırken kullanılacak Windows Azure depolama hesabı adını belirtir.
Bu değer, hizmet yayımlanana kadar kullanılmaz.
Bu parametre belirtilmediğinde, değer son **set-AzureServiceProject** komutundan alınır.
Hiçbir depolama hesabı belirtilmemişse, hizmetin adıyla eşleşen bir depolama hesabı kullanılır.
Böyle bir depolama hesabı yoksa cmdlet, yenisini oluşturmaya çalışır.
Ancak, başka bir abonelikte hizmet adıyla eşleşen bir depolama hesabı varsa, deneme başarısız olabilir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

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

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


