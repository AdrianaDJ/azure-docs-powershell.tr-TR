---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586814"
---
# Add-AzureRmVmssExtension

## SYNOPSIS
VMSUBNET 'e bir uzantı ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Add-Azurermvmssextenma** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir uzantı ekler.

## ÖRNEKLERDEN

### Örnek 1: VMSS 'ye uzantı ekleme
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

Bu komut VMMS 'ye bir uzantı ekler.

## PARAMETRELERINE

### -AutoUpgradeMinorVersion
Uzantı sürümünün otomatik olarak yeni bir alt sürüme güncelleştirilip güncelleştirilmeyeceğini belirtir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in eklediği uzantının adını belirtir.

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

### -ProtectedSetting
Uzantı için özel yapılandırmayı bir dize olarak belirtir.
Bu cmdlet özel yapılandırmayı şifreler.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
Uzantı yayıncısı adını belirtir.
Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.
Bu, yayımcıyı almak için [Get-Azurermvmımagepublisher](./Get-AzureRmVMImagePublisher.md) cmdlet 'ini kullanabilir.

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

### -Ayarlar
Uzantı için genel yapılandırmayı bir dize olarak belirtir.
Bu cmdlet ortak yapılandırmayı şifrelemez.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tür
Uzantı türünü belirtir.
Extension türünü almak için [Get-Azurermvmextensionımagetype](./Get-AzureRmVMExtensionImageType.md) cmdlet 'ini kullanabilirsiniz.

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

### -TypeHandlerVersion
Bu sanal makine için kullanılacak uzantının sürümünü belirtir.
Uzantının sürümünü almak için [Get-Azurermvmextensionımage](./Get-AzureRmVMExtensionImage.md) cmdlet 'ini kullanabilirsiniz.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS nesnesini belirtin.
Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 'i kullanabilirsiniz.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

###  
Bu cmdlet hiçbir çıkış üretmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-Azurermvmssextenma](./Remove-AzureRmVmssExtension.md)

[Get-Azurermvmımagepublisher](./Get-AzureRmVMImagePublisher.md)

[Get-Azurermvmextensionımagetype](./Get-AzureRmVMExtensionImageType.md)

[Get-Azurermvmextensionımage](./Get-AzureRmVMExtensionImage.md)

[Yeni-AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
