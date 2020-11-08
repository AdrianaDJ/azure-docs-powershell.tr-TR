---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105735"
---
# Add-AzureDataDisk

## SYNOPSIS
Sanal makineye veri diski ekler.

## INDEKI

### CreateNew (varsayılan)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Aktarılacağı
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### Importfrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Add-AzureDataDisk** cmdlet 'ı bir Azure sanal makine nesnesine yeni veya varolan bir veri diski ekler.
Belirtilen boyutta ve etikete sahip yeni bir veri disketi oluşturmak için *CreateNew* parametresini kullanın.
Görüntü deposundan var olan bir diski eklemek için *Içeri aktarma* parametresini kullanın.
Depolama hesabındaki bir blob 'dan var olan bir diski eklemek için *ımportfrom* parametresini kullanın.
Ekli veri diskinin ana bilgisayar önbelleği modunu belirtebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: depodan veri diski Içeri aktarma
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

Bu komut, VirtualMachine07 adlı sanal makine için, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice bulut hizmetinde bir sanal makine nesnesi alır.
Komut, ardışık düzen işlecini kullanarak bunu geçerli cmdlet 'e geçirir.
Bu komut, depodan varolan bir veri diskini sanal makineye iliştirir.
Veri diskinin LUN 'U 0 ' dır.
Bu komut, **Update-AzureVM** cmdlet 'ini kullanarak değişikliklerinizi yansıtmak için sanal makineyi güncelleştirir.

### Örnek 2: yeni veri disketi ekleme
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Bu komut, VirtualMachine08 adındaki sanal makine için bir sanal makine nesnesi alır.
Komut bunu geçerli cmdlet 'e geçirir.
Bu komut, MyNewDisk. vhd adlı yeni bir veri diskine iliştirir.
Cmdlet, diski geçerli aboneliğin varsayılan depolama hesabında VHD kapsayıcısında oluşturur.
Komut, sanal makineyi değişikliklerinizi yansıtacak şekilde güncelleştirir.

### Örnek 3: belirtilen konumdan veri diski ekleme
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Bu komut, veritabanı adlı sanal makine için bir sanal makine nesnesi alır.
Komut bunu geçerli cmdlet 'e geçirir.
Bu komut, Disk14. vhd adlı varolan bir veri disketini belirtilen konumdan iliştirir.
Komut, sanal makineyi değişikliklerinizi yansıtacak şekilde güncelleştirir.

## PARAMETRELERINE

### -CreateNew
Bu cmdlet 'in veri disketi oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
Yeni veri diskinin disk etiketini belirtir.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskName
Disk deposundaki bir veri diskinin adını belirtir.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Yeni bir veri diskinin mantıksal disk boyutunu gigabayt cinsinden belirtir.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Diskin ana bilgisayar düzeyi önbelleğe alma ayarlarını belirtir.
Geçerli değerler: 

- Yabilirsiniz 
- Özelliğinin 
- Yazma

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Import
Bu cmdlet 'in görüntü deposundan var olan bir veri diskini aldığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Importfrom
Bu cmdlet 'in depolama hesabındaki bir blob 'dan var olan veri diskini aldığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
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
Sanal makinedeki veri sürücüsünün mantıksal birim numarasını (LUN) belirtir.
Geçerli değerler: 0 ile 15 arası.
Her veri diskinin benzersiz bir LUN 'U olmalıdır.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Bu cmdlet 'in veri diskini sakladığı bir Azure depolama hesabında blob 'un konumunu belirtir.
Konum belirtmezseniz cmdlet, veri diskini geçerli aboneliğin varsayılan depolama hesabında VHD kapsayıcısında depolar.
VHD kapsayıcısı yoksa, cmdlet bir VHD kapsayıcısı oluşturur.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
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

### -VM
Bu cmdlet 'in veri diskine ilişolduğu sanal makine nesnesini belirtir.
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

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Güncelleştirme-AzureVM](./Update-AzureVM.md)


