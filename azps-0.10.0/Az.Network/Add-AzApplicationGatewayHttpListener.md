---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: eaae79c09f6ee609d7a7bf645c2312007a78ad59
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935657"
---
# <span data-ttu-id="52862-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="52862-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="52862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52862-102">SYNOPSIS</span></span>
<span data-ttu-id="52862-103">Uygulama ağ geçidine HTTP dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="52862-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="52862-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52862-104">SYNTAX</span></span>

### <span data-ttu-id="52862-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="52862-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52862-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="52862-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52862-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="52862-107">DESCRIPTION</span></span>
<span data-ttu-id="52862-108">**Add-AzApplicationGatewayHttpListener** cmdlet 'i uygulama ağ geçidine http dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="52862-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="52862-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52862-109">EXAMPLES</span></span>

### <span data-ttu-id="52862-110">Örnek 1: HTTP dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="52862-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="52862-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine HTTP dinleyicisini ekler.</span><span class="sxs-lookup"><span data-stu-id="52862-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="52862-112">Örnek 2: SSL ile HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="52862-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="52862-113">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="52862-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="52862-114">İkinci komut, uygulama ağ geçidine HTTPS protokolünü kullanan dinleyiciyi ekler.</span><span class="sxs-lookup"><span data-stu-id="52862-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="52862-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52862-115">PARAMETERS</span></span>

### <span data-ttu-id="52862-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="52862-116">-ApplicationGateway</span></span>
<span data-ttu-id="52862-117">Bu cmdlet 'in HTTP dinleyicisi eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="52862-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52862-118">-DefaultProfile</span></span>
<span data-ttu-id="52862-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="52862-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52862-120">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="52862-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="52862-121">Uygulama ağ geçidi ön uç IP kaynağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-121">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-122">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="52862-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="52862-123">Uygulama ağ geçidi ön uç IP KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-123">Specifies the application gateway front-end IP ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-124">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="52862-124">-FrontendPort</span></span>
<span data-ttu-id="52862-125">Uygulama ağ geçidi ön uç bağlantı noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-125">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-126">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="52862-126">-FrontendPortId</span></span>
<span data-ttu-id="52862-127">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-127">Specifies the application gateway front-end port ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-128">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="52862-128">-HostName</span></span>
<span data-ttu-id="52862-129">Bu cmdlet 'in HTTP dinleyicisi eklediği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="52862-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="52862-130">-Name</span></span>
<span data-ttu-id="52862-131">Bu komutun eklediği ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-131">Specifies the name of the front-end port that this command adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-132">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="52862-132">-Protocol</span></span>
<span data-ttu-id="52862-133">HTTP dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="52862-134">Hem HTTP hem de HTTPS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="52862-134">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="52862-135">-RequireServerNameIndication</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="52862-136">-SslCertificate</span></span>
<span data-ttu-id="52862-137">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="52862-138">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="52862-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-139">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="52862-139">-SslCertificateId</span></span>
<span data-ttu-id="52862-140">HTTP dinleyicisinin SSL sertifikası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="52862-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="52862-141">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="52862-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52862-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52862-142">CommonParameters</span></span>
<span data-ttu-id="52862-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52862-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52862-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52862-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52862-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52862-145">INPUTS</span></span>

### <span data-ttu-id="52862-146">System. String</span><span class="sxs-lookup"><span data-stu-id="52862-146">System.String</span></span>

## <span data-ttu-id="52862-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52862-147">OUTPUTS</span></span>

### <span data-ttu-id="52862-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="52862-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="52862-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52862-149">NOTES</span></span>

## <span data-ttu-id="52862-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52862-150">RELATED LINKS</span></span>

[<span data-ttu-id="52862-151">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="52862-151">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="52862-152">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="52862-152">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="52862-153">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="52862-153">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="52862-154">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="52862-154">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


