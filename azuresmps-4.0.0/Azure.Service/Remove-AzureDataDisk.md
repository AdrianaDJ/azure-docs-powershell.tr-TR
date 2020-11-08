---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106166"
---
# Remove-AzureDataDisk

## SYNOPSIS
Azure sanal makinesinden veri diskini kaldırır.

## INDEKI

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Remove-AzureDataDisk** cmdlet 'i Azure sanal makinesinden veri diskini kaldırır.
Varsayılan olarak, bu cmdlet veri diski blob 'unu depolama hesabından kaldırmaz.

## ÖRNEKLERDEN

### Örnek 1: veri diskini kaldırma
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette VirtualMachine07 adındaki sanal makineyi alır.
Komut, ardışık düzen işlecini kullanarak sanal makineyi geçerli cmdlet 'e geçirir.
Geçerli cmdlet, LUN 0 olan veri diskini kaldırır.

### Örnek 2: veri diskini ve sanal sabit disk dosyasını kaldırma
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

Bu komut, VirtualMachine07 adındaki sanal makineyi ContosoService adındaki hizmette alır.
Komut sanal makineyi geçerli cmdlet 'e geçirir.
Geçerli cmdlet, LUN 0 olan veri diskini kaldırır.
Komut, *Deletevhd* parametresini içerir.
Bu nedenle temel sanal sabit disk de silinir.
Bu komut, **Update-AzureVM** cmdlet 'ini kullanarak değişikliklerinizi yansıtmak için sanal makineyi güncelleştirir.

## PARAMETRELERINE

### -DeleteVHD
Bu cmdlet 'in veri diskini ve sanal sabit diski (VHD) blob depolamadan kaldırmadığını gösterir.

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

### -LUN
Sanal makinedeki veri sürücüsünün mantıksal birim numarasını (LUN) belirtir.
Geçerli değerler: 0 ile 15 arası.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### -VM
Veri diskine eklenmiş olan sanal makine nesnesini belirtir.
Sanal makine nesnesi edinmek için **Get-AzureVM** cmdlet 'ini kullanın.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Güncelleştirme-AzureVM](./Update-AzureVM.md)


