---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275263"
---
# Add-AzApplicationGatewayHttpListener

## SYNOPSIS
Uygulama ağ geçidine HTTP dinleyicisi ekler.

## INDEKI

### Setbyresourceıd
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SetByResource
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Add-AzApplicationGatewayHttpListener** cmdlet 'i uygulama ağ geçidine http dinleyicisi ekler.

## ÖRNEKLERDEN

### Örnek 1: HTTP dinleyicisi ekleme
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine HTTP dinleyicisini ekler.

### Örnek 2: SSL ile HTTPS dinleyicisi ekleme
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.
İkinci komut, uygulama ağ geçidine HTTPS protokolünü kullanan dinleyiciyi ekler.

### Örnek 3: SSL ve ana bilgisayar adları içeren HTTPS dinleyicisi ekleme
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.
İkinci komut, uygulama ağ geçidine SSL sertifikaları ve ana bilgisayar adları olan HTTPS protokolünü kullanan dinleyiciyi ekler.

## PARAMETRELERINE

### -ApplicationGateway
Bu cmdlet 'in HTTP dinleyicisi eklediği uygulama ağ geçidini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CustomErrorConfiguration
Uygulama ağ geçidinde müşteri hatası

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicy
FirewallPolicy

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Firewallpolicyıd
Firewallpolicyıd

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Frontendıyapılandırma
Uygulama ağ geçidi ön uç IP kaynağı nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Frontendıconfigurationıd
Uygulama ağ geçidi ön uç IP KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Frontenvseçport
Uygulama ağ geçidi ön uç bağlantı noktası nesnesini belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Frontenvseçportıd
Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ana bilgisayar adı
Bu cmdlet 'in HTTP dinleyicisi eklediği ana bilgisayar adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ana makine adları
Ana bilgisayar adları

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Bu komutun eklediği ön uç bağlantı noktasının adını belirtir.

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

### -İletişim kuralı
HTTP dinleyicisi protokolünü belirtir.
Hem HTTP hem de HTTPS destekleniyor.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireServerNameIndication
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslCertificate
HTTP dinleyicisinin SSL sertifikasını belirtir.
HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sslcertificateıd
HTTP dinleyicisinin SSL sertifikası KIMLIĞINI belirtir.
HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
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

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzApplicationGatewayHttpListener](./Get-AzApplicationGatewayHttpListener.md)

[Yeni-AzApplicationGatewayHttpListener](./New-AzApplicationGatewayHttpListener.md)

[Remove-AzApplicationGatewayHttpListener](./Remove-AzApplicationGatewayHttpListener.md)

[Set-AzApplicationGatewayHttpListener](./Set-AzApplicationGatewayHttpListener.md)


