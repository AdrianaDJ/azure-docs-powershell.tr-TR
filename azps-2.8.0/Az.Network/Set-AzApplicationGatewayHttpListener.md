---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932228"
---
# <span data-ttu-id="b5e25-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b5e25-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b5e25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5e25-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e25-103">Uygulama ağ geçidi için bir HTTP dinleyicisini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="b5e25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5e25-104">SYNTAX</span></span>

### <span data-ttu-id="b5e25-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b5e25-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5e25-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b5e25-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5e25-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5e25-107">DESCRIPTION</span></span>
<span data-ttu-id="b5e25-108">**Set-AzApplicationGatewayHttpListener** cmdlet 'i, bir Azure uygulama ağ GEÇIDI için HTTP dinleyicisini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="b5e25-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5e25-109">EXAMPLES</span></span>

### <span data-ttu-id="b5e25-110">Örnek 1: HTTP dinleyicisi ayarlama</span><span class="sxs-lookup"><span data-stu-id="b5e25-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="b5e25-111">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5e25-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b5e25-112">İkinci komut ağ geçidinin HTTP dinleyicisini, bağlantı noktası 80 ' da HTTP protokolüyle $FIP 01 ' de depolanan ön uç yapılandırmasını kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b5e25-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="b5e25-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5e25-113">PARAMETERS</span></span>

### <span data-ttu-id="b5e25-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5e25-114">-ApplicationGateway</span></span>
<span data-ttu-id="b5e25-115">Bu cmdlet 'in HTTP dinleyicisini ilişkilendiğinde uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="b5e25-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5e25-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="b5e25-117">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="b5e25-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="b5e25-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e25-118">-DefaultProfile</span></span>
<span data-ttu-id="b5e25-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5e25-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5e25-120">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="b5e25-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b5e25-121">Uygulama ağ geçidinin ön uç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b5e25-122">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="b5e25-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b5e25-123">Uygulama ağ geçidinin ön uç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="b5e25-124">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="b5e25-124">-FrontendPort</span></span>
<span data-ttu-id="b5e25-125">Uygulama ağ geçidi ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="b5e25-126">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="b5e25-126">-FrontendPortId</span></span>
<span data-ttu-id="b5e25-127">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="b5e25-128">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="b5e25-128">-HostName</span></span>
<span data-ttu-id="b5e25-129">Bu cmdlet 'in HTTP dinleyicisini gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="b5e25-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5e25-130">-Name</span></span>
<span data-ttu-id="b5e25-131">HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="b5e25-132">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b5e25-132">-Protocol</span></span>
<span data-ttu-id="b5e25-133">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="b5e25-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b5e25-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5e25-135">Http</span><span class="sxs-lookup"><span data-stu-id="b5e25-135">Http</span></span>
- <span data-ttu-id="b5e25-136">Https</span><span class="sxs-lookup"><span data-stu-id="b5e25-136">Https</span></span>

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

### <span data-ttu-id="b5e25-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b5e25-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="b5e25-138">Cmdlet 'in bir sunucu adı göstergesi gerektirip gerektirmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="b5e25-139">Bu parametre için kabul edilebilir değerler şunlardır: doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="b5e25-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="b5e25-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b5e25-140">-SslCertificate</span></span>
<span data-ttu-id="b5e25-141">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="b5e25-142">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="b5e25-142">-SslCertificateId</span></span>
<span data-ttu-id="b5e25-143">HTTP dinleyicisinin Güvenli Yuva Katmanı (SSL) sertifika KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e25-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="b5e25-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e25-144">CommonParameters</span></span>
<span data-ttu-id="b5e25-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5e25-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e25-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e25-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e25-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5e25-147">INPUTS</span></span>

### <span data-ttu-id="b5e25-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5e25-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5e25-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5e25-149">OUTPUTS</span></span>

### <span data-ttu-id="b5e25-150">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b5e25-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b5e25-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5e25-151">NOTES</span></span>

## <span data-ttu-id="b5e25-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5e25-152">RELATED LINKS</span></span>

[<span data-ttu-id="b5e25-153">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b5e25-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b5e25-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b5e25-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b5e25-155">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b5e25-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b5e25-156">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b5e25-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


