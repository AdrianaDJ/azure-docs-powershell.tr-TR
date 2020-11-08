---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106066"
---
# Set-AzureDataDisk

## SYNOPSIS
Azure sanal makinesinde varolan bir veri diskinin ana bilgisayarını önbelleğe almasını değiştirir.

## INDEKI

### NoResize
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Yeniden boyutlandırma
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Tanım
**Set-AzureDataDisk** cmdlet 'ı, Azure sanal makinesindeki mevcut bir veri diskinin önbellek özniteliklerini değiştirir.
Hangi veri diskinin mantıksal birim numarasıyla (LUN) güncelleştirileceğini belirtin.

## ÖRNEKLERDEN

### Örnek 1: veri diskinin önbelleğe alınmasını değiştirme
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adlı hizmette çalışan sanal makineleri alır.
Komut, ardışık düzen işlecini kullanarak bunları geçerli cmdlet 'e geçirir.
Bu cmdlet, VirtualMachine07 adındaki sanal makinenin LUN 2 ' deki veri diskini ReadOnly Host önbelleğe almayı kullanacak şekilde ayarlar.
Bu komut, **Update-AzureVM** cmdlet 'ini kullanarak değişikliklerinizi yansıtmak için sanal makineyi güncelleştirir.

### Örnek 2: sanal makinedeki tüm veri disklerinin ana bilgisayar önbelleğini değiştirme
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

Bu komut, ContosoService bulut hizmetinde VirtualMachine07 adındaki sanal makine için bir nesne alır.
Komut bu sanal makinenin veri disklerini alan **Get-AzureDataDisk** cmdlet 'ine geçirir.
Geçerli cmdlet, her veri disklerinin ana bilgisayar önbellekleme modunu ReadWrite olarak ayarlar.
Komut, sanal makineyi değişikliklerinizi yansıtacak şekilde güncelleştirir.

## PARAMETRELERINE

### -DiskName
Bu cmdlet 'in değiştirdiği veri diski yapılandırmasının adını belirtir.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> Disk önbelleğe alma, diskler 4 ve üstü için desteklenmez. VM 'inize birden çok disk eklenirse, 4 ' ten küçük olan her disk önbelleğe almayı destekler.
>
> Bir Azure diskinin önbellek ayarını değiştirmek, hedef diski ayırır ve yeniden iliştirir. İşletim sistemi diski ise VM yeniden başlatılır. Disk önbelleği ayarını değiştirmeden önce bu durdurmadan etkilenebilecek tüm uygulamaları/hizmetleri durdurun. Bu önerilerin olmaması verilerin bozulmasına yol açabilir.

Diskin ana bilgisayar düzeyi önbelleğe alma ayarlarını belirtir.
Geçerli değerler:

- Yabilirsiniz
- Özelliğinin
- Yazma

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
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
Sanal makinedeki veri sürücüsünün LUN öğesini belirtir.
Geçerli değerler: 0 ile 15 arası.

```yaml
Type: Int32
Parameter Sets: NoResize
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

### -ResizedSizeInGB
Veri diskinin yeni boyutunu gigabayt cinsinden belirtir.
Yeni boyut geçerli boyuttan büyük olmalıdır.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
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

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Güncelleştirme-AzureVM](./Update-AzureVM.md)


