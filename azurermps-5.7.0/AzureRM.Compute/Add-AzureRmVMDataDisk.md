---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588987"
---
# Add-AzureRmVMDataDisk

## SYNOPSIS
Sanal makineye veri diski ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## Tanım
**Add-Azurermvmdatadısk** cmdlet 'i, bir sanal makineye veri diski ekler.
Bir sanal makine oluşturduğunuzda veri diski ekleyebilirsiniz veya varolan bir sanal makineye veri diski ekleyebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: yeni bir sanal makineye veri diskleri ekleme
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.
Bu komut sanal makineye bir ad ve boyut atar.

Sonraki üç komut, $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03 değişkenlerine üç veri disklerinin yollarını atar.
Bu yaklaşım yalnızca aşağıdaki komutların okunurluğu için kullanılır.

Her biri $VirtualMachine depolanan sanal makineye bir veri diski ekler.
Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.
Her diskin URI 'SI $DataDiskVhdUri 01, $DataDiskVhdUri 02 ve $DataDiskVhdUri 03.

### Örnek 2: var olan bir sanal makineye veri diski ekleme
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

İlk komut VirtualMachine07 adındaki sanal makineyi [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet 'ini kullanarak alır.
Komut, $VirtualMachine değişkeninde sanal makineyi depolar.

İkinci komut $VirtualMachine depolanan sanal makineye bir veri diski ekler.

Son komutu, ResourceGroup11 'da $VirtualMachine depolanan sanal makinenin durumunu güncelleştirir.

### Örnek 3: genelleştirilmiş bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diski ekleme
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.
Bu komut sanal makineye bir ad ve boyut atar.

Sonraki iki komut, veri görüntüsü ve veri disklerinin yollarını sırasıyla $DataImageUri ve $DataDiskUri değişkenlerine atar.
Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.

Son komutlar $VirtualMachine depolanan sanal makineye bir veri diski ekler.
Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.

### Örnek 4: özel bir Kullanıcı görüntüsünden yeni bir sanal makineye veri diskleri ekleme
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.
Bu komut sanal makineye bir ad ve boyut atar.

Sonraki komutlar veri diskinin yollarını $DataDiskUri değişkenine atar.
Bu yaklaşım, aşağıdaki komutların okunabilirliğini geliştirmek için kullanılır.

Son komutu $VirtualMachine depolanan sanal makineye bir veri diski ekler.
Komut, diskin adını ve konumunu ve diskin diğer özelliklerini belirtir.

## PARAMETRELERINE

### -Önbelleğe alma
Diskin önbelleğe alma modunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Özelliğinin
- Yazma
- Yabilirsiniz

Varsayılan değer ReadWrite değeridir.
Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.

Bu ayar, diskin tutarlılığını ve performansını etkiler.

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
Bu cmdlet 'in sanal makinede bir platform veya Kullanıcı görüntüsünden disk oluşturup oluşturmayacağını belirtir, boş bir disk oluşturur veya var olan bir diski iliştirir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Nota.
Özel bir diskten sanal makine oluşturmak için bu seçeneği belirtin.
Bu seçeneği belirttiğinizde *Sourceımageuri* parametresini belirtmeyin.
Bu *, Azure* platformuna sanal sabit diskin (VHD) sanal sabit diskinin (VHD), sanal makineye veri diski olarak iliştirileceği yeri bildirmek için gereklidir.
- Boşaltma.
Boş bir veri disketi oluşturmak için bunu belirtin.
- FromImage.
Genelleştirilmiş bir yansıma veya diskten sanal makine oluşturmak için bu seçeneği belirtin.
Bu seçeneği belirttiğinizde, Azure platformuna veri diski olarak eklenecek VHD 'nin konumunu belirtmek için *Sourceımageuri* parametresini de belirtmeniz gerekir.
*Vhduri* parametresi, sanal makine tarafından kullanıldığında VERI diski VHD 'nin depolanacağı konumu tanımlayan konum olarak kullanılır.

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Sanal makineye eklenecek boş bir diskin boyutunu gigabayt cinsinden belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LUN
Veri diskinin mantıksal birim numarasını (LUN) belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Manageddiskıd
Yönetilen bir diskin KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Eklenecek veri diskinin adını belirtir.

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

### -Sourceımageuri
Bu cmdlet 'in ilişolduğu diskin Kaynak URI 'sini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Yönetilen diskin depolama hesabı türünü belirtir.

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
Bir platform görüntüsü veya Kullanıcı görüntüsü kullanıldığında oluşturulacak sanal sabit disk (VHD) dosyasının Tekdüzen Kaynak tanımlayıcısını (VHD) belirtir.
Bu cmdlet, resim ikili büyük nesnesini (blob) bu konuma kopyalar.
Bu, sanal makinenin başlayacağı konumdur.

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

### -VM
Veri diskinin ekleneceği yerel sanal makine nesnesini belirtir.
Sanal makine nesnesi edinmek için **Get-AzureRmVM** cmdlet 'ini kullanabilirsiniz.
Sanal makine nesnesi oluşturmak için **New-AzureRmVMConfig** cmdlet 'ini kullanabilirsiniz.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureRmVMDataDisk](./Remove-AzureRmVMDataDisk.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Yeni-AzureRmVMConfig](./New-AzureRmVMConfig.md)
