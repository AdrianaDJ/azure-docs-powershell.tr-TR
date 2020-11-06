---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E066BBFA-2E03-431D-85D1-99F230B6AC59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterface.md
ms.openlocfilehash: e17ac9d538424e3e7883060e6a3dcbec9c6a2c8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595082"
---
# Get-AzureRmNetworkInterface

## SYNOPSIS
Ağ arabirimini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### NoExpandStandAloneNic (varsayılan)
```
Get-AzureRmNetworkInterface [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Expandstandlı
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NoExpandScaleSetNic
```
Get-AzureRmNetworkInterface [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ExpandScaleSetNic
```
Get-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azurermnetworkınterface** cmdlet 'ı bir Azure ağ arabirimini veya kaynak grubundaki Azure ağ arabirimlerinin listesini alır.

## ÖRNEKLERDEN

### Örnek 1: tüm ağ arabirimlerini alma
```
PS C:\>Get-AzureRmNetworkInterface
```

Bu komut geçerli aboneliğin tüm ağ arabirimlerini alır.

### Örnek 2: belirli bir sağlama durumuyla tüm ağ arabirimlerini alma
```
PS C:\>Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" | Where-Object {$_.ProvisioningState -eq 'Succeeded'}
```

Bu komut, kaynak grubundaki, kaynak grubundaki, sağlama durumu başarılı olan tüm ağ arabirimlerini ResourceGroup1.

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

### -ExpandResource
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in aldığı ağ arabiriminin adını belirtir.

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic, NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in ağ arabirimlerini aldığı kaynak grubun adını belirtir.

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneNic, NoExpandScaleSetNic, ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Virtualmachineındex
Bu cmdlet 'in ağ arabirimlerini aldığı sanal makine ölçek kümesinin sanal makine dizinini belirtir.

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSetName
Bu cmdlet 'in ağ arabirimlerini aldığı sanal makine ölçeği kümesinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetNic
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetNic
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azurermnetworkınterface](./New-AzureRmNetworkInterface.md)

[Remove-Azurermnetworkınterface](./Remove-AzureRmNetworkInterface.md)

[Set-Azurermnetworkınterface](./Set-AzureRmNetworkInterface.md)


