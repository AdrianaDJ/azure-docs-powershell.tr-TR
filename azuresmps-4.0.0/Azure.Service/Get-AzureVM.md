---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106547"
---
# Get-AzureVM

## SYNOPSIS
Bir veya daha fazla Azure sanal makinelerinden bilgi alır.

## INDEKI

### ListAllVMs (varsayılan)
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### GetVMByServiceAndVMName
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**Get-AzureVM** cmdlet 'i Azure 'da çalışan sanal makineler hakkında bilgi alır.
Belirli bir sanal makinede bilgi içeren bir nesne veya geçerli aboneliğin belirtilen hizmetindeki tüm sanal makineler için sanal makine belirtilmemişse bir nesne döndürür.

## ÖRNEKLERDEN

### Örnek 1: belirtilen sanal makinedeki bilgileri alma
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

Bu komut, ContosoService01 bulut hizmetinde çalışan VirtualMachine02 sanal makinesindeki bilgileri içeren bir nesne döndürür.

### Örnek 2: tüm sanal makinelerde bilgileri alma
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

Bu komut, ContosoService01 bulut hizmetinde çalışan tüm sanal makinelerde bilgi içeren bir liste nesnesi alır.

### Örnek 3: sanal makine durumlarının tablosunu görüntüleme
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

Bu komut, ContosoService01 hizmetinde çalışan sanal makinelerin, yükseltme etki alanının ve her sanal makinenin geçerli durumunun gösterildiği bir tablo görüntüler.

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

### -Ad
Bilgileri alacak sanal makinenin adını belirtir.
Bu parametre sağlanmadıysa cmdlet, belirtilen hizmette tüm sanal makinelerle ilgili bilgileri içeren bir liste nesnesi döndürür.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
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
Sanal makine bilgileri döndürülecek bulut hizmetinin adını belirtir.

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
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

[New-AzureVM](./New-AzureVM.md)

[New-AzureVMConfig](./New-AzureVMConfig.md)

[Remove-AzureVM](./Remove-AzureVM.md)

[Restart-AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)

[Stop-AzureVM](./Stop-AzureVM.md)

[Güncelleştirme-AzureVM](./Update-AzureVM.md)


