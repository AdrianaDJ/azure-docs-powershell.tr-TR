---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935584"
---
# Get-AzApplicationGatewayProbeConfig

## SYNOPSIS
Uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.

## INDEKI

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzApplicationGatewayProbeConfig cmdlet 'i uygulama ağ geçidinden var olan bir sistem durumu araştırması yapılandırmasını alır.

## ÖRNEKLERDEN

### Örnek 1: uygulama ağ geçidinden varolan bir araştırma alma
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

Bu komut ağ geçidi adlı uygulama ağ geçidinden Probe02 adlı sistem durumu araştırılmasını alır.

## PARAMETRELERINE

### -ApplicationGateway
Bu cmdlet 'in yoklama yapılandırması aldığı uygulama ağ geçidini belirtir.

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
Araştırın adını belirtir.

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

### PSApplicationGateway
Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe

### System. Koleksiyonlar. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Var olan uygulama ağ geçidine araştırma ekleme](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[Add-AzApplicationGatewayProbeConfig]()

[Yeni-AzApplicationGatewayProbeConfig]()

[Remove-AzApplicationGatewayProbeConfig]()

[Set-AzApplicationGatewayProbeConfig]()

