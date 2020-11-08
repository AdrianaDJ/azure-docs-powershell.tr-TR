---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105825"
---
# Set-AzureReservedIPAssociation

## SYNOPSIS
Ayrılmış bir IP adresini mevcut bir sanal makineyle veya bulut hizmetiyle ilişkilendirir.

## INDEKI

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Set-AzureReservedIPAssociation** cmdlet 'i, ayrılmış bir IP adresini çalışan bir sanal makinenin veya bulut HIZMETININ sanal IP ADRESIYLE (VIP) ilişkilendirir.
Ayrılmış IP adresi bu cmdlet 'in başlatılması sırasında kullanımda olmamalıdır ve sanal makine veya bulut hizmetiyle aynı bölgede olmalıdır.

İşlemin tamamlanması yaklaşık 30 saniye sürer ve bu da ayrılmış IP adresi kullanılarak sanal makine veya hizmetin erişilebilir olması gerekir.

## ÖRNEKLERDEN

### Örnek 1: ayrılmış IP ilişkilendirmesi ayarlama
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

Bu komut, ResIp14 adlı ayrılmış IP adresini hizmet PipTestWestEurope olarak atar.
ResIp14, Batı Avrupa bölgesinde ayrılmış bir IP.

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

### -Rezervedıpname
Sanal makine veya hizmetle ilişkilendirilecek ayrılmış IP adresinin adını belirtir.

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

### -HizmetAdı
Ayrılmış IP adresiyle ilişkilendirilecek dağıtımın bulunduğu hizmetin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Yuvalı
Dağıtım yuvasını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Geçici saklama
- Üretim

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualIPName
Ayrılmış bir IP ile ilişkilendirilecek mevcut bir VIP 'in adını belirtir.
Bulut hizmetinize VIP eklemek için Add-AzureVirtualIP bakın.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Windowsazme. Commands. Utilities. Common. ManagementOperationContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureReservedIPAssociation](./Remove-AzureReservedIPAssociation.md)


