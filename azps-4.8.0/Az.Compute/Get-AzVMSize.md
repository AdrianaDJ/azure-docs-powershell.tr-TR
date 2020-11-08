---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: e9ed9350b8ffdd93dd83843ee083c90bac786edd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108416"
---
# Get-AzVMSize

## SYNOPSIS
Kullanılabilir sanal makine boyutlarını alır.

## INDEKI

### Listvirtualparaminesizeparamset (varsayılan)
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listavailablesizesforkullanılabilirliği Bilityset
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzVMSize** cmdlet 'i kullanılabilir sanal makine boyutlarını alır.

## ÖRNEKLERDEN

### Örnek 1: bir konum için sanal makine boyutlarını alma
```
PS C:\> Get-AzVMSize -Location "Central US"
```

Bu komut, belirtilen konumdaki sanal makinelerin kullanılabilir boyutlarını alır.

### Örnek 2: kullanılabilirlik kümesi için boyutları alma
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

Bu komut, AvailabilitySet17 adlı kullanılabilirlik kümesinde dağıtabileceğiniz sanal makinelerin kullanılabilir boyutlarını alır.

### Örnek 3: var olan bir sanal makinenin boyutlarını alma
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

Bu komut, VirtualMachine12 adındaki mevcut sanal makine için kullanılabilir boyutları alır.
Bu komutun aldığı boyutlara bu sanal makineyi yeniden boyutlandırabilirsiniz.

## PARAMETRELERINE

### -Kullanılabilirlik
Bu cmdlet 'in kullanılabilir sanal makine boyutlarını aldığı kullanılabilirlik kümesinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Konum
Bu cmdlet 'in kullanılabilir sanal makine boyutlarını aldığı konumu belirtir.

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Bu cmdlet 'in yeniden boyutlandırma için kullanılabilir sanal makine boyutlarını aldığı sanal makinenin adını belirtir.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. psvirtualın

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVM](./Get-AzVM.md)


