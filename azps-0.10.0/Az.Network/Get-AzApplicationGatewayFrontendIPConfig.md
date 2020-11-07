---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 364C41D0-A5DB-4AEF-853A-FE5A11AD9155
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2004fe6a10fe2700d256ae4cae8419ab631a2f64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935587"
---
# Get-AzApplicationGatewayFrontendIPConfig

## SYNOPSIS
Uygulama ağ geçidinin ön uç IP yapılandırmasını alır.

## INDEKI

```
Get-AzApplicationGatewayFrontendIPConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azapplicationgatewayfrontendıconfıg** cmdlet 'i, uygulama ağ geçidinin ön uç IP yapılandırmasını alır.

## ÖRNEKLERDEN

### Örnek 1: belirtilen ön uç IP yapılandırmasını alma
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIP= Get-AzApplicationGatewayFrontendIPConfig -Name "FrontEndIP01" -ApplicationGateway $AppGw
```

İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, FrontEndIP01 adlı ön uç IP yapılandırmasını $AppGw ve $FrontEndIP değişkeninde depolar.

### Örnek 2: ön uç IP yapılandırmalarının listesini alma
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndIPs= Get-AzApplicationGatewayFrontendIPConfig  -ApplicationGateway $AppGw
```

İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut $AppGw 'dan ön uç IP yapılandırmalarının bir listesini alır ve $FrontEndIPs değişkeninde depolar.

## PARAMETRELERINE

### -ApplicationGateway
Ön uç IP yapılandırmasını içeren uygulama ağ geçidi nesnesini belirtir.

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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
Bu cmdlet 'in aldığı ön uç IP yapılandırmasının adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendIPConfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azapplicationgatewayfrontendıconfıg yapılandırması](./Add-AzApplicationGatewayFrontendIPConfig.md)

[Yeni-Azapplicationgatewayfrontendıyapılandırma](./New-AzApplicationGatewayFrontendIPConfig.md)

[Remove-Azapplicationgatewayfrontendıyapılandırma](./Remove-AzApplicationGatewayFrontendIPConfig.md)

[Set-Azapplicationgatewayfrontendıyapılandırma](./Set-AzApplicationGatewayFrontendIPConfig.md)


