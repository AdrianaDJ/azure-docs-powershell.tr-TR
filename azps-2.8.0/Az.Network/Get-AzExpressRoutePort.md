---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 69a03bc9772e9d74fdc1863221c99b46620ae700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932018"
---
# Get-AzExpressRoutePort

## SYNOPSIS
Bir Azure ExpressRoutePort kaynağını alır.

## INDEKI

### ResourceNameParameterSet (varsayılan)
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourceıdparameterset
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzExpressRoutePort** cmdlet 'i aboneliğinizden bir ExpressRoutePort nesnesini almak için kullanılır. Döndürülen expressrouteport nesnesi ExpressRoutePort üzerinde çalışan diğer cmdlet 'ler için girdi olarak kullanılabilir.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

Aboneliğinizdeki $rg $PortName adlı ExpressRoutePort nesnesini alır.

### Örnek 2
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

Adı "test" ile başlayan ExpressRoutePort nesnelerini alır.

### Örnek 3
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

RESOURCEID $id ile ExpressRoutePort nesnesini alır. 

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

### -Ad
ExpressRoutePort adı.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
ExpressRoutePort kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -RESOURCEID
Hızlı rota bağlantı noktasının RESOURCEID.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSExpressRoutePort

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzExpressRoutePort](./New-AzExpressRoutePort.md)

[Remove-AzExpressRoutePort](./Remove-AzExpressRoutePort.md)

[Set-AzExpressRoutePort](./Set-AzExpressRoutePort.md)
