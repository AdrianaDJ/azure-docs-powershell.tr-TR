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
# <span data-ttu-id="431cd-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="431cd-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="431cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="431cd-102">SYNOPSIS</span></span>
<span data-ttu-id="431cd-103">Uygulama ağ geçidine HTTP dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="431cd-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="431cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="431cd-104">SYNTAX</span></span>

### <span data-ttu-id="431cd-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="431cd-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="431cd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="431cd-106">SetByResource</span></span>
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

## <span data-ttu-id="431cd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="431cd-107">DESCRIPTION</span></span>
<span data-ttu-id="431cd-108">**Add-AzApplicationGatewayHttpListener** cmdlet 'i uygulama ağ geçidine http dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="431cd-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="431cd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="431cd-109">EXAMPLES</span></span>

### <span data-ttu-id="431cd-110">Örnek 1: HTTP dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="431cd-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="431cd-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine HTTP dinleyicisini ekler.</span><span class="sxs-lookup"><span data-stu-id="431cd-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="431cd-112">Örnek 2: SSL ile HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="431cd-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="431cd-113">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="431cd-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="431cd-114">İkinci komut, uygulama ağ geçidine HTTPS protokolünü kullanan dinleyiciyi ekler.</span><span class="sxs-lookup"><span data-stu-id="431cd-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="431cd-115">Örnek 3: SSL ve ana bilgisayar adları içeren HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="431cd-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="431cd-116">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="431cd-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="431cd-117">İkinci komut, uygulama ağ geçidine SSL sertifikaları ve ana bilgisayar adları olan HTTPS protokolünü kullanan dinleyiciyi ekler.</span><span class="sxs-lookup"><span data-stu-id="431cd-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="431cd-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="431cd-118">PARAMETERS</span></span>

### <span data-ttu-id="431cd-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="431cd-119">-ApplicationGateway</span></span>
<span data-ttu-id="431cd-120">Bu cmdlet 'in HTTP dinleyicisi eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="431cd-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="431cd-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="431cd-122">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="431cd-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="431cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="431cd-123">-DefaultProfile</span></span>
<span data-ttu-id="431cd-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="431cd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="431cd-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="431cd-125">-FirewallPolicy</span></span>
<span data-ttu-id="431cd-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="431cd-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="431cd-127">-Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="431cd-127">-FirewallPolicyId</span></span>
<span data-ttu-id="431cd-128">Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="431cd-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="431cd-129">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="431cd-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="431cd-130">Uygulama ağ geçidi ön uç IP kaynağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="431cd-131">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="431cd-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="431cd-132">Uygulama ağ geçidi ön uç IP KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="431cd-133">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="431cd-133">-FrontendPort</span></span>
<span data-ttu-id="431cd-134">Uygulama ağ geçidi ön uç bağlantı noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="431cd-135">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="431cd-135">-FrontendPortId</span></span>
<span data-ttu-id="431cd-136">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="431cd-137">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="431cd-137">-HostName</span></span>
<span data-ttu-id="431cd-138">Bu cmdlet 'in HTTP dinleyicisi eklediği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="431cd-139">-Ana makine adları</span><span class="sxs-lookup"><span data-stu-id="431cd-139">-HostNames</span></span>
<span data-ttu-id="431cd-140">Ana bilgisayar adları</span><span class="sxs-lookup"><span data-stu-id="431cd-140">Host names</span></span>

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

### <span data-ttu-id="431cd-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="431cd-141">-Name</span></span>
<span data-ttu-id="431cd-142">Bu komutun eklediği ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="431cd-143">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="431cd-143">-Protocol</span></span>
<span data-ttu-id="431cd-144">HTTP dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="431cd-145">Hem HTTP hem de HTTPS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="431cd-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="431cd-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="431cd-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="431cd-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="431cd-147">-SslCertificate</span></span>
<span data-ttu-id="431cd-148">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="431cd-149">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="431cd-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="431cd-150">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="431cd-150">-SslCertificateId</span></span>
<span data-ttu-id="431cd-151">HTTP dinleyicisinin SSL sertifikası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="431cd-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="431cd-152">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="431cd-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="431cd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="431cd-153">CommonParameters</span></span>
<span data-ttu-id="431cd-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="431cd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="431cd-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="431cd-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="431cd-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="431cd-156">INPUTS</span></span>

### <span data-ttu-id="431cd-157">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="431cd-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="431cd-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="431cd-158">OUTPUTS</span></span>

### <span data-ttu-id="431cd-159">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="431cd-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="431cd-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="431cd-160">NOTES</span></span>

## <span data-ttu-id="431cd-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="431cd-161">RELATED LINKS</span></span>

[<span data-ttu-id="431cd-162">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="431cd-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="431cd-163">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="431cd-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="431cd-164">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="431cd-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="431cd-165">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="431cd-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


