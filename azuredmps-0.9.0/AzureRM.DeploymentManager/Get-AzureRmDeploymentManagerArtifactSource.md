---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761782"
---
# Get-AzureRmDeploymentManagerArtifactSource

## SYNOPSIS
Bir yapıt kaynağı alır.

## INDEKI

### Etkileşimli (varsayılan)
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmDeploymentManagerArtifactSource** cmdlet 'i bir yapıt kaynağı alır ve bu yapıt kaynağını temsil eden bir nesne döndürür.
Yapıt kaynağını adına ve kaynak grup adına göre belirtin. Alternatif olarak, ArtifactSource nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.

Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerArtifactSource cmdlet 'ini kullanarak yapı kaynağına değişiklikleri uygulayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: yapıt kaynağı alma
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağı alır.

### Örnek 2: kaynak tanımlayıcısını kullanarak yapıt kaynağı alma
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağı alır.

### Örnek 3: New-AzureRmDeploymentManagerArtifactSource tarafından döndürülen bir nesneyi kullanarak yapıt kaynağı alma
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

Bu komut, adı ve ResourceGroup 'in sırasıyla $artifactSourceObject Name ve ResourceGroupName özellikleriyle eşleşen bir yapıt kaynağı alır.

## PARAMETRELERINE

### -ArtifactSource
Yapıt kaynağı nesnesi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
Yapıt kaynağının adı.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmDeploymentManagerArtifactSource](./New-AzureRmDeploymentManagerArtifactSource.md)

[Remove-AzureRmDeploymentManagerArtifactSource](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[Set-AzureRmDeploymentManagerArtifactSource](./Set-AzureRmDeploymentManagerArtifactSource.md)