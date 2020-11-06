---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: b9c2499c3172fcd34000c8adaa0bde144217bcbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589851"
---
# Remove-AzureRmVMDiagnosticsExtension

## SYNOPSIS
Sanal makineden tanılama uzantısını kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## Tanım
**Remove-Azurermvmdiagnosticsextenma** cmdlet 'i, bir Azure Diagnostics uzantısını sanal makineden kaldırır.
Değişikliklerinizi uygulamak için bu cmdlet 'in çıkışını Update-AzureRmVM cmdlet 'ine geçirmelisiniz.

## ÖRNEKLERDEN

### Örnek 1: sanal makineden tanılama uzantısını kaldırma
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

Bu komut, ContosoVM22 adındaki bir sanal makineden tanılama uzantısını kaldırır.
Komut sonucu, ardışık düzen işlecini kullanarak Update-AzureRmVM cmdlet 'ine geçirir.
Bu komut sanal makineyi güncelleştirir.

## PARAMETRELERINE

### -Ad
Bu cmdlet 'in kaldırıldığı tanılama uzantısının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
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
Bu cmdlet 'in tanılama uzantısını kaldırdığı sanal makinenin adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-azurermvmdiagnosticsexten](./Get-AzureRMVMDiagnosticsExtension.md)

[Set-azurermvmdiagnosticsexten](./Set-AzureRMVMDiagnosticsExtension.md)

[Güncelleştirme-AzureRmVM](./Update-AzureRmVM.md)


