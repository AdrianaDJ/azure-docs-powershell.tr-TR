---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571277"
---
# Get-AzureRmDeploymentManagerRollout

## SYNOPSIS
Bir piyasaya çıkma alır.

## INDEKI

### Etkileşimli (varsayılan)
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azurermdeploymentmanagerpiyasaya** çıkarma cmdlet 'i bir piyasaya alır ve bu sürümü, kademeli olan bilgilerin tüm ayrıntılı bilgileriyle birlikte döndürür.
Dağıtımı adına ve kaynak grubu adına göre belirtin. Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır.

### Örnek 2: kaynak tanımlayıcısını kullanarak bir ürün edinin
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır.

### Örnek 3: piyasaya çıkarma nesnesini kullanarak bir ürün edinin.
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

Bu komut, adı ve ResourceGroup 'in sırasıyla $rolloutObject Name ve ResourceGroupName özellikleriyle eşleşen bir dağıtımı alır.

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

### -RetryAttempt
Piyasaya yeniden deneme girişimi.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ürün
Piyasaya çıkarma nesnesi.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Stop-Azurermdeploymentmanagerpiyasaya](./Stop-AzureRmDeploymentManagerRollout.md)

[Restart-Azurermdeploymentmanagerpiyasaya](./Restart-AzureRmDeploymentManagerRollout.md)

[Remove-Azurermdeploymentmanagerpiyasaya](./Remove-AzureRmDeploymentManagerRollout.md)