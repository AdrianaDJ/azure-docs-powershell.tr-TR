---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 104a5e022d89421ac960d699c7391db660c0dd6b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935428"
---
# <span data-ttu-id="ddbad-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddbad-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ddbad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddbad-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbad-103">Uygulama ağ geçidi için HTTP dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ddbad-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="ddbad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddbad-104">SYNTAX</span></span>

### <span data-ttu-id="ddbad-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="ddbad-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ddbad-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ddbad-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddbad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddbad-107">DESCRIPTION</span></span>
<span data-ttu-id="ddbad-108">**Yeni-AzApplicationGatewayHttpListener** cmdlet 'ı bir Azure uygulama ağ GEÇIDI için http dinleyicisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ddbad-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="ddbad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddbad-109">EXAMPLES</span></span>

### <span data-ttu-id="ddbad-110">Örnek 1: HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ddbad-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="ddbad-111">Bu komut Listener01 adlı bir HTTP dinleyicisi oluşturur ve sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="ddbad-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="ddbad-112">Örnek 2: SSL ile HTTP dinleyicisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ddbad-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="ddbad-113">Bu komut SSL boşaltması kullanan bir HTTP dinleyicisi oluşturur ve $SSLCert 01 değişkeninde SSL sertifikası sağlar.</span><span class="sxs-lookup"><span data-stu-id="ddbad-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="ddbad-114">Komut sonucu $Listener adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="ddbad-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="ddbad-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddbad-115">PARAMETERS</span></span>

### <span data-ttu-id="ddbad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbad-116">-DefaultProfile</span></span>
<span data-ttu-id="ddbad-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddbad-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddbad-118">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="ddbad-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="ddbad-119">HTTP dinleyicisi için ön uç IP yapılandırması nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddbad-120">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="ddbad-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="ddbad-121">HTTP dinleyicisi için ön uç IP yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddbad-122">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="ddbad-122">-FrontendPort</span></span>
<span data-ttu-id="ddbad-123">HTTP dinleyicisi için ön uç bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddbad-124">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="ddbad-124">-FrontendPortId</span></span>
<span data-ttu-id="ddbad-125">HTTP dinleyicisi için ön uç bağlantı noktası nesnesinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddbad-126">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="ddbad-126">-HostName</span></span>
<span data-ttu-id="ddbad-127">Uygulama ağ geçidi HTTP dinleyicisinin ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="ddbad-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="ddbad-128">-Name</span></span>
<span data-ttu-id="ddbad-129">Bu cmdlet 'in oluşturduğu HTTP dinleyicisinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ddbad-130">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ddbad-130">-Protocol</span></span>
<span data-ttu-id="ddbad-131">HTTP dinleyicisinin kullandığı protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="ddbad-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="ddbad-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="ddbad-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="ddbad-133">-SslCertificate</span></span>
<span data-ttu-id="ddbad-134">HTTP dinleyicisi için SSL sertifikası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="ddbad-135">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="ddbad-135">-SslCertificateId</span></span>
<span data-ttu-id="ddbad-136">HTTP dinleyicisi için SSL sertifikasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddbad-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="ddbad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbad-137">CommonParameters</span></span>
<span data-ttu-id="ddbad-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddbad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbad-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddbad-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbad-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddbad-140">INPUTS</span></span>

### <span data-ttu-id="ddbad-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ddbad-141">System.String</span></span>

## <span data-ttu-id="ddbad-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddbad-142">OUTPUTS</span></span>

### <span data-ttu-id="ddbad-143">Microsoft. Azure. Commands. Network. modeller. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddbad-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="ddbad-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddbad-144">NOTES</span></span>

## <span data-ttu-id="ddbad-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddbad-145">RELATED LINKS</span></span>

[<span data-ttu-id="ddbad-146">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddbad-146">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ddbad-147">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddbad-147">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ddbad-148">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddbad-148">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ddbad-149">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ddbad-149">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


