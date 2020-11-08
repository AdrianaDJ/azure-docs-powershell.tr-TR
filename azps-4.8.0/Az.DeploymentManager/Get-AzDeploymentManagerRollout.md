---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108331"
---
# Get-AzDeploymentManagerRollout

## SYNOPSIS
Dağıtımı alır.

## INDEKI

### Etkileşimli (varsayılan)
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azdeploymentmanagerpiyasaya dağıtım** cmdlet 'i bir piyasaya alır ve bu sürümü, piyasaya çıkarma işleminin ilerleme durumuyla ilgili tüm ayrıntılı bilgilerle birlikte döndürür.
Dağıtımı adına ve kaynak grubu adına göre belirtin. Alternatif olarak, piyasaya çıkarma veya RESOURCEID sağlayabilirsiniz.

Döndürülen dağıtım nesnesi, dağıtılan Hizmetleri, hizmet birimlerini ve adımları ve sürmekte olan adımları içerir. Henüz dağıtılmayan olanlar yanıt vermiyor.

## ÖRNEKLERDEN

### Örnek 1 dağıtımı alın
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır. 

### Örnek 2 dağıtım ayrıntılarını alma ve görüntüleme
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır. -Verbose anahtarı tüm dağıtım ayrıntılarını hiyerarşik olarak görüntüler; Hizmetin, hizmet birimlerinin ve her bir Holistic görünümü için her adımın altındaki adımları gösterin.

### Örnek 3: kaynak tanımlayıcısını kullanarak bir ürün edinin
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Bu komut, ContosoResourceGroup 'da ContosoRollout adlı bir piyasaya alır.

### Örnek 4: piyasaya çıkarma nesnesini kullanarak bir ürün edinin.
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

Bu komut, adı ve ResourceGroup 'in sırasıyla $rolloutObject Name ve ResourceGroupName özellikleriyle eşleşen bir dağıtımı alır.

## PARAMETRELERINE

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

### -InputObject
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

### -Ad
Ürün adı.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
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
Accept pipeline input: False
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

### Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DeploymentManager. modeller. Pspiyasaya çıkarma

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
