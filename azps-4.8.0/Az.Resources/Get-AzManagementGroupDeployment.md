---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 79eeb4e1725adf38b2f1dc70fe181280312fa1e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274227"
---
# Get-AzManagementGroupDeployment

## SYNOPSIS
Yönetim grubunda dağıtım alma

## INDEKI

### GetByDeploymentName (varsayılan)
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzManagementGroupDeployment** cmdlet 'i bir yönetim grubundaki dağıtımları alır.
Sonuçları filtrelemek için *ad* veya *ID* parametresini belirtin.
**Get-AzManagementGroupDeployment** , varsayılan olarak yönetim grubundaki tüm dağıtımları alır.

## ÖRNEKLERDEN

### Örnek 1: yönetim grubundaki tüm dağıtımları alma
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

Bu komut, "myMG" yönetim grubundaki tüm dağıtımları alır.

### Örnek 2: ada göre dağıtım alma
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

Bu komut, "myMG" yönetim grubunda "Deploy01" dağıtımını alır.
**Yeni-AzManagementGroupDeployment** cmdlet 'lerini kullanarak oluşturduğunuz dağıtıma bir ad atayabilirsiniz.
Bir ad atamazsanız, cmdlet 'ler dağıtımı oluşturmak için kullanılan şablona dayalı olarak varsayılan bir ad sağlar.

### Örnek 3: KIMLIĞE göre dağıtım alma
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

Bu komut, "myMG" yönetim grubunda "Deploy01" dağıtımını alır.

## PARAMETRELERINE

### -Apıversion
Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.
Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Dağıtımın tam kaynak kimliği.
Örnek:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupId
Yönetim grubu kimliği.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Dağıtımın adı.

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pre-
Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeplote

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
