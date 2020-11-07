---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 26cf3a0fb3ae118913130a754def47a257aac254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764420"
---
# <span data-ttu-id="d326d-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d326d-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d326d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d326d-102">SYNOPSIS</span></span>
<span data-ttu-id="d326d-103">Uygulama ağ geçidi için bir HTTP dinleyicisini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d326d-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d326d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d326d-104">SYNTAX</span></span>

### <span data-ttu-id="d326d-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d326d-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d326d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d326d-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d326d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d326d-107">DESCRIPTION</span></span>
<span data-ttu-id="d326d-108">**Set-AzureRmApplicationGatewayHttpListener** cmdlet 'ı bir Azure Application Gateway için HTTP dinleyicisini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d326d-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="d326d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d326d-109">EXAMPLES</span></span>

### <span data-ttu-id="d326d-110">Örnek 1: HTTP dinleyicisi ayarlama</span><span class="sxs-lookup"><span data-stu-id="d326d-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="d326d-111">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d326d-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="d326d-112">İkinci komut ağ geçidinin HTTP dinleyicisini, bağlantı noktası 80 ' da HTTP protokolüyle $FIP 01 ' de depolanan ön uç yapılandırmasını kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d326d-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="d326d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d326d-113">PARAMETERS</span></span>

### <span data-ttu-id="d326d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d326d-114">-ApplicationGateway</span></span>
<span data-ttu-id="d326d-115">Bu cmdlet 'in HTTP dinleyicisini ilişkilendiğinde uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="d326d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d326d-116">-DefaultProfile</span></span>
<span data-ttu-id="d326d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d326d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d326d-118">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="d326d-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="d326d-119">Uygulama ağ geçidinin ön uç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d326d-120">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="d326d-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="d326d-121">Uygulama ağ geçidinin ön uç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="d326d-122">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="d326d-122">-FrontendPort</span></span>
<span data-ttu-id="d326d-123">Uygulama ağ geçidi ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="d326d-124">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="d326d-124">-FrontendPortId</span></span>
<span data-ttu-id="d326d-125">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="d326d-126">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="d326d-126">-HostName</span></span>
<span data-ttu-id="d326d-127">Bu cmdlet 'in HTTP dinleyicisini gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="d326d-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="d326d-128">-Name</span></span>
<span data-ttu-id="d326d-129">HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="d326d-130">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d326d-130">-Protocol</span></span>
<span data-ttu-id="d326d-131">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="d326d-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d326d-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d326d-133">Http</span><span class="sxs-lookup"><span data-stu-id="d326d-133">Http</span></span>
- <span data-ttu-id="d326d-134">Https</span><span class="sxs-lookup"><span data-stu-id="d326d-134">Https</span></span>

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

### <span data-ttu-id="d326d-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="d326d-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="d326d-136">Cmdlet 'in bir sunucu adı göstergesi gerektirip gerektirmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="d326d-137">Bu parametre için kabul edilebilir değerler şunlardır: doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="d326d-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="d326d-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="d326d-138">-SslCertificate</span></span>
<span data-ttu-id="d326d-139">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="d326d-140">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="d326d-140">-SslCertificateId</span></span>
<span data-ttu-id="d326d-141">HTTP dinleyicisinin Güvenli Yuva Katmanı (SSL) sertifika KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d326d-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="d326d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d326d-142">CommonParameters</span></span>
<span data-ttu-id="d326d-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d326d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d326d-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d326d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d326d-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d326d-145">INPUTS</span></span>

### <span data-ttu-id="d326d-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d326d-146">System.String</span></span>

## <span data-ttu-id="d326d-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d326d-147">OUTPUTS</span></span>

### <span data-ttu-id="d326d-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d326d-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d326d-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d326d-149">NOTES</span></span>

## <span data-ttu-id="d326d-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d326d-150">RELATED LINKS</span></span>

[<span data-ttu-id="d326d-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d326d-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d326d-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d326d-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d326d-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d326d-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="d326d-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d326d-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

