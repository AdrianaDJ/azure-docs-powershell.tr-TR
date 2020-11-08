---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109792"
---
# Save-AzVMImage

## SYNOPSIS
Sanal makineyi Vmımage olarak kaydeder.

## INDEKI

### ResourceGroupNameParameterSetName (varsayılan)
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Idparametersetname
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Save-AzVMImage** cmdlet 'i bir sanal makineyi vmımage olarak kaydeder.
Sanal makine yansıması oluşturmadan önce, sanal makine Sysprep 'i, ardından Set-AzVM cmdlet 'ini kullanarak Genelleştirilmiş olarak işaretleyin.
Bu cmdlet 'in çıktısı JavaScript nesne gösterimi (JSON) şablonudur.
Yakalanan telefonunuzdan sanal makineler dağıtabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: sanal makine yakalama
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

İlk komut VirtualMachine07 adındaki sanal makineyi genelleþtirilmiþ olarak işaretler.
İkinci komut, Vmımage olarak VirtualMachine07 adındaki sanal makineyi yakalar.
**Output** ÖZELLIĞI bir JSON şablonu döndürür.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationContainerName
"Sistem" kapsayıcısı içinde resimlerinizi tutmak istediğiniz kapsayıcının adını belirtir.
Konteyner yoksa, sizin için oluşturulur.
Vmımage 'ı oluşturan sanal sabit diskler (VHD) Bu parametrenin belirttiği kapsayıcıda bulunur.
VHD 'ler birden çok depolama hesabına yayılmışsa, bu cmdlet her depolama hesabında bu ada sahip bir kapsayıcı oluşturur.
Kaydedilen görüntünün URL 'si: https:// \<storageAccountName\> . blob.Core.Windows.NET/System/Microsoft.COMPUTE/Images/ \<imagesContainer\> / \<vhdPrefix-osDisk\> . xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx. vhd.

```yaml
Type: System.String
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
Type: System.String
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
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
Yakalanan resmin şablonunun depolandığı dosya yolu.

```yaml
Type: System.String
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
Type: System.String
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
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. PSComputeLongRunningOperation

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-Azvmımageteklifini](./Get-AzVMImageOffer.md)

[Get-Azvmımagepublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Set-AzVM](./Set-AzVM.md)


