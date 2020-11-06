---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: 67da94a783d932501413008523c744f6695f6024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589474"
---
# <span data-ttu-id="eefc4-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eefc4-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="eefc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefc4-102">SYNOPSIS</span></span>
<span data-ttu-id="eefc4-103">Uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eefc4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eefc4-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-FrontendIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]>]
 -FrontendPorts <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]>
 [-Probes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]>]
 -BackendAddressPools <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>
 -BackendHttpSettingsCollection <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]>
 -HttpListeners <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]>
 [-UrlPathMaps <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]>]
 -RequestRoutingRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]>
 [-RedirectConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eefc4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eefc4-105">DESCRIPTION</span></span>
<span data-ttu-id="eefc4-106">**New-AzureRmApplicationGateway** cmdlet 'ı bir Azure Application Gateway oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="eefc4-107">Uygulama ağ geçidi aşağıdakileri gerektirir:</span><span class="sxs-lookup"><span data-stu-id="eefc4-107">An application gateway requires the following:</span></span>
- <span data-ttu-id="eefc4-108">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="eefc4-108">A resource group.</span></span>
- <span data-ttu-id="eefc4-109">Sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="eefc4-109">A virtual network.</span></span>
- <span data-ttu-id="eefc4-110">Arka uç sunucuların IP adreslerini içeren bir arka uç sunucu havuzu.</span><span class="sxs-lookup"><span data-stu-id="eefc4-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="eefc4-111">Arka uç sunucu havuzu ayarları.</span><span class="sxs-lookup"><span data-stu-id="eefc4-111">Back-end server pool settings.</span></span> <span data-ttu-id="eefc4-112">Her havuzda, havuz içindeki tüm sunuculara uygulanan bağlantı noktası, protokol ve tanımlama bilgisi tabanlı benzeşim gibi ayarlar vardır.</span><span class="sxs-lookup"><span data-stu-id="eefc4-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="eefc4-113">Uygulama ağ geçidinde açılan IP adresleri olan ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="eefc4-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="eefc4-114">Ön uç IP adresi ortak bir IP adresi veya iç IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="eefc4-115">Uygulama ağ geçidinde açık olan ortak bağlantı noktaları olan ön uç bağlantı noktaları.</span><span class="sxs-lookup"><span data-stu-id="eefc4-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="eefc4-116">Bu bağlantı noktaları ile eşleşen trafik arka uç sunucularına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="eefc4-117">Dinleyiciyi ve arka uç sunucu havuzunu bağlayan bir istek yönlendirme kuralı.</span><span class="sxs-lookup"><span data-stu-id="eefc4-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="eefc4-118">Kural, trafiğin belirli bir dinleyiciyi ziyaret edildiğinde hangi arka uç sunucu havuzunun yönlendirilmelidir?</span><span class="sxs-lookup"><span data-stu-id="eefc4-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="eefc4-119">Bir dinleyicinin ön uç bağlantı noktası, ön uç IP adresi, protokol (HTTP veya HTTPS) ve Güvenli Yuva Katmanı (SSL) sertifikası adı (SSL boşaltması yapılandırıyorsanız) bulunur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="eefc4-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eefc4-120">EXAMPLES</span></span>

### <span data-ttu-id="eefc4-121">Örnek 1: uygulama ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="eefc4-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="eefc4-122">Aşağıdaki örnekte, önce bir kaynak grubu ve bir sanal ağ oluşturularak aşağıdaki gibi bir uygulama ağ geçidi oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="eefc4-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="eefc4-123">Arka uç sunucu havuzu</span><span class="sxs-lookup"><span data-stu-id="eefc4-123">A back-end server pool</span></span>
- <span data-ttu-id="eefc4-124">Arka uç sunucu havuzu ayarları</span><span class="sxs-lookup"><span data-stu-id="eefc4-124">Back-end server pool settings</span></span>
- <span data-ttu-id="eefc4-125">Ön uç bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="eefc4-125">Front-end ports</span></span>
- <span data-ttu-id="eefc4-126">Ön uç IP adresleri</span><span class="sxs-lookup"><span data-stu-id="eefc4-126">Front-end IP addresses</span></span>
- <span data-ttu-id="eefc4-127">İstek yönlendirme kuralı bu dört komut sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-127">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="eefc4-128">İlk komut bir alt ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-128">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="eefc4-129">İkinci komut sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-129">The second command creates a virtual network.</span></span>
<span data-ttu-id="eefc4-130">Üçüncü komut, alt ağ yapılandırmasını doğrular ve dördüncü komut sanal ağın başarıyla oluşturulduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="eefc4-130">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="eefc4-131">Aşağıdaki komutlar uygulama ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-131">The following commands create the application gateway.</span></span>
<span data-ttu-id="eefc4-132">İlk komut daha önce oluşturulan alt ağ için GatewayIp01 adlı bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-132">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="eefc4-133">İkinci komut, arka uç IP adresleri Pool01 adlı bir arka uç sunucu havuzu oluşturur ve havuzu $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="eefc4-133">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="eefc4-134">Üçüncü komut arka uç sunucu havuzunun ayarlarını oluşturur ve $PoolSetting değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="eefc4-134">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="eefc4-135">İleri komutu bağlantı noktası 80 üzerinde ön uç bir bağlantı noktası oluşturur, bunu FrontEndPort01 adlandırır ve $FrontEndPort değişkeninde bağlantı noktasını depolar.</span><span class="sxs-lookup"><span data-stu-id="eefc4-135">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="eefc4-136">Beşinci komut, New-Azurermpublicıpaddress kullanarak genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-136">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="eefc4-137">Altıncı komut $PublicIp kullanarak ön uç IP yapılandırması oluşturur, FrontEndPortConfig01 adlandırır ve $FrontEndIpConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="eefc4-137">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="eefc4-138">Yedinci komutu, önceden oluşturulmuş $FrontEndIpConfig $FrontEndPort kullanarak dinleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-138">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="eefc4-139">Sekizinci komutu dinleyici için bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-139">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="eefc4-140">Dokuzuncu komutu STB 'yi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eefc4-140">The ninth command sets the SKU.</span></span>
<span data-ttu-id="eefc4-141">Onuncu komutu, önceki komutların kullandığı nesneleri kullanarak ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eefc4-141">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="eefc4-142">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eefc4-142">PARAMETERS</span></span>

### <span data-ttu-id="eefc4-143">-Iş</span><span class="sxs-lookup"><span data-stu-id="eefc4-143">-AsJob</span></span>
<span data-ttu-id="eefc4-144">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="eefc4-144">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-145">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="eefc4-145">-AuthenticationCertificates</span></span>
<span data-ttu-id="eefc4-146">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-146">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-147">-Otomatik ölçek yapılandırması</span><span class="sxs-lookup"><span data-stu-id="eefc4-147">-AutoscaleConfiguration</span></span>
<span data-ttu-id="eefc4-148">Otomatik ölçeklendirme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="eefc4-148">Autoscale Configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-149">-Backendaddresspoir</span><span class="sxs-lookup"><span data-stu-id="eefc4-149">-BackendAddressPools</span></span>
<span data-ttu-id="eefc4-150">Uygulama ağ geçidi için arka uç adres havuzlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-150">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-151">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="eefc4-151">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="eefc4-152">Uygulama ağ geçidi için arka uç HTTP ayarlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-152">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefc4-153">-DefaultProfile</span></span>
<span data-ttu-id="eefc4-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eefc4-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eefc4-155">-Enablefıps</span><span class="sxs-lookup"><span data-stu-id="eefc4-155">-EnableFIPS</span></span>
<span data-ttu-id="eefc4-156">FIPS 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="eefc4-156">Whether FIPS is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-157">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="eefc4-157">-EnableHttp2</span></span>
<span data-ttu-id="eefc4-158">HTTP2 etkinleştirilip etkinleştirilmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="eefc4-158">Whether HTTP2 is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-159">-Force</span><span class="sxs-lookup"><span data-stu-id="eefc4-159">-Force</span></span>
<span data-ttu-id="eefc4-160">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="eefc4-160">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-161">-Frontendıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="eefc4-161">-FrontendIPConfigurations</span></span>
<span data-ttu-id="eefc4-162">Uygulama ağ geçidi için ön uç IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-162">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-163">-Frontenvseçports</span><span class="sxs-lookup"><span data-stu-id="eefc4-163">-FrontendPorts</span></span>
<span data-ttu-id="eefc4-164">Uygulama ağ geçidi için ön uç bağlantı noktalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-164">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-165">-Gatewayıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="eefc4-165">-GatewayIPConfigurations</span></span>
<span data-ttu-id="eefc4-166">Uygulama ağ geçidi için IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-166">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-167">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="eefc4-167">-HttpListeners</span></span>
<span data-ttu-id="eefc4-168">Uygulama ağ geçidi için HTTP dinleyicilerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-168">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-169">-Konum</span><span class="sxs-lookup"><span data-stu-id="eefc4-169">-Location</span></span>
<span data-ttu-id="eefc4-170">Uygulama ağ geçidinin oluşturulacağı bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-170">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-171">-Ad</span><span class="sxs-lookup"><span data-stu-id="eefc4-171">-Name</span></span>
<span data-ttu-id="eefc4-172">Uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-172">Specifies the name of application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-173">-Sondaları</span><span class="sxs-lookup"><span data-stu-id="eefc4-173">-Probes</span></span>
<span data-ttu-id="eefc4-174">Uygulama ağ geçidi için yoklamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-174">Specifies probes for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-175">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="eefc4-175">-RedirectConfigurations</span></span>
<span data-ttu-id="eefc4-176">Yönlendirme yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="eefc4-176">The list of redirect configuration</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-177">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="eefc4-177">-RequestRoutingRules</span></span>
<span data-ttu-id="eefc4-178">Uygulama ağ geçidi için istek yönlendirme kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-178">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eefc4-179">-ResourceGroupName</span></span>
<span data-ttu-id="eefc4-180">Uygulama ağ geçidinin oluşturulacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-180">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-181">-SKU</span><span class="sxs-lookup"><span data-stu-id="eefc4-181">-Sku</span></span>
<span data-ttu-id="eefc4-182">Uygulama ağ geçidinin stok tutma birimini (STB) belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-182">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-183">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="eefc4-183">-SslCertificates</span></span>
<span data-ttu-id="eefc4-184">Uygulama ağ geçidi için Güvenli Yuva Katmanı (SSL) sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-184">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-185">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="eefc4-185">-SslPolicy</span></span>
<span data-ttu-id="eefc4-186">Uygulama ağ geçidi için bir SSL ilkesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-186">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-187">Etiketli</span><span class="sxs-lookup"><span data-stu-id="eefc4-187">-Tag</span></span>
<span data-ttu-id="eefc4-188">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="eefc4-188">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="eefc4-189">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="eefc4-189">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-190">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="eefc4-190">-TrustedRootCertificate</span></span>
<span data-ttu-id="eefc4-191">Güvenilir kök sertifikaları listesi</span><span class="sxs-lookup"><span data-stu-id="eefc4-191">The list of trusted root certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-192">-Urlyoleşlemleri</span><span class="sxs-lookup"><span data-stu-id="eefc4-192">-UrlPathMaps</span></span>
<span data-ttu-id="eefc4-193">Uygulama ağ geçidi için URL yol eşlemelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-193">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-194">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="eefc4-194">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="eefc4-195">Web uygulaması güvenlik duvarı (WAF) yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-195">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="eefc4-196">WAF almak için Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eefc4-196">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-197">-Bölge</span><span class="sxs-lookup"><span data-stu-id="eefc4-197">-Zone</span></span>
<span data-ttu-id="eefc4-198">Uygulama ağ geçidinin nereden gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="eefc4-198">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-199">-Onay</span><span class="sxs-lookup"><span data-stu-id="eefc4-199">-Confirm</span></span>
<span data-ttu-id="eefc4-200">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eefc4-200">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eefc4-201">-WhatIf</span></span>
<span data-ttu-id="eefc4-202">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eefc4-202">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eefc4-203">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eefc4-203">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eefc4-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefc4-204">CommonParameters</span></span>
<span data-ttu-id="eefc4-205">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eefc4-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefc4-206">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eefc4-206">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefc4-207">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eefc4-207">INPUTS</span></span>

### <span data-ttu-id="eefc4-208">System. String</span><span class="sxs-lookup"><span data-stu-id="eefc4-208">System.String</span></span>

### <span data-ttu-id="eefc4-209">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eefc4-209">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="eefc4-210">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="eefc4-210">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="eefc4-211">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-211">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-212">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-212">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-213">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-213">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-214">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendIPConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-214">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-215">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-215">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-216">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-216">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-217">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-217">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-218">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-218">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-219">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-219">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-220">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-220">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-221">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-221">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-222">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eefc4-222">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="eefc4-223">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="eefc4-223">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="eefc4-224">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="eefc4-224">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eefc4-225">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eefc4-225">OUTPUTS</span></span>

### <span data-ttu-id="eefc4-226">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eefc4-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eefc4-227">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eefc4-227">NOTES</span></span>

## <span data-ttu-id="eefc4-228">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eefc4-228">RELATED LINKS</span></span>

[<span data-ttu-id="eefc4-229">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eefc4-229">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="eefc4-230">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="eefc4-230">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="eefc4-231">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="eefc4-231">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="eefc4-232">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="eefc4-232">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="eefc4-233">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="eefc4-233">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="eefc4-234">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="eefc4-234">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="eefc4-235">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eefc4-235">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="eefc4-236">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="eefc4-236">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="eefc4-237">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eefc4-237">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="eefc4-238">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="eefc4-238">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
