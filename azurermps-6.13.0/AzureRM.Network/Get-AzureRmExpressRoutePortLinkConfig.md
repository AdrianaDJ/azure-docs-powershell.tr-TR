---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594379"
---
# Get-AzureRmExpressRoutePortLinkConfig

## SYNOPSIS
ExpressRoutePort bağlantı yapılandırmasını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ResourceNameParameterSet (varsayılan)
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourceıdparameterset
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmExpressRoutePortLinkConfig** cmdlet 'ı ExpressRoutePort bağlantısının yapılandırmasını alır.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

ExpressRoutePort 'un link1 yapılandırmasını alır $erport

### Örnek 2
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

ExpressRoutePort $erport RESOURCEID $id ile bağlantının yapılandırmasını alır

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

### -ExpressRoutePort
ExpressRoutePort kaynağının başvurusu.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Ad
Bağlantının adı.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Bağlantının RESOURCEID.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. model. PSExpressRoutePort

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSExpressRouteLink

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
