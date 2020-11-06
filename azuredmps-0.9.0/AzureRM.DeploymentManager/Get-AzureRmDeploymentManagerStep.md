---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571530"
---
# Get-AzureRmDeploymentManagerStep

## SYNOPSIS
Dağıtım adımını alır.

## INDEKI

### Etkileşimli (varsayılan)
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmDeploymentManagerStep** cmdlet 'i bir adım alır ve bu adımı temsil eden bir nesne döndürür.
Adım adını ve kaynak grubu adını belirtin. Alternatif olarak, Step nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.

Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerStep cmdlet 'ini kullanarak yapı kaynağına değişiklikleri uygulayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: adım alma
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

Bu komut, ContosoResourceGroup 'da ContosoService1WaitStep adındaki bir adımı alır.

### Örnek 2: kaynak tanımlayıcısını kullanarak bir adım alma
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

Bu komut, ContosoResourceGroup 'da ContosoService1WaitStep adındaki bir adımı alır.

### Örnek 3: New-AzureRmDeploymentManagerStep tarafından döndürülen bir nesneyi kullanarak adım alma
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 Bu komut, adı ve ResourceGroup 'in sırasıyla $stepObject Name ve ResourceGroupName özellikleriyle eşleşen bir adımını alır.


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
Adımın adı.

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

### -Adım
Adım kaynak nesnesi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.
Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DeploymentManager. modeller. PSStepResource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
