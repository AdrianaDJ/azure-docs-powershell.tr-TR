---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7A1B92F5-C698-4D5E-ACD7-4013F1BC6247
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: a0c2b1dbad943a690ae2965a9ea9520063909b9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273682"
---
# Add-AzVmssDiagnosticsExtension

## SYNOPSIS
VMSUBNET 'e bir tanılama uzantısı ekler.

## INDEKI

```
Add-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-SettingFilePath] <String>
 [[-ProtectedSettingFilePath] <String>] [[-Name] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Add-Azvmssdiagnosticsextenma** cmdlet 'ı, sanal makine ölçek KÜMESI (VMSS) örneğine bir tanılama uzantısı ekler.

## ÖRNEKLERDEN

### Örnek 1: VMSS 'ye tanılama uzantısı ekleme
```
PS C:\> Add-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -SettingFilePath $publicConfigPath -ProtectedSettingFilePath $privateConfigPath -Name $extName -TypeHandlerVersion $typeVersion -AutoUpgradeMinorVersion $True -Force
```

Bu komut, VMSS 'ye bir tanılama uzantısı ekler.

## PARAMETRELERINE

### -AutoUpgradeMinorVersion
Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesine izin verip vermediğini gösterir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -Ad
Bir uzantının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Protectedsettingdosyayolu
Özel yapılandırma dosyasının yolunu belirtir.

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

### -Settingdosyayolu
Genel yapılandırma dosyasının yolunu belirtir.

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

### -TypeHandlerVersion
Bu VMSS için kullanılacak uzantının sürümünü belirtir.
Sürümü edinmek için, *PublisherName* parametresi ve *tür* parametresi için ıaasdiagnostics değeriyle [Get-azvmextensionımage](./Get-AzVMExtensionImage.md) cmdlet 'ini çalıştırın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS nesnesini belirtin.
Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet

### System. String

### System. Boolean

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzVmssExtension](./Add-AzVmssExtension.md)

[Remove-azvmssdiagnosticsexten](./Remove-AzVmssDiagnosticsExtension.md)

[Set-azvmdiagnosticsexten](./Set-AzVMDiagnosticsExtension.md)
