---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105828"
---
# Set-AzureOSDisk

## SYNOPSIS
Azure sanal makinesinin ana bilgisayar önbelleği modunu değiştirir.

## INDEKI

### NoResize
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Yeniden boyutlandırma
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Tanım
**Set-AzureOSDisk** cmdlet 'i Azure sanal makinesindeki işletim sistemi diskinin ana bilgisayar önbelleği modunu değiştirir.
Desteklenen ana bilgisayar önbelleği modları ReadOnly ve ReadWrite.
Bu cmdlet 'i çalışan bir sanal makinede çalıştırırsanız, bu sanal makine yeniden başlatılır.

## ÖRNEKLERDEN

### Örnek 1: ardışık düzeni kullanarak ana bilgisayar önbellek modunu ReadOnly olarak ayarlama
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak contososervice adındaki hizmette VirtualMachine02 adındaki sanal makineyi alır.
Komut, ardışık düzen işlecini kullanarak sanal makineyi geçerli cmdlet 'e geçirir.
Geçerli cmdlet, bu sanal makinenin işletim sistemi diskinin ana bilgisayar önbelleği modunu ReadOnly olarak ayarlar.

### Örnek 2: Ana bilgisayar önbellek modunu ReadWrite olarak ayarlama
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

İlk komut, VirtualMachine02 adındaki sanal makineyi ContosoService adındaki hizmette alır ve değişkende depolar.

İkinci komut, bu sanal makinenin işletim sistemi diskinin ana bilgisayar önbelleği modunu ReadWrite olarak ayarlar.

## PARAMETRELERINE

### -HostCaching
İşletim sistemi diskinin ana bilgisayar önbelleği özniteliğini belirtir.
Geçerli değerler: 

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
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
İşletim sistemi diski için, gigabayt cinsinden yeni bir boyut belirtir.
Boyut geçerli boyuttan büyük olmalıdır.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Bu cmdlet 'in işletim sistemi diskini değiştirdiği sanal makineyi belirtir.
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

[Add-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureOSDisk](./Get-AzureOSDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Güncelleştirme-AzureVM](./Update-AzureVM.md)


