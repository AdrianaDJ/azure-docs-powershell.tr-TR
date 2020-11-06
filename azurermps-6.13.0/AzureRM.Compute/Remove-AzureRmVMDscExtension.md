---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDscExtension.md
ms.openlocfilehash: b25b65e9c42cd388d685320802690c6538122e94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587258"
---
# Remove-AzureRmVMDscExtension

## SYNOPSIS
Bir kaynak grubundaki sanal makineden DSC genişletme işleyicisini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmVMDscExtension** cmdlet 'i, bir kaynak grubundaki sanal makineden Istenen durum yapılandırma (DSC) uzantı işleyicisini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: DSC uzantısını kaldırma
```
PS C:\> Remove-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

Bu komut, VM07 adındaki sanal makinede DSC adlı uzantıyı kaldırır.

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

### -Ad
Bu cmdlet 'in kaldırıldığı DSC uzantısının adını belirtir.
Set-AzureRmVMDscExtension cmdlet, **Remove-AzureRmVMDscExtension** tarafından kullanılan varsayılan değer olan Microsoft. POWERSHELL. DSC olarak ayarlanır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Bu cmdlet 'in DSC uzantısını kaldırdığı sanal makinenin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmVMDscExtension](./Get-AzureRmVMDscExtension.md)

[Set-AzureRmVMDscExtension](./Set-AzureRmVMDscExtension.md)


