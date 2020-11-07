---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 6cf8dc5ab895ac59697b10494f7f39d158238d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764549"
---
# <span data-ttu-id="753df-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="753df-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="753df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="753df-102">SYNOPSIS</span></span>
<span data-ttu-id="753df-103">Uygulama ağ geçidine HTTP dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="753df-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="753df-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="753df-104">SYNTAX</span></span>

### <span data-ttu-id="753df-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="753df-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="753df-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="753df-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="753df-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="753df-107">DESCRIPTION</span></span>
<span data-ttu-id="753df-108">**Add-AzureRmApplicationGatewayHttpListener** cmdlet 'i uygulama ağ geçidine http dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="753df-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="753df-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="753df-109">EXAMPLES</span></span>

### <span data-ttu-id="753df-110">Örnek 1: HTTP dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="753df-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="753df-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine HTTP dinleyicisini ekler.</span><span class="sxs-lookup"><span data-stu-id="753df-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="753df-112">Örnek 2: SSL ile HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="753df-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="753df-113">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="753df-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="753df-114">İkinci komut, uygulama ağ geçidine HTTPS protokolünü kullanan dinleyiciyi ekler.</span><span class="sxs-lookup"><span data-stu-id="753df-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="753df-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="753df-115">PARAMETERS</span></span>

### <span data-ttu-id="753df-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="753df-116">-ApplicationGateway</span></span>
<span data-ttu-id="753df-117">Bu cmdlet 'in HTTP dinleyicisi eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="753df-118">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="753df-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="753df-119">Uygulama ağ geçidi ön uç IP kaynağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-119">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="753df-120">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="753df-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="753df-121">Uygulama ağ geçidi ön uç IP KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-121">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="753df-122">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="753df-122">-FrontendPort</span></span>
<span data-ttu-id="753df-123">Uygulama ağ geçidi ön uç bağlantı noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-123">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="753df-124">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="753df-124">-FrontendPortId</span></span>
<span data-ttu-id="753df-125">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="753df-126">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="753df-126">-HostName</span></span>
<span data-ttu-id="753df-127">Bu cmdlet 'in HTTP dinleyicisi eklediği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-127">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="753df-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="753df-128">-Name</span></span>
<span data-ttu-id="753df-129">Bu komutun eklediği ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-129">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="753df-130">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="753df-130">-Protocol</span></span>
<span data-ttu-id="753df-131">HTTP dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-131">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="753df-132">Hem HTTP hem de HTTPS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="753df-132">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="753df-133">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="753df-133">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="753df-134">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="753df-134">-SslCertificate</span></span>
<span data-ttu-id="753df-135">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-135">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="753df-136">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="753df-136">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="753df-137">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="753df-137">-SslCertificateId</span></span>
<span data-ttu-id="753df-138">HTTP dinleyicisinin SSL sertifikası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="753df-138">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="753df-139">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="753df-139">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="753df-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753df-140">-DefaultProfile</span></span>
<span data-ttu-id="753df-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="753df-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="753df-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753df-142">CommonParameters</span></span>
<span data-ttu-id="753df-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="753df-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753df-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="753df-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753df-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="753df-145">INPUTS</span></span>

### <span data-ttu-id="753df-146">System. String</span><span class="sxs-lookup"><span data-stu-id="753df-146">System.String</span></span>

## <span data-ttu-id="753df-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="753df-147">OUTPUTS</span></span>

### <span data-ttu-id="753df-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="753df-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="753df-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="753df-149">NOTES</span></span>

## <span data-ttu-id="753df-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="753df-150">RELATED LINKS</span></span>

[<span data-ttu-id="753df-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="753df-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="753df-152">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="753df-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="753df-153">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="753df-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="753df-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="753df-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


