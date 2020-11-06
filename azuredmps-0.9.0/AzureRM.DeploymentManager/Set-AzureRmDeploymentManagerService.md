---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571389"
---
# Set-AzureRmDeploymentManagerService

## SYNOPSIS
Hizmet topolojisinde bir hizmeti güncelleştirir.

## INDEKI

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmDeploymentManagerService** cmdlet 'i belirtilen hizmet nesnesiyle bir hizmeti güncelleştirir.
Cmdlet, güncelleştirilmiş hizmet nesnesini döndürür.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

Bu komut, adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla $serviceObject adı, ServiceTopologyName ve ResourceGroupName özellikleriyle eşleşen bir hizmeti güncelleştirir.
Hizmet, $serviceObject belirlenen özelliklere güncelleştirilecektir.

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

### -Hizmet
Hizmet nesnesi.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
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

### Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource

## ÇıKıŞLAR

### Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmDeploymentManagerService](./New-AzureRmDeploymentManagerService.md)

[Get-AzureRmDeploymentManagerService](./Set-AzureRmDeploymentManagerService.md)

[Remove-AzureRmDeploymentManagerService](./Remove-AzureRmDeploymentManagerService.md)