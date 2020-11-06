---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572201"
---
# Restart-AzureRmDeploymentManagerRollout

## SYNOPSIS
Başarısız bir dağıtımı yeniden başlatın.

## INDEKI

### Etkileşimli (varsayılan)
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Içermiyor
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Restart-Azurermdeploymentmanagerpiyasaya kapatma** cmdlet 'i başarısız olan bir dağıtımı yeniden başlatır ve bu sürümü, kademeli olan bilgilerin tüm ayrıntılı bilgileriyle birlikte döndürür.
Dağıtımı adına ve kaynak grubu adına göre belirtin. Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.
İsteğe bağlı parametre SkipSucceeded, önceki sürümdeki tüm başarılı adımları atlamanıza olanak tanır.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

Bu komut, ContosoRollout adındaki bir dağıtımı yeniden başlatır. SkipSucceeded bayrağı, başarıyla çalıştırılan tüm adımların atlanacağını ve piyasaya yürütmenin son başarısız olduğunda yürütmeye devam etmesi gerektiğini belirtir.

### Örnek 2: kaynak tanımlayıcısını kullanarak bir dağıtımı yeniden başlatın
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Bu komut, ContosoRollout adındaki bir dağıtımı yeniden başlatır.

### Örnek 3: piyasaya çıkarma nesnesini kullanarak bir dağıtımı yeniden başlatın.
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

Bu komut, adı ve ResourceGroup 'ın sırasıyla $rolloutObject ad ve ResourceGroupName özellikleriyle eşleştiğini yeniden başlatır.

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

### -SkipSucceeded
Önceki çalıştırmada başarılı olan adımları atlayın.

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
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

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

[Stop-Azurermdeploymentmanagerpiyasaya](./Stop-AzureRmDeploymentManagerRollout.md)

[Remove-Azurermdeploymentmanagerpiyasaya](./Remove-AzureRmDeploymentManagerRollout.md)