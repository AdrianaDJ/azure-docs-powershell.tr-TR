---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 5648bb1cb7497517afb5ff461674294e426c0131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932115"
---
# <span data-ttu-id="1fe39-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe39-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="1fe39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe39-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe39-103">Uygulama ağ geçidine HTTP dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="1fe39-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="1fe39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fe39-104">SYNTAX</span></span>

### <span data-ttu-id="1fe39-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="1fe39-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fe39-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1fe39-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fe39-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fe39-107">DESCRIPTION</span></span>
<span data-ttu-id="1fe39-108">**Add-AzApplicationGatewayHttpListener** cmdlet 'i uygulama ağ geçidine http dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="1fe39-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="1fe39-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fe39-109">EXAMPLES</span></span>

### <span data-ttu-id="1fe39-110">Örnek 1: HTTP dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="1fe39-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="1fe39-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine HTTP dinleyicisini ekler.</span><span class="sxs-lookup"><span data-stu-id="1fe39-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="1fe39-112">Örnek 2: SSL ile HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="1fe39-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="1fe39-113">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1fe39-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1fe39-114">İkinci komut, uygulama ağ geçidine HTTPS protokolünü kullanan dinleyiciyi ekler.</span><span class="sxs-lookup"><span data-stu-id="1fe39-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="1fe39-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fe39-115">PARAMETERS</span></span>

### <span data-ttu-id="1fe39-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fe39-116">-ApplicationGateway</span></span>
<span data-ttu-id="1fe39-117">Bu cmdlet 'in HTTP dinleyicisi eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="1fe39-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fe39-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="1fe39-119">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="1fe39-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="1fe39-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe39-120">-DefaultProfile</span></span>
<span data-ttu-id="1fe39-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fe39-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe39-122">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="1fe39-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="1fe39-123">Uygulama ağ geçidi ön uç IP kaynağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="1fe39-124">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="1fe39-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="1fe39-125">Uygulama ağ geçidi ön uç IP KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="1fe39-126">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="1fe39-126">-FrontendPort</span></span>
<span data-ttu-id="1fe39-127">Uygulama ağ geçidi ön uç bağlantı noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="1fe39-128">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="1fe39-128">-FrontendPortId</span></span>
<span data-ttu-id="1fe39-129">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="1fe39-130">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="1fe39-130">-HostName</span></span>
<span data-ttu-id="1fe39-131">Bu cmdlet 'in HTTP dinleyicisi eklediği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="1fe39-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="1fe39-132">-Name</span></span>
<span data-ttu-id="1fe39-133">Bu komutun eklediği ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="1fe39-134">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="1fe39-134">-Protocol</span></span>
<span data-ttu-id="1fe39-135">HTTP dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="1fe39-136">Hem HTTP hem de HTTPS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="1fe39-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="1fe39-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="1fe39-137">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="1fe39-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="1fe39-138">-SslCertificate</span></span>
<span data-ttu-id="1fe39-139">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="1fe39-140">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="1fe39-141">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="1fe39-141">-SslCertificateId</span></span>
<span data-ttu-id="1fe39-142">HTTP dinleyicisinin SSL sertifikası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="1fe39-143">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="1fe39-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="1fe39-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe39-144">CommonParameters</span></span>
<span data-ttu-id="1fe39-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fe39-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe39-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe39-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe39-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fe39-147">INPUTS</span></span>

### <span data-ttu-id="1fe39-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fe39-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1fe39-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fe39-149">OUTPUTS</span></span>

### <span data-ttu-id="1fe39-150">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1fe39-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1fe39-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fe39-151">NOTES</span></span>

## <span data-ttu-id="1fe39-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fe39-152">RELATED LINKS</span></span>

[<span data-ttu-id="1fe39-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe39-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1fe39-154">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe39-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1fe39-155">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe39-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="1fe39-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="1fe39-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


