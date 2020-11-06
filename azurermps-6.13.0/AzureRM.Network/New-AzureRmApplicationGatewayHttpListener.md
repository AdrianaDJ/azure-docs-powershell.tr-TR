---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 29df7c4ac7cb941e8826c3e1fb929d92cc626512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592307"
---
# <span data-ttu-id="bf4ae-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4ae-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bf4ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="bf4ae-103">Uygulama ağ geçidi için HTTP dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf4ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf4ae-104">SYNTAX</span></span>

### <span data-ttu-id="bf4ae-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="bf4ae-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bf4ae-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bf4ae-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf4ae-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf4ae-107">DESCRIPTION</span></span>
<span data-ttu-id="bf4ae-108">**New-AzureRmApplicationGatewayHttpListener** cmdlet 'ı bir Azure Application Gateway için http dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="bf4ae-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf4ae-109">EXAMPLES</span></span>

### <span data-ttu-id="bf4ae-110">Örnek 1: HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bf4ae-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="bf4ae-111">Bu komut Listener01 adlı bir HTTP dinleyicisi oluşturur ve sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="bf4ae-112">Örnek 2: SSL ile HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bf4ae-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="bf4ae-113">Bu komut SSL boşaltması kullanan bir HTTP dinleyicisi oluşturur ve $SSLCert 01 değişkeninde SSL sertifikası sağlar.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="bf4ae-114">Komut sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="bf4ae-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf4ae-115">PARAMETERS</span></span>

### <span data-ttu-id="bf4ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf4ae-116">-DefaultProfile</span></span>
<span data-ttu-id="bf4ae-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf4ae-118">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="bf4ae-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="bf4ae-119">HTTP dinleyicisi için ön uç IP yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="bf4ae-120">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="bf4ae-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="bf4ae-121">HTTP dinleyicisi için ön uç IP yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="bf4ae-122">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="bf4ae-122">-FrontendPort</span></span>
<span data-ttu-id="bf4ae-123">HTTP dinleyicisi için ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="bf4ae-124">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="bf4ae-124">-FrontendPortId</span></span>
<span data-ttu-id="bf4ae-125">HTTP dinleyicisi için ön uç bağlantı noktası nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="bf4ae-126">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="bf4ae-126">-HostName</span></span>
<span data-ttu-id="bf4ae-127">Uygulama ağ geçidi HTTP dinleyicisinin ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="bf4ae-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf4ae-128">-Name</span></span>
<span data-ttu-id="bf4ae-129">Bu cmdlet 'in oluşturduğu HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="bf4ae-130">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="bf4ae-130">-Protocol</span></span>
<span data-ttu-id="bf4ae-131">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="bf4ae-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="bf4ae-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="bf4ae-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="bf4ae-133">-SslCertificate</span></span>
<span data-ttu-id="bf4ae-134">HTTP dinleyicisi için SSL sertifikası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="bf4ae-135">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="bf4ae-135">-SslCertificateId</span></span>
<span data-ttu-id="bf4ae-136">HTTP dinleyicisi için SSL sertifikasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="bf4ae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf4ae-137">CommonParameters</span></span>
<span data-ttu-id="bf4ae-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf4ae-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf4ae-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf4ae-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf4ae-140">INPUTS</span></span>

### <span data-ttu-id="bf4ae-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bf4ae-141">None</span></span>

## <span data-ttu-id="bf4ae-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf4ae-142">OUTPUTS</span></span>

### <span data-ttu-id="bf4ae-143">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4ae-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bf4ae-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf4ae-144">NOTES</span></span>

## <span data-ttu-id="bf4ae-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf4ae-145">RELATED LINKS</span></span>

[<span data-ttu-id="bf4ae-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4ae-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bf4ae-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4ae-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bf4ae-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4ae-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bf4ae-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4ae-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


