---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: bda8ce00d316d57522bb307518c535c591e7b602
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940129"
---
# <span data-ttu-id="01bc9-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01bc9-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="01bc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01bc9-102">SYNOPSIS</span></span>
<span data-ttu-id="01bc9-103">Uygulama ağ geçidine HTTP dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="01bc9-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01bc9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01bc9-104">SYNTAX</span></span>

### <span data-ttu-id="01bc9-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="01bc9-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01bc9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="01bc9-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01bc9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01bc9-107">DESCRIPTION</span></span>
<span data-ttu-id="01bc9-108">**Add-AzureRmApplicationGatewayHttpListener** cmdlet 'i uygulama ağ geçidine http dinleyicisi ekler.</span><span class="sxs-lookup"><span data-stu-id="01bc9-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="01bc9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01bc9-109">EXAMPLES</span></span>

### <span data-ttu-id="01bc9-110">Örnek 1: HTTP dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="01bc9-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="01bc9-111">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine HTTP dinleyicisini ekler.</span><span class="sxs-lookup"><span data-stu-id="01bc9-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="01bc9-112">Örnek 2: SSL ile HTTPS dinleyicisi ekleme</span><span class="sxs-lookup"><span data-stu-id="01bc9-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="01bc9-113">İlk komut uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="01bc9-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="01bc9-114">İkinci komut, uygulama ağ geçidine HTTPS protokolünü kullanan dinleyiciyi ekler.</span><span class="sxs-lookup"><span data-stu-id="01bc9-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="01bc9-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01bc9-115">PARAMETERS</span></span>

### <span data-ttu-id="01bc9-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01bc9-116">-ApplicationGateway</span></span>
<span data-ttu-id="01bc9-117">Bu cmdlet 'in HTTP dinleyicisi eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="01bc9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01bc9-118">-DefaultProfile</span></span>
<span data-ttu-id="01bc9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01bc9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01bc9-120">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="01bc9-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="01bc9-121">Uygulama ağ geçidi ön uç IP kaynağı nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-121">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="01bc9-122">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="01bc9-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="01bc9-123">Uygulama ağ geçidi ön uç IP KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="01bc9-124">-Frontenvseçport</span><span class="sxs-lookup"><span data-stu-id="01bc9-124">-FrontendPort</span></span>
<span data-ttu-id="01bc9-125">Uygulama ağ geçidi ön uç bağlantı noktası nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-125">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="01bc9-126">-Frontenvseçportıd</span><span class="sxs-lookup"><span data-stu-id="01bc9-126">-FrontendPortId</span></span>
<span data-ttu-id="01bc9-127">Uygulama ağ geçidi ön uç bağlantı noktası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="01bc9-128">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="01bc9-128">-HostName</span></span>
<span data-ttu-id="01bc9-129">Bu cmdlet 'in HTTP dinleyicisi eklediği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="01bc9-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="01bc9-130">-Name</span></span>
<span data-ttu-id="01bc9-131">Bu komutun eklediği ön uç bağlantı noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="01bc9-132">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="01bc9-132">-Protocol</span></span>
<span data-ttu-id="01bc9-133">HTTP dinleyicisi protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="01bc9-134">Hem HTTP hem de HTTPS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="01bc9-134">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="01bc9-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="01bc9-135">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="01bc9-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="01bc9-136">-SslCertificate</span></span>
<span data-ttu-id="01bc9-137">HTTP dinleyicisinin SSL sertifikasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="01bc9-138">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="01bc9-139">-Sslcertificateıd</span><span class="sxs-lookup"><span data-stu-id="01bc9-139">-SslCertificateId</span></span>
<span data-ttu-id="01bc9-140">HTTP dinleyicisinin SSL sertifikası KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="01bc9-141">HTTPS 'yi dinleyici protokolü olarak seçtiyseniz, belirtilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="01bc9-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="01bc9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bc9-142">CommonParameters</span></span>
<span data-ttu-id="01bc9-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01bc9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bc9-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01bc9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bc9-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01bc9-145">INPUTS</span></span>

### <span data-ttu-id="01bc9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="01bc9-146">System.String</span></span>

## <span data-ttu-id="01bc9-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01bc9-147">OUTPUTS</span></span>

### <span data-ttu-id="01bc9-148">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01bc9-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="01bc9-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01bc9-149">NOTES</span></span>

## <span data-ttu-id="01bc9-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01bc9-150">RELATED LINKS</span></span>

[<span data-ttu-id="01bc9-151">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01bc9-151">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="01bc9-152">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01bc9-152">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="01bc9-153">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01bc9-153">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="01bc9-154">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="01bc9-154">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


