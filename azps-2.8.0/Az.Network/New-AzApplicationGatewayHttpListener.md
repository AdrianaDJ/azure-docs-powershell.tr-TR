---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918343"
---
# <span data-ttu-id="01118-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01118-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="01118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01118-102">SYNOPSIS</span></span>
<span data-ttu-id="01118-103">Uygulama ağ geçidi için HTTP dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01118-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="01118-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01118-104">SYNTAX</span></span>

### <span data-ttu-id="01118-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="01118-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="01118-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="01118-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01118-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01118-107">DESCRIPTION</span></span>
<span data-ttu-id="01118-108">**Yeni-AzApplicationGatewayHttpListener** cmdlet 'ı bir Azure uygulama ağ GEÇIDI için http dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01118-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="01118-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01118-109">EXAMPLES</span></span>

### <span data-ttu-id="01118-110">Örnek 1: HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="01118-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="01118-111">Bu komut Listener01 adlı bir HTTP dinleyicisi oluşturur ve sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="01118-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="01118-112">Örnek 2: SSL ile HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="01118-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="01118-113">Bu komut SSL boşaltması kullanan bir HTTP dinleyicisi oluşturur ve $SSLCert 01 değişkeninde SSL sertifikası sağlar.</span><span class="sxs-lookup"><span data-stu-id="01118-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="01118-114">Komut sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="01118-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="01118-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01118-115">PARAMETERS</span></span>

### <span data-ttu-id="01118-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="01118-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="01118-117">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="01118-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="01118-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01118-118">-DefaultProfile</span></span>
<span data-ttu-id="01118-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01118-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01118-120">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="01118-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="01118-121">HTTP dinleyicisi için ön uç IP yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="01118-122">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="01118-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="01118-123">HTTP dinleyicisi için ön uç IP yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="01118-124">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="01118-124">-FrontendPort</span></span>
<span data-ttu-id="01118-125">HTTP dinleyicisi için ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="01118-126">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="01118-126">-FrontendPortId</span></span>
<span data-ttu-id="01118-127">HTTP dinleyicisi için ön uç bağlantı noktası nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="01118-128">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="01118-128">-HostName</span></span>
<span data-ttu-id="01118-129">Uygulama ağ geçidi HTTP dinleyicisinin ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="01118-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="01118-130">-Name</span></span>
<span data-ttu-id="01118-131">Bu cmdlet 'in oluşturduğu HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="01118-132">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="01118-132">-Protocol</span></span>
<span data-ttu-id="01118-133">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="01118-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="01118-134">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01118-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="01118-135">-SslCertificate</span></span>
<span data-ttu-id="01118-136">HTTP dinleyicisi için SSL sertifikası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="01118-137">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="01118-137">-SslCertificateId</span></span>
<span data-ttu-id="01118-138">HTTP dinleyicisi için SSL sertifikasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="01118-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="01118-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01118-139">CommonParameters</span></span>
<span data-ttu-id="01118-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01118-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01118-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01118-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01118-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01118-142">INPUTS</span></span>

### <span data-ttu-id="01118-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="01118-143">None</span></span>

## <span data-ttu-id="01118-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01118-144">OUTPUTS</span></span>

### <span data-ttu-id="01118-145">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01118-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="01118-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01118-146">NOTES</span></span>

## <span data-ttu-id="01118-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01118-147">RELATED LINKS</span></span>

[<span data-ttu-id="01118-148">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01118-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="01118-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01118-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="01118-150">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01118-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="01118-151">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01118-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


