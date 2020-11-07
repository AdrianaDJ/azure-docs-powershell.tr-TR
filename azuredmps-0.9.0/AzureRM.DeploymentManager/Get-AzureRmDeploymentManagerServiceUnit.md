---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761705"
---
# Get-AzureRmDeploymentManagerServiceUnit

## SYNOPSIS
Hizmet birimini alır.

## INDEKI

### Etkileşimli (varsayılan)
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceObject
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByServiceResourceId
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTopologyObjectAndServiceName
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByTopologyResourceAndServiceName
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Içermiyor
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmDeploymentManagerServiceUnit** cmdlet 'i, bir hizmette hizmet birimini alır.

Hizmet birimini adına, tanımladığı hizmete, hizmet topolojisi adına ve kaynak grubu adına göre belirtin. Alternatif olarak, ServiceUnit nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.

Bu nesneyi yerel olarak değiştirebilir ve Set-AzureRmDeploymentManagerServiceUnit cmdlet 'ini kullanarak hizmet birimine değişiklikler uygulayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.

### Örnek 2: kaynak tanımlayıcısını kullanarak bir hizmet birimi alın.
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.

### Örnek 3: hizmet birimi nesnesini kullanarak bir hizmet birimi alın.
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

Bu komut, adı, hizmet adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla adı, HizmetAdı, ServiceTopologyName ve ResourceGroupName $serviceUnitObject özellikleriyle eşleşen bir hizmet birimini alır.

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
Hizmet biriminin adı.

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu.

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
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

### -Hizmet
Hizmet biriminin oluşturulması gereken servis nesnesi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HizmetAdı
Hizmet biriminin parçası olduğu hizmetin adı.

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceResourceId
Hizmet biriminin oluşturulması gereken hizmet kaynak tanıtıcısı.

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTopology
Hizmet biriminin oluşturulması gereken hizmet topolojisi nesnesi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceTopologyName
Hizmet biriminin parçası olan hizmet topolojisinin adı.

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

### -Servicetopologyresourceıd
Hizmet biriminin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceUnit
Hizmet birimi kaynak nesnesi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
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

### Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmDeploymentManagerServiceUnit](./New-AzureRmDeploymentManagerServiceUnit.md)

[Remove-AzureRmDeploymentManagerServiceUnit](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[Set-AzureRmDeploymentManagerServiceUnit](./Set-AzureRmDeploymentManagerServiceUnit.md)