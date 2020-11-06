---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: 8f3aebe1e9e79423d7251fa79084d6fa85407b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594116"
---
# Save-AzureRmVMImage

## SYNOPSIS
Sanal makineyi Vmımage olarak kaydeder.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ResourceGroupNameParameterSetName (varsayılan)
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [<CommonParameters>]
```

### Idparametersetname
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [<CommonParameters>]
```

## Tanım
**Save-Azurermvmımage** cmdlet 'i bir sanal makineyi bir vmımage olarak kaydeder.
Sanal makine yansıması oluşturmadan önce, sanal makine Sysprep 'i, ardından Set-AzureRmVM cmdlet 'ini kullanarak Genelleştirilmiş olarak işaretleyin.

Bu cmdlet 'in çıktısı JavaScript nesne gösterimi (JSON) şablonudur.
Yakalanan telefonunuzdan sanal makineler dağıtabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: sanal makine yakalama
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

İlk komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.

İkinci komut, Vmımage olarak VirtualMachine07 adındaki sanal makineyi yakalar.
**Output** ÖZELLIĞI bir JSON şablonu döndürür.

## PARAMETRELERINE

### -DestinationContainerName
"Sistem" kapsayıcısı içinde resimlerinizi tutmak istediğiniz kapsayıcının adını belirtir.

Konteyner yoksa, sizin için oluşturulur.
Vmımage 'ı oluşturan sanal sabit diskler (VHD) Bu parametrenin belirttiği kapsayıcıda bulunur.
VHD 'ler birden çok depolama hesabına yayılmışsa, bu cmdlet her depolama hesabında bu ada sahip bir kapsayıcı oluşturur.
Kaydedilen görüntünün URL 'SI şuna benzer: 

https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Sanal makinenin kaynak KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Bu cmdlet 'in hedef kapsayıcıda aynı öneke sahip olan tüm VHD 'Lerin üzerine yazabileceğini gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
VHD 'nin yolunu belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VHDNamePrefix
Vmımage 'ın depolama profilini oluşturan blobın adındaki öneki belirtir.

Örneğin, işletim sistemi diskinin önek Vhdi öneki, ad Vhdönek-OSDisk ile sonuçlanır. \<guid\> . sahip.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

[Get-Azurermvmımage](./Get-AzureRmVMImage.md)

[Get-Azurermvmımageteklifini](./Get-AzureRmVMImageOffer.md)

[Get-Azurermvmımagepublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Set-AzureRmVM](./Set-AzureRmVM.md)


