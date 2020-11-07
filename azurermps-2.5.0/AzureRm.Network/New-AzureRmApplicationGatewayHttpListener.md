---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: f6b8e2a869ba6c59011241c5ebb7b1fe46ac2bc7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938941"
---
# <span data-ttu-id="72dde-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72dde-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="72dde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72dde-102">SYNOPSIS</span></span>
<span data-ttu-id="72dde-103">Uygulama ağ geçidi için HTTP dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72dde-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72dde-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72dde-104">SYNTAX</span></span>

### <span data-ttu-id="72dde-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="72dde-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72dde-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="72dde-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72dde-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="72dde-107">DESCRIPTION</span></span>
<span data-ttu-id="72dde-108">**New-AzureRmApplicationGatewayHttpListener** cmdlet 'ı bir Azure Application Gateway için http dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="72dde-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="72dde-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72dde-109">EXAMPLES</span></span>

### <span data-ttu-id="72dde-110">Örnek 1: HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="72dde-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="72dde-111">Bu komut Listener01 adlı bir HTTP dinleyicisi oluşturur ve sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="72dde-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="72dde-112">Örnek 2: SSL ile HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="72dde-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="72dde-113">Bu komut SSL boşaltması kullanan bir HTTP dinleyicisi oluşturur ve $SSLCert 01 değişkeninde SSL sertifikası sağlar.</span><span class="sxs-lookup"><span data-stu-id="72dde-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="72dde-114">Komut sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="72dde-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="72dde-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72dde-115">PARAMETERS</span></span>

### <span data-ttu-id="72dde-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72dde-116">-DefaultProfile</span></span>
<span data-ttu-id="72dde-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72dde-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72dde-118">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="72dde-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="72dde-119">HTTP dinleyicisi için ön uç IP yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="72dde-120">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="72dde-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="72dde-121">HTTP dinleyicisi için ön uç IP yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="72dde-122">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="72dde-122">-FrontendPort</span></span>
<span data-ttu-id="72dde-123">HTTP dinleyicisi için ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="72dde-124">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="72dde-124">-FrontendPortId</span></span>
<span data-ttu-id="72dde-125">HTTP dinleyicisi için ön uç bağlantı noktası nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="72dde-126">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="72dde-126">-HostName</span></span>
<span data-ttu-id="72dde-127">Uygulama ağ geçidi HTTP dinleyicisinin ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="72dde-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="72dde-128">-Name</span></span>
<span data-ttu-id="72dde-129">Bu cmdlet 'in oluşturduğu HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="72dde-130">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="72dde-130">-Protocol</span></span>
<span data-ttu-id="72dde-131">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="72dde-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="72dde-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="72dde-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="72dde-133">-SslCertificate</span></span>
<span data-ttu-id="72dde-134">HTTP dinleyicisi için SSL sertifikası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="72dde-135">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="72dde-135">-SslCertificateId</span></span>
<span data-ttu-id="72dde-136">HTTP dinleyicisi için SSL sertifikasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="72dde-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="72dde-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72dde-137">CommonParameters</span></span>
<span data-ttu-id="72dde-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72dde-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72dde-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72dde-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72dde-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72dde-140">INPUTS</span></span>

### <span data-ttu-id="72dde-141">System. String</span><span class="sxs-lookup"><span data-stu-id="72dde-141">System.String</span></span>

## <span data-ttu-id="72dde-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72dde-142">OUTPUTS</span></span>

### <span data-ttu-id="72dde-143">Microsoft. Azure. Commands. Network. modeller. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="72dde-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="72dde-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72dde-144">NOTES</span></span>

## <span data-ttu-id="72dde-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72dde-145">RELATED LINKS</span></span>

[<span data-ttu-id="72dde-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72dde-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="72dde-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72dde-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="72dde-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72dde-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="72dde-149">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="72dde-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


