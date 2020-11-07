---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: be1e70538aae66b05bdff5b06859cfb2f30681ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935588"
---
# Get-AzApplicationGatewayFrontendPort

## SYNOPSIS
Uygulama ağ geçidinin ön uç bağlantı noktasını alır.

## INDEKI

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azapplicationgatewayfrontenvseçport** cmdlet 'i, uygulama ağ geçidinin ön uç bağlantı noktasını alır.

## ÖRNEKLERDEN

### Örnek 1: belirtilen ön uç bağlantı noktasını alma
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.
İkinci komut, $AppGw FrontEndPort01 adındaki ön uç bağlantı noktasını alır ve $FrontEndPort değişkeninde depolar.

### Örnek 2: ön uç bağlantı noktalarının listesini alma
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

İlk komut, ResourceGroup01 adındaki kaynak grubundan ApplicationGateway01 adlı bir uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.
İkinci komut $AppGw 'dan ön uç bağlantı noktalarının bir listesini alır ve $FrontEndPorts değişkeninde depolar.

## PARAMETRELERINE

### -ApplicationGateway
Ön uç bağlantı noktasını içeren uygulama ağ geçidi nesnesini belirtir.

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
Alınacak ön uç bağlantı noktasının adını belirtir.

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

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azapplicationgatewayfrontenvseçport](./Add-AzApplicationGatewayFrontendPort.md)

[Yeni-Azapplicationgatewayfrontenvseçport](./New-AzApplicationGatewayFrontendPort.md)

[Remove-Azapplicationgatewayfrontenvseçport](./Remove-AzApplicationGatewayFrontendPort.md)

[Set-Azapplicationgatewayfrontenvseçport](./Set-AzApplicationGatewayFrontendPort.md)


