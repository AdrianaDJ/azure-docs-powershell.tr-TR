---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVM.md
ms.openlocfilehash: 8601a7cc6a02211a0264030784485a5ecb4d29fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588555"
---
# Get-AzureRmVM

## SYNOPSIS
Sanal makinenin özelliklerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Listallvirtual, Inesparamset (varsayılan)
```
Get-AzureRmVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listvirtualmachineınresourcegroupparamset
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Getvirtualmachineınresourcegroupparamset
```
Get-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listlocationvirtual
```
Get-AzureRmVM -Location <String> [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Listnextlinkvirtual, Inesparamset
```
Get-AzureRmVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmVM** cmdlet 'i, bir Azure sanal makinesinin model görünümünü ve örnek görünümünü alır.
Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.
Örnek görünümü sanal makinenin örnek düzeyi durumudur.
Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.

## ÖRNEKLERDEN

### Örnek 1: model ve örnek görünümü özelliklerini alma
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

Bu komut, VirtualMachine07 adındaki sanal makinenin model görünümü ve örnek görünümü özelliklerini alır.

### Örnek 2: örnek görünümü özelliklerini alma
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

Bu komut, VirtualMachine07 adındaki sanal makinenin özelliklerini alır.
Bu komut, *Status* parametresini belirtir.
Bu nedenle, komut yalnızca örnek görünümü özelliklerini alır.

### Örnek 3: kaynak grubundaki tüm sanal makinelerin özelliklerini alma
```
PS C:\> Get-AzureRmVM -ResourceGroupName "ResourceGroup11"
```

Bu komut, ResourceGroup11 adlı kaynak grubundaki tüm sanal makinelerin özelliklerini alır.

### Örnek 4: aboneliğinizdeki tüm sanal makineleri edinme
```
PS C:\> Get-AzureRmVM
```

Bu komut aboneliğinizdeki tüm sanal makineleri alır.

### Örnek 5: konumdaki tüm sanal makineleri edinin.
```
PS C:\> Get-AzureRmVM -Location "westus"
```

Bu komut, Batı ABD bölgesindeki tüm sanal makineleri alır.

## PARAMETRELERINE

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

### -DisplayHint
Sanal makine nesnesinin nasıl görüntülendiğini belirler.
Geçerli değerler:--Compact: yalnızca üst düzey özelliklerini görüntüler--Genişlet: tüm düzeylerdeki tüm özellikleri görüntüler

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases:
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Görüntülenecek sanal makinelerin konumunu belirtir.

```yaml
Type: System.String
Parameter Sets: ListLocationVirtualMachinesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Alınacak sanal makinenin adını belirtir.

```yaml
Type: System.String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Sonraki bağlantıyı belirtir.

```yaml
Type: System.Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Durum
Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Uri

### Microsoft. Azure. Commands. COMPUTE. modeller. DisplayHintType

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine

### Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineınstanceview

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmVM](./New-AzureRmVM.md)

[Remove-AzureRmVM](./Remove-AzureRmVM.md)

[Restart-AzureRmVM](./Restart-AzureRmVM.md)

[Başlangıç-AzureRmVM](./Start-AzureRmVM.md)

[Stop-AzureRmVM](./Stop-AzureRmVM.md)

[Güncelleştirme-AzureRmVM](./Update-AzureRmVM.md)


