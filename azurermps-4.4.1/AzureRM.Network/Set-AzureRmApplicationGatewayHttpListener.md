---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 6805eaa6f1d710c607a7911b628d3642d48ece29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763097"
---
# <span data-ttu-id="9d9bd-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d9bd-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9d9bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="9d9bd-103">Uygulama ağ geçidi için bir HTTP dinleyicisini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d9bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d9bd-104">SYNTAX</span></span>

### <span data-ttu-id="9d9bd-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="9d9bd-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d9bd-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9d9bd-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d9bd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d9bd-107">DESCRIPTION</span></span>
<span data-ttu-id="9d9bd-108">**Set-AzureRmApplicationGatewayHttpListener** cmdlet 'ı bir Azure Application Gateway için HTTP dinleyicisini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="9d9bd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d9bd-109">EXAMPLES</span></span>

### <span data-ttu-id="9d9bd-110">Örnek 1: HTTP dinleyicisi ayarlama</span><span class="sxs-lookup"><span data-stu-id="9d9bd-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="9d9bd-111">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9d9bd-112">İkinci komut ağ geçidinin HTTP dinleyicisini, bağlantı noktası 80 ' da HTTP protokolüyle $FIP 01 ' de depolanan ön uç yapılandırmasını kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="9d9bd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d9bd-113">PARAMETERS</span></span>

### <span data-ttu-id="9d9bd-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d9bd-114">-ApplicationGateway</span></span>
<span data-ttu-id="9d9bd-115">Bu cmdlet 'in HTTP dinleyicisini ilişkilendiğinde uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="9d9bd-116">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="9d9bd-116">-FrontendIPConfiguration</span></span>
<span data-ttu-id="9d9bd-117">Uygulama ağ geçidinin ön uç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-117">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="9d9bd-118">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="9d9bd-118">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="9d9bd-119">Uygulama ağ geçidinin ön uç IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-119">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="9d9bd-120">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="9d9bd-120">-FrontendPort</span></span>
<span data-ttu-id="9d9bd-121">Uygulama ağ geçidi ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-121">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="9d9bd-122">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="9d9bd-122">-FrontendPortId</span></span>
<span data-ttu-id="9d9bd-123">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-123">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="9d9bd-124">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="9d9bd-124">-HostName</span></span>
<span data-ttu-id="9d9bd-125">Bu cmdlet 'in HTTP dinleyicisini gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-125">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="9d9bd-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="9d9bd-126">-Name</span></span>
<span data-ttu-id="9d9bd-127">HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-127">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="9d9bd-128">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="9d9bd-128">-Protocol</span></span>
<span data-ttu-id="9d9bd-129">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-129">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="9d9bd-130">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9d9bd-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d9bd-131">Http</span><span class="sxs-lookup"><span data-stu-id="9d9bd-131">Http</span></span>
- <span data-ttu-id="9d9bd-132">Https</span><span class="sxs-lookup"><span data-stu-id="9d9bd-132">Https</span></span>

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

### <span data-ttu-id="9d9bd-133">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="9d9bd-133">-RequireServerNameIndication</span></span>
<span data-ttu-id="9d9bd-134">Cmdlet 'in bir sunucu adı göstergesi gerektirip gerektirmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-134">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="9d9bd-135">Bu parametre için kabul edilebilir değerler şunlardır: doğru veya yanlış.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-135">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="9d9bd-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="9d9bd-136">-SslCertificate</span></span>
<span data-ttu-id="9d9bd-137">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-137">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="9d9bd-138">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="9d9bd-138">-SslCertificateId</span></span>
<span data-ttu-id="9d9bd-139">HTTP dinleyicisinin Güvenli Yuva Katmanı (SSL) sertifika KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-139">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="9d9bd-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d9bd-140">-DefaultProfile</span></span>
<span data-ttu-id="9d9bd-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d9bd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d9bd-142">CommonParameters</span></span>
<span data-ttu-id="9d9bd-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d9bd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d9bd-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d9bd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d9bd-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d9bd-145">INPUTS</span></span>

### <span data-ttu-id="9d9bd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9d9bd-146">System.String</span></span>

## <span data-ttu-id="9d9bd-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d9bd-147">OUTPUTS</span></span>

### <span data-ttu-id="9d9bd-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9d9bd-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9d9bd-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d9bd-149">NOTES</span></span>

## <span data-ttu-id="9d9bd-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d9bd-150">RELATED LINKS</span></span>

[<span data-ttu-id="9d9bd-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d9bd-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9d9bd-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d9bd-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9d9bd-153">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d9bd-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="9d9bd-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9d9bd-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


