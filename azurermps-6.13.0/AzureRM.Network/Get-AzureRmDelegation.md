---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592762"
---
# Get-AzureRmDelegation

## SYNOPSIS
Verilen bir alt ağda bir temsilci (veya tüm temsilcileri) edinin.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-Azurermtemsilci** cmdlet 'i alt ağdan adlandırılmış temsilciyi alır. Herhangi bir temsilci adı adlandırılmadıysa, sağlanan alt ağdaki tüm temsilcileri döndürür.

## ÖRNEKLERDEN

### 1: belirli bir temsilci alma
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

İlk satır ilgi alt ağını alır. İkinci satır "Benimtemsilci" adlı temsilci için temsilci bilgilerini gösterir.

### 2: tüm alt ağ temsilcileri alınıyor
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

İlk satır ilgi alt ağını alır. İkinci satır, _Mysubnet_ 'teki tüm temsilci listesini $Delegations değişkeninde depolar.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Temsilci adı

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

### -Alt ağ
Alt ağ

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.
Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. PSSubnet

## ÇıKıŞLAR

### Microsoft.Azure.Commands.Network.Models.PSD

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
[Add-Azurermtemsilci](./Add-AzureRmDelegation.md) 
 [Yeni-Azurermtemsilci](./New-AzureRmDelegation.md) 
 [Remove-Azurermtemsilci](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
