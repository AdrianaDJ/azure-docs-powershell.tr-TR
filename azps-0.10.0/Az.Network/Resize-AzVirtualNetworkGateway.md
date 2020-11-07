---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DE2441FC-9504-4F3F-AEAF-37EDCD9B7275
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/resize-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Resize-AzVirtualNetworkGateway.md
ms.openlocfilehash: bd42d7cec30b7d42dcb1cdb3657f6681bf2cb6b0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936584"
---
# Resize-AzVirtualNetworkGateway

## SYNOPSIS
Var olan bir sanal ağ ağ geçidini yeniden boyutlandırır.

## INDEKI

```
Resize-AzVirtualNetworkGateway -VirtualNetworkGateway <PSVirtualNetworkGateway> -GatewaySku <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Resize-AzVirtualNetworkGateway** cmdlet 'i, sanal ağ geçidi için hisse senedi BIRIMINI (SKU) değiştirmenizi sağlar.
STB 'ler, üretilen iş ve izin verilen en fazla IP tüneli sayısı dahil olmak üzere, ağ geçidinin özelliklerini belirler.
Azure temel, standart, yüksek performanslı, VpnGw1, VpnGw2 ve VpnGw3 SKU 'Larını (bazen küçük, orta ve büyük STB 'ler olarak da adlandırılır) destekler.
Her SKU türünün özellikleri hakkında ayrıntılı bilgi için bkz https://azure.microsoft.com/en-us/documentation/articles/vpn-gateway-about-vpngateways/ .

STB 'Ların, yeteneklerin yanı sıra fiyatlandırmayla farklı olmasına dikkat edin.
Daha fazla bilgi için bkz https://azure.microsoft.com/en-us/pricing/details/vpn-gateway/ .

## ÖRNEKLERDEN

### Örnek 1: sanal ağ geçidi boyutunu değiştirme
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Resize-AzVirtualNetworkGateway -VirtualNetworkGateway $Gateway -GatewaySku "Basic"
```

Bu örnekte, ContosoVirtualGateway adındaki sanal ağ geçidinin boyutu değişir.

İlk komut, ContosoVirtualGateway için bir nesne başvurusu oluşturur; Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.

İkinci komut daha sonra *Gatewaysku* özelliğini temel olarak ayarlamak için **Resize-AzVirtualNetworkGateway** cmdlet 'ini kullanır.

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

### -GatewaySku
Yeni ağ geçidi SKU türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Ana
- Ardından
- Yüksek performans
- VpnGw1
- VpnGw2
- VpnGw3

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkGateway
Yeniden boyutlandırılacak sanal ağ geçidi 'nin nesne başvurusunu belirtir.
Bu nesne başvurusunu oluşturmak için Get-AzVirtualNetworkGateway kullanarak ağ geçidinin adını belirtin.

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin ardışık olarak birleştirilmiş örneklerini kabul eder.

## ÇıKıŞLAR

###  
Bu cmdlet, **Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway** nesnesinin varolan örneklerini değiştirir.

## NOTLARıNDA
Temel/standart/üst performans SKU 'larından yeni VpnGw1/VpnGw2/VpnGw3 SKU 'Larını yeniden boyutlandıramazsınız. https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-about-vpngatewaysYönergeler için bkz.

## ILGILI BAĞLANTıLAR

[Get-AzVpnClientPackage](./Get-AzVpnClientPackage.md)

[Get-AzVirtualNetworkGateway](./Get-AzVirtualNetworkGateway.md)

[Set-AzVirtualNetworkGatewayVpnClientConfig](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


