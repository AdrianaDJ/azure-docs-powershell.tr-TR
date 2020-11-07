---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764338"
---
# Remove-AzureRmDelegation

## SYNOPSIS
Sağlanan alt ağdan bir hizmet temsilcisini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-Azurermtemsilci** cmdlet 'i, temsilcileri olan bir alt ağı alır ve bu alt ağdan adlandırılmış temsilciyi kaldırır.

## ÖRNEKLERDEN

### Örnek 1
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

Bu örnekte, ilk yarısı ( _"varolan bir alt ağa Temsilci Ekle"_ altında bulunan), [-Azurermtemsilci ekleme](./Add-AzureRmDelegation.md)ile aynıdır. İkinci yarısında, ilk iki cmdlet ilgilendiğiniz alt ağı alır ve Yerel kopyayı sunucuda olduğu gibi yenileyin. Üçüncü cmdlet _mysubnet_ 'den ilk yarısı oluşturulmuş temsilciyi kaldırır ve güncelleştirilen alt ağı _$subnet_ olarak depolar. Son cmdlet, sunucuyu kaldırılan temsilciyle güncelleştirir.

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
Temsilci adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HizmetAdı
Alt ağın temsil ettiği hizmetin adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Alt ağ
Temsilci seçiminin kaldırılacağı alt ağ

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. PSSubnet
### System. String
## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSSubnet
## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermtemsilci](./Add-AzureRmDelegation.md) 
 [Get-Azurermtemsilci](./Get-AzureRmDelegation.md) 
 [Yeni-Azurermtemsilci](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)
