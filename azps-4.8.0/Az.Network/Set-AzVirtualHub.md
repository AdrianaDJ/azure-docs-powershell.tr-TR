---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualHub.md
ms.openlocfilehash: 12bf5d24421f79eecb3138a68425968b9b4fbe62
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274061"
---
# Set-AzVirtualHub

## SYNOPSIS
Sanal hub 'ı değiştirir ve buna sanal hub yol tablosu ekler.

## INDEKI

### ByVirtualHubName (varsayılan)
```
Set-AzVirtualHub -ResourceGroupName <String> -Name <String> -RouteTable <PSVirtualHubRouteTable[]>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Byvirtualhubresourceıd
```
Set-AzVirtualHub -ResourceId <String> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByVirtualHubObject
```
Set-AzVirtualHub -InputObject <PSVirtualHub> -RouteTable <PSVirtualHubRouteTable[]> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
{{Açıklamayı doldurun}}

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> $existingHub�=�Get-AzVirtualHub�-ResourceGroupName�"testRg"�-Name�"westushub"
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> $routeTable1�=�Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"
PS C:\> Set-AzVirtualHub�-VirtualHub�$existingHub�-RouteTable�@($routeTable1)

VirtualWan                            : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/testWan
ResourceGroupName                     : testRg
Name                                  : westushub
Id                                    : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubswestushub
AddressPrefix                         : 10.40.0.0/16
RouteTable                            : Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable
VirtualNetworkExpressRouteConnections :
RouteTables                           : {routeTable1}
Location                              : westus
Sku                                   : Standard
Type                                  : Microsoft.Network/virtualHubs
ProvisioningState                     : Succeeded
```

İlk önce bir sanal hub yol nesnesi oluşturun ve sanal hub yol tablosu kaynağı oluşturmak için bunu kullanın. Ardından, Set-AzVirtualHub komutunu kullanarak bu yol tablosu kaynağını sanal hub olarak ayarladık.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

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

### -InputObject
Değiştirilecek sanal hub nesnesi.

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Kaynak adı.

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases: ResourceName, VirtualHubName, HubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Değiştirilecek sanal hub 'ın kaynak kimliği.

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RouteTable
Bu sanal hub ile ilişkilendirilmiş yol tabloları.

```yaml
Type: PSVirtualHubRouteTable[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Kaynak etiketlerini temsil eden bir Hashtable.

```yaml
Type: Hashtable
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### Microsoft. Azure. Commands. Network. modeller. PSVirtualHub

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSVirtualHub

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
