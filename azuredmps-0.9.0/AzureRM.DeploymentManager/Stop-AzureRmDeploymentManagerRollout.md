---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761704"
---
# Stop-AzureRmDeploymentManagerRollout

## SYNOPSIS
Devam eden bir dağıtımı durdurur.

## INDEKI

### Etkileşimli (varsayılan)
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Içermiyor
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Stop-Azurermdeploymentmanagerpiyasaya** çıkarma cmdlet 'i devam etmekte olan bir dağıtımı durdurur
Dağıtımı adına ve kaynak grubu adına göre belirtin. Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.

Bir dağıtım durdurulduğunda, sürdürülemez veya yeniden başlatılamaz. Yalnızca yeni bir ürün oluşturabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı durdurur. 

### Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı durdurma
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Bu komut, ContosoResourceGroup 'da ContosoRollout adındaki bir dağıtımı durdurur.

### Örnek 3: piyasaya çıkarma nesnesini kullanarak bir dağıtımı durdurma.
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini durdurur.

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

### -Force
Onay sorma.

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
Ürün adı.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Kaynak tanımlayıcısı.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ürün
Kaldırılacak kaynak.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
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

### Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azurermdeploymentmanagerpiyasaya](./Get-AzureRmDeploymentManagerRollout.md)

[Restart-Azurermdeploymentmanagerpiyasaya](./Restart-AzureRmDeploymentManagerRollout.md)

[Remove-Azurermdeploymentmanagerpiyasaya](./Remove-AzureRmDeploymentManagerRollout.md)