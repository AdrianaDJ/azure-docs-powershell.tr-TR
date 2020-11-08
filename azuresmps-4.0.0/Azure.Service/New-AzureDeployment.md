---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105929"
---
# New-AzureDeployment

## SYNOPSIS
Bir hizmetten dağıtım oluşturur.

## INDEKI

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**New-AzureDeployment** cmdlet 'i, Web rollerini ve çalışan rollerini içeren hizmetten bir Azure dağıtımı oluşturur.
Bu cmdlet, paket dosyasına (. cspkg) ve hizmet yapılandırma dosyasına (. cscfg) dayalı bir dağıtım oluşturur.
Dağıtım ortamında benzersiz bir ad belirtin.

Azure sanal makinelerine dayalı bir dağıtım oluşturmak için **New-AzureVM** cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: dağıtım oluşturma
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

Bu komut, ContosoPackage. cspkg adındaki paketi ve ContosoConfiguration. cscfg adlı bir yapılandırmayı temel alan bir üretim dağıtımı oluşturur.
Komut, dağıtımın etiketini belirtir.
Bir ad belirtmez.
Bu cmdlet ad olarak bir GUID oluşturur.

### Örnek 2: bir uzantı yapılandırmasına dayalı dağıtım oluşturma
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

Bu komut, pakete ve yapılandırmaya dayalı bir üretim dağıtımı oluşturur.
Komut, ContosoExtensionConfig. cscfg adlı bir uzantı yapılandırması belirtir.
Bu cmdlet ad ve etiket olarak GUID 'Ler oluşturur.

## PARAMETRELERINE

### -Yapılandırma
Hizmet yapılandırma dosyasının tam yolunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DoNotStart
Bu cmdlet 'in dağıtımı başlatmeyeceğini belirtir.

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

### -ExtensionConfiguration
Uzantı yapılandırma nesneleri dizisini belirtir.

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### Etiketli
Dağıtım için bir etiket adı belirtir.
Etiket belirtmezseniz, bu cmdlet bir GUID kullanır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Dağıtım adını belirtir.
Bir ad belirtmezseniz, bu cmdlet bir GUID kullanır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package
Aynı aboneliğe veya projeye sahip depolama alanındaki bir. cspkg dosyasının yolunu veya URI 'sini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -HizmetAdı
Dağıtım için Azure hizmetinin adını belirtir.

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

### Yuvalı
Bu cmdlet 'in dağıtımı oluşturduğu ortamı belirtir.
Geçerli değerler: hazırlama ve üretim.
Varsayılan değer Production değeridir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TreatWarningsAsError
Uyarı iletilerinin hata olduğunu belirtir.
Bu parametreyi belirtirseniz, dağıtımın başarısız olmasına neden olan bir uyarı iletisi.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Taşı-AzureDeployment](./Move-AzureDeployment.md)

[New-AzureVM](./New-AzureVM.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Set-AzureDeployment](./Set-AzureDeployment.md)


