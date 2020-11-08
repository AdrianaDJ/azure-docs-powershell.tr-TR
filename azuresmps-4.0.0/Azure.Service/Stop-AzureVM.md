---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105741"
---
# Stop-AzureVM

## SYNOPSIS
Bir Azure sanal makinesini kapatır.

## INDEKI

### ByName (varsayılan)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Girdiden
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Tanım
**Stop-AzureVM** cmdlet 'i bir sanal makineyi kapatır.

## ÖRNEKLERDEN

### Örnek 1: sanal makineyi kapatma
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

Bu komut belirtilen hizmetin içerdiği bir sanal makineyi kapatır.

### Örnek 2: sanal makine nesnesini kullanarak sanal makineyi kapatma
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

Bu komut, **Get-AzureVM** döndüren sanal makine nesnesini kullanarak belirtilen hizmetin içerdiği bir sanal makineyi kapatır.

### Örnek 3: VM 'yi kapatma ve VM 'yi sağlandı
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

Bu komut belirtilen hizmetin içerdiği bir sanal makineyi kapatır ve bu hizmeti sağladı.

### Örnek 4: sanal makineyi kapatma ve dağıtımdaki son VM 'yi ayırmayı verme
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

Bu komut, belirtilen hizmetin içerdiği bir sanal makineyi kapatır ve dağıtımdaki son sanal makinenin yeniden oluşturulmasına olanak tanır.

### Örnek 5: birden çok VM 'yi kapatma
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

Bu komut, belirtilen hizmetin içerdiği birden çok sanal makineyi kapatır.

## PARAMETRELERINE

### -Force
Dağıtımdaki son sanal makinenin ayırmayı kaldırma izni verip vermeyeceğinizi belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
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

### -Ad
Kapatılacak sanal makinenin adını belirtir.

Birden çok sanal makineyi zaman uyumsuz olarak durdurmak için joker karakter kullanın.
Joker karakterle, bu cmdlet, kapatma https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) rolü işlemi yerine ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
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
Kapatılacak sanal makineyi içeren Azure hizmetinin adını belirtir.

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

### -Staysağlandı
Bu cmdlet 'in, sanal makinenin sağlandığını belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Kapatılacak sanal makineyi tanımlayan sanal makine nesnesini belirtir.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
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

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[Restart-AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)


