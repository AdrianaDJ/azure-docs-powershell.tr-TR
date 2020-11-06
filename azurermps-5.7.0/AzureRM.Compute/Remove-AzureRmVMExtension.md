---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: da05148a0e27ba553f80fa18b44cb45decf9f1df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586794"
---
# Remove-AzureRmVMExtension

## SYNOPSIS
Sanal makineden uzantıyı kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-Azurermvmexter** cmdlet 'i, sanal makinenin sanal makine uzantılarından bir uzantıyı kaldırır.

## ÖRNEKLERDEN

### Örnek 1: sanal makineden uzantıyı kaldırma
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

Bu komut, ResourceGroup11 'da VirtualMachine22 adındaki sanal makineden ContosoTest adlı uzantıyı kaldırır.

## PARAMETRELERINE

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in kaldırdığı uzantının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.

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

### -VMName
Bu cmdlet 'in uzantıyı kaldırdığı sanal makinenin adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.

Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
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

[Get-Azurermvmexgeri](./Get-AzureRmVMExtension.md)

[Set-Azurermvmexgeri](./Set-AzureRmVMExtension.md)


