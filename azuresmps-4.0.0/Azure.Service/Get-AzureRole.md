---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106314"
---
# Get-AzureRole

## SYNOPSIS
Microsoft Azure hizmetinizden rollerin listesini döndürür.

## INDEKI

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRole** cmdlet 'ı, Microsoft Azure hizmetinizden rollerle ilgili ayrıntılar içeren bir liste nesnesi döndürür.
*RoleName* parametresini belirtirseniz **Get-AzureRole** yalnızca bu rolle ilgili ayrıntıları döndürür.
*Instancedetails* parametresini belirtirseniz, örneğe özgü ek ayrıntılar verilir.

## ÖRNEKLERDEN

### Örnek 1: hizmet rollerinin listesini alma
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

Bu komut, MySvc01 hizmetinde çalışan tüm üretim rollerinde ayrıntılı bir nesne döndürür.

### Örnek 2: hizmette çalışan bir role ilişkin ayrıntıları alma
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

Bu komut, MySvc01 hizmetinin hazırlama ortamında çalışan MyTestVM3 rolündeki ayrıntılar içeren bir nesne döndürür.

### Örnek 3: hizmette çalışan bir rolün örneklerine örnek bilgileri alma
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

Bu komut, MySvc01 hizmetindeki üretim ortamında çalışan MyTestVM02 rolünün örneklerinin ayrıntılarını içeren bir nesne döndürür.

### Örnek 4: hizmetle ilişkilendirilmiş rol örneklerinin tablosunu alma
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

Bu komut, MySvc01 hizmetindeki üretim ortamında çalışan tüm rol örneklerinin örnek adına, boyutuna ve durumuna döner.

## PARAMETRELERINE

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

### -Instancedetails
Bu cmdlet 'in her roldeki örneklerin ayrıntılarını döndürmeyeceğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -RoleName
Alınacak rolün adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HizmetAdı
Azure hizmetinin adını belirtir.

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
Azure dağıtım ortamını belirtir.
Bu parametre için kabul edilebilir değerler: Production veya basamaklandırma.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

[Set-AzureRole](./Set-AzureRole.md)


