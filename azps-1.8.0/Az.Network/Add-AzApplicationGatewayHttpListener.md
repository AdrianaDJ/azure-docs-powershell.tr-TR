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
ms.locfileid: "93760745"
---
# <span data-ttu-id="6197d-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6197d-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6197d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6197d-102">SYNOPSIS</span></span>
<span data-ttu-id="6197d-103">Uygulama ağ geçidine HTTP dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="6197d-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="6197d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6197d-104">SYNTAX</span></span>

### <span data-ttu-id="6197d-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6197d-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6197d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6197d-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6197d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6197d-107">DESCRIPTION</span></span>
<span data-ttu-id="6197d-108">**Add-AzApplicationGatewayHttpListener** cmdlet 'i uygulama ağ geçidine http dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="6197d-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="6197d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6197d-109">EXAMPLES</span></span>

### <span data-ttu-id="6197d-110">Örnek 1: HTTP dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="6197d-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="6197d-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine HTTP dinleyicisini ekler.</span><span class="sxs-lookup"><span data-stu-id="6197d-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="6197d-112">Örnek 2: SSL ile HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="6197d-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="6197d-113">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6197d-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6197d-114">İkinci komut, uygulama ağ geçidine HTTPS protokolünü kullanan dinleyiciyi ekler.</span><span class="sxs-lookup"><span data-stu-id="6197d-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="6197d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6197d-115">PARAMETERS</span></span>

### <span data-ttu-id="6197d-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6197d-116">-ApplicationGateway</span></span>
<span data-ttu-id="6197d-117">Bu cmdlet 'in HTTP dinleyicisi eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="6197d-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6197d-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="6197d-119">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="6197d-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="6197d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6197d-120">-DefaultProfile</span></span>
<span data-ttu-id="6197d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6197d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6197d-122">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="6197d-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="6197d-123">Uygulama ağ geçidi ön uç IP kaynağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="6197d-124">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="6197d-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="6197d-125">Uygulama ağ geçidi ön uç IP KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="6197d-126">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="6197d-126">-FrontendPort</span></span>
<span data-ttu-id="6197d-127">Uygulama ağ geçidi ön uç bağlantı noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="6197d-128">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="6197d-128">-FrontendPortId</span></span>
<span data-ttu-id="6197d-129">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="6197d-130">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="6197d-130">-HostName</span></span>
<span data-ttu-id="6197d-131">Bu cmdlet 'in HTTP dinleyicisi eklediği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="6197d-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="6197d-132">-Name</span></span>
<span data-ttu-id="6197d-133">Bu komutun eklediği ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="6197d-134">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="6197d-134">-Protocol</span></span>
<span data-ttu-id="6197d-135">HTTP dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="6197d-136">Hem HTTP hem de HTTPS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="6197d-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="6197d-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="6197d-137">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="6197d-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="6197d-138">-SslCertificate</span></span>
<span data-ttu-id="6197d-139">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="6197d-140">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6197d-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="6197d-141">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="6197d-141">-SslCertificateId</span></span>
<span data-ttu-id="6197d-142">HTTP dinleyicisinin SSL sertifikası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6197d-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="6197d-143">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6197d-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="6197d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6197d-144">CommonParameters</span></span>
<span data-ttu-id="6197d-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6197d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6197d-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6197d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6197d-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6197d-147">INPUTS</span></span>

### <span data-ttu-id="6197d-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6197d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6197d-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6197d-149">OUTPUTS</span></span>

### <span data-ttu-id="6197d-150">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6197d-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6197d-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6197d-151">NOTES</span></span>

## <span data-ttu-id="6197d-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6197d-152">RELATED LINKS</span></span>

[<span data-ttu-id="6197d-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6197d-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6197d-154">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6197d-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6197d-155">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6197d-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6197d-156">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6197d-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


