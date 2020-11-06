---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMSize.md
ms.openlocfilehash: 33abc50f4cc336230e1c6f4ef14d12f51b22af83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595196"
---
# Get-AzureRmVMSize

## SYNOPSIS
Kullanılabilir sanal makine boyutlarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Listvirtualparaminesizeparamset (varsayılan)
```
Get-AzureRmVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listavailablesizesforkullanılabilirliği Bilityset
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzureRmVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmVMSize** cmdlet 'i kullanılabilir sanal makine boyutlarını alır.

## ÖRNEKLERDEN

### Örnek 1: bir konum için sanal makine boyutlarını alma
```
PS C:\> Get-AzureRmVMSize -Location "Central US"
```

Bu komut, belirtilen konumdaki sanal makinelerin kullanılabilir boyutlarını alır.

### Örnek 2: kullanılabilirlik kümesi için boyutları alma
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

Bu komut, AvailabilitySet17 adlı kullanılabilirlik kümesinde dağıtabileceğiniz sanal makinelerin kullanılabilir boyutlarını alır.

### Örnek 3: var olan bir sanal makinenin boyutlarını alma
```
PS C:\> Get-AzureRmVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmVM](./Get-AzureRmVM.md)


