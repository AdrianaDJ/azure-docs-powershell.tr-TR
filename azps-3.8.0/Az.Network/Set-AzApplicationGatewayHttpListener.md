---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 3cc9af0865ca47099f5617cc1e94f3232ed9bdb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096828"
---
# <span data-ttu-id="5d0a4-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5d0a4-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5d0a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d0a4-103">Uygulama ağ geçidi için bir HTTP dinleyicisini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="5d0a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d0a4-104">SYNTAX</span></span>

### <span data-ttu-id="5d0a4-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="5d0a4-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5d0a4-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5d0a4-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d0a4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d0a4-107">DESCRIPTION</span></span>
<span data-ttu-id="5d0a4-108">**Set-AzApplicationGatewayHttpListener** cmdlet 'i, bir Azure uygulama ağ GEÇIDI için HTTP dinleyicisini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="5d0a4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d0a4-109">EXAMPLES</span></span>

### <span data-ttu-id="5d0a4-110">Örnek 1: HTTP dinleyicisi ayarlama</span><span class="sxs-lookup"><span data-stu-id="5d0a4-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="5d0a4-111">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5d0a4-112">İkinci komut ağ geçidinin HTTP dinleyicisini, bağlantı noktası 80 ' da HTTP protokolüyle $FIP 01 ' de depolanan ön uç yapılandırmasını kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="5d0a4-113">Örnek 2: SSL ve ana bilgisayar adları içeren bir HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="5d0a4-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="5d0a4-114">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5d0a4-115">İkinci komut, uygulama ağ geçidine SSL sertifikaları ve ana bilgisayar adları olan HTTPS protokolünü kullanan dinleyiciyi ekler.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="5d0a4-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d0a4-116">PARAMETERS</span></span>

### <span data-ttu-id="5d0a4-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d0a4-117">-ApplicationGateway</span></span>
<span data-ttu-id="5d0a4-118">Bu cmdlet 'in HTTP dinleyicisini ilişkilendiğinde uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="5d0a4-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d0a4-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="5d0a4-120">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="5d0a4-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="5d0a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d0a4-121">-DefaultProfile</span></span>
<span data-ttu-id="5d0a4-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d0a4-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5d0a4-123">-FirewallPolicy</span></span>
<span data-ttu-id="5d0a4-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="5d0a4-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="5d0a4-125">-Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="5d0a4-125">-FirewallPolicyId</span></span>
<span data-ttu-id="5d0a4-126">Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="5d0a4-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="5d0a4-127">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="5d0a4-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="5d0a4-128">Uygulama ağ geçidinin ön uç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="5d0a4-129">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="5d0a4-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="5d0a4-130">Uygulama ağ geçidinin ön uç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="5d0a4-131">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="5d0a4-131">-FrontendPort</span></span>
<span data-ttu-id="5d0a4-132">Uygulama ağ geçidi ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="5d0a4-133">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="5d0a4-133">-FrontendPortId</span></span>
<span data-ttu-id="5d0a4-134">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="5d0a4-135">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="5d0a4-135">-HostName</span></span>
<span data-ttu-id="5d0a4-136">Bu cmdlet 'in HTTP dinleyicisini gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="5d0a4-137">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="5d0a4-137">-HostNames</span></span>
<span data-ttu-id="5d0a4-138">Ana bilgisayar adları</span><span class="sxs-lookup"><span data-stu-id="5d0a4-138">Host names</span></span>

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

### <span data-ttu-id="5d0a4-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d0a4-139">-Name</span></span>
<span data-ttu-id="5d0a4-140">HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="5d0a4-141">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="5d0a4-141">-Protocol</span></span>
<span data-ttu-id="5d0a4-142">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="5d0a4-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5d0a4-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5d0a4-144">Http</span><span class="sxs-lookup"><span data-stu-id="5d0a4-144">Http</span></span>
- <span data-ttu-id="5d0a4-145">Https</span><span class="sxs-lookup"><span data-stu-id="5d0a4-145">Https</span></span>

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

### <span data-ttu-id="5d0a4-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="5d0a4-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="5d0a4-147">Cmdlet 'in bir sunucu adı göstergesi gerektirip gerektirmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="5d0a4-148">Bu parametre için kabul edilebilir değerler şunlardır: doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="5d0a4-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5d0a4-149">-SslCertificate</span></span>
<span data-ttu-id="5d0a4-150">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="5d0a4-151">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="5d0a4-151">-SslCertificateId</span></span>
<span data-ttu-id="5d0a4-152">HTTP dinleyicisinin Güvenli Yuva Katmanı (SSL) sertifika KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="5d0a4-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d0a4-153">CommonParameters</span></span>
<span data-ttu-id="5d0a4-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d0a4-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d0a4-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d0a4-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d0a4-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d0a4-156">INPUTS</span></span>

### <span data-ttu-id="5d0a4-157">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d0a4-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5d0a4-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d0a4-158">OUTPUTS</span></span>

### <span data-ttu-id="5d0a4-159">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d0a4-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5d0a4-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d0a4-160">NOTES</span></span>

## <span data-ttu-id="5d0a4-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d0a4-161">RELATED LINKS</span></span>

[<span data-ttu-id="5d0a4-162">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5d0a4-162">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5d0a4-163">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5d0a4-163">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5d0a4-164">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5d0a4-164">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="5d0a4-165">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5d0a4-165">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


