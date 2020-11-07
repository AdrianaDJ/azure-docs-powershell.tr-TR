---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 131a068faec659b8215790a1bcdc1609b3494cb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760434"
---
# <span data-ttu-id="92b8d-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92b8d-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="92b8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92b8d-102">SYNOPSIS</span></span>
<span data-ttu-id="92b8d-103">Uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-103">Creates an application gateway.</span></span>

## <span data-ttu-id="92b8d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="92b8d-104">SYNTAX</span></span>

### <span data-ttu-id="92b8d-105">Identitybyuseratandidentityid (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="92b8d-105">IdentityByUserAssignedIdentityId (Default)</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] [-UserAssignedIdentityId <String>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b8d-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="92b8d-106">SetByResourceId</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicyId <String>] [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>]
 [-EnableHttp2] [-EnableFIPS] [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b8d-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="92b8d-107">SetByResource</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92b8d-108">Identitybyıdentityobject</span><span class="sxs-lookup"><span data-stu-id="92b8d-108">IdentityByIdentityObject</span></span>
```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <PSApplicationGatewayIPConfiguration[]>
 [-SslCertificates <PSApplicationGatewaySslCertificate[]>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>]
 [-FrontendIPConfigurations <PSApplicationGatewayFrontendIPConfiguration[]>]
 -FrontendPorts <PSApplicationGatewayFrontendPort[]> [-Probes <PSApplicationGatewayProbe[]>]
 -BackendAddressPools <PSApplicationGatewayBackendAddressPool[]>
 -BackendHttpSettingsCollection <PSApplicationGatewayBackendHttpSettings[]>
 -HttpListeners <PSApplicationGatewayHttpListener[]> [-UrlPathMaps <PSApplicationGatewayUrlPathMap[]>]
 -RequestRoutingRules <PSApplicationGatewayRequestRoutingRule[]>
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet[]>]
 [-RedirectConfigurations <PSApplicationGatewayRedirectConfiguration[]>]
 [-WebApplicationFirewallConfiguration <PSApplicationGatewayWebApplicationFirewallConfiguration>]
 [-AutoscaleConfiguration <PSApplicationGatewayAutoscaleConfiguration>] [-EnableHttp2] [-EnableFIPS]
 [-Zone <String[]>] [-Tag <Hashtable>] -Identity <PSManagedServiceIdentity> [-Force] [-AsJob]
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92b8d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="92b8d-109">DESCRIPTION</span></span>
<span data-ttu-id="92b8d-110">**Yeni-AzApplicationGateway** cmdlet 'ı bir Azure Application Gateway oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-110">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>
<span data-ttu-id="92b8d-111">Uygulama ağ geçidi aşağıdakileri gerektirir:</span><span class="sxs-lookup"><span data-stu-id="92b8d-111">An application gateway requires the following:</span></span>
- <span data-ttu-id="92b8d-112">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="92b8d-112">A resource group.</span></span>
- <span data-ttu-id="92b8d-113">Sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="92b8d-113">A virtual network.</span></span>
- <span data-ttu-id="92b8d-114">Arka uç sunucuların IP adreslerini içeren bir arka uç sunucu havuzu.</span><span class="sxs-lookup"><span data-stu-id="92b8d-114">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="92b8d-115">Arka uç sunucu havuzu ayarları.</span><span class="sxs-lookup"><span data-stu-id="92b8d-115">Back-end server pool settings.</span></span> <span data-ttu-id="92b8d-116">Her havuzda, havuz içindeki tüm sunuculara uygulanan bağlantı noktası, protokol ve tanımlama bilgisi tabanlı benzeşim gibi ayarlar vardır.</span><span class="sxs-lookup"><span data-stu-id="92b8d-116">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="92b8d-117">Uygulama ağ geçidinde açılan IP adresleri olan ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="92b8d-117">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="92b8d-118">Ön uç IP adresi ortak bir IP adresi veya iç IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-118">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="92b8d-119">Uygulama ağ geçidinde açık olan ortak bağlantı noktaları olan ön uç bağlantı noktaları.</span><span class="sxs-lookup"><span data-stu-id="92b8d-119">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="92b8d-120">Bu bağlantı noktaları ile eşleşen trafik arka uç sunucularına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-120">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="92b8d-121">Dinleyiciyi ve arka uç sunucu havuzunu bağlayan bir istek yönlendirme kuralı.</span><span class="sxs-lookup"><span data-stu-id="92b8d-121">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="92b8d-122">Kural, trafiğin belirli bir dinleyiciyi ziyaret edildiğinde hangi arka uç sunucu havuzunun yönlendirilmelidir?</span><span class="sxs-lookup"><span data-stu-id="92b8d-122">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>
<span data-ttu-id="92b8d-123">Bir dinleyicinin ön uç bağlantı noktası, ön uç IP adresi, protokol (HTTP veya HTTPS) ve Güvenli Yuva Katmanı (SSL) sertifikası adı (SSL boşaltması yapılandırıyorsanız) bulunur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-123">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="92b8d-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="92b8d-124">EXAMPLES</span></span>

### <span data-ttu-id="92b8d-125">Örnek 1: uygulama ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="92b8d-125">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="92b8d-126">Aşağıdaki örnekte, önce bir kaynak grubu ve bir sanal ağ oluşturularak aşağıdaki gibi bir uygulama ağ geçidi oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="92b8d-126">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>
- <span data-ttu-id="92b8d-127">Arka uç sunucu havuzu</span><span class="sxs-lookup"><span data-stu-id="92b8d-127">A back-end server pool</span></span>
- <span data-ttu-id="92b8d-128">Arka uç sunucu havuzu ayarları</span><span class="sxs-lookup"><span data-stu-id="92b8d-128">Back-end server pool settings</span></span>
- <span data-ttu-id="92b8d-129">Ön uç bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="92b8d-129">Front-end ports</span></span>
- <span data-ttu-id="92b8d-130">Ön uç IP adresleri</span><span class="sxs-lookup"><span data-stu-id="92b8d-130">Front-end IP addresses</span></span>
- <span data-ttu-id="92b8d-131">İstek yönlendirme kuralı bu dört komut sanal ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-131">A request routing rule These four commands create a virtual network.</span></span>
<span data-ttu-id="92b8d-132">İlk komut bir alt ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-132">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="92b8d-133">İkinci komut sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-133">The second command creates a virtual network.</span></span>
<span data-ttu-id="92b8d-134">Üçüncü komut, alt ağ yapılandırmasını doğrular ve dördüncü komut sanal ağın başarıyla oluşturulduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="92b8d-134">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>
<span data-ttu-id="92b8d-135">Aşağıdaki komutlar uygulama ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-135">The following commands create the application gateway.</span></span>
<span data-ttu-id="92b8d-136">İlk komut daha önce oluşturulan alt ağ için GatewayIp01 adlı bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-136">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="92b8d-137">İkinci komut, arka uç IP adresleri Pool01 adlı bir arka uç sunucu havuzu oluşturur ve havuzu $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="92b8d-137">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="92b8d-138">Üçüncü komut arka uç sunucu havuzunun ayarlarını oluşturur ve $PoolSetting değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="92b8d-138">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="92b8d-139">İleri komutu bağlantı noktası 80 üzerinde ön uç bir bağlantı noktası oluşturur, bunu FrontEndPort01 adlandırır ve $FrontEndPort değişkeninde bağlantı noktasını depolar.</span><span class="sxs-lookup"><span data-stu-id="92b8d-139">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="92b8d-140">Beşinci komut, New-Azpublicıpaddress kullanarak genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-140">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="92b8d-141">Altıncı komut $PublicIp kullanarak ön uç IP yapılandırması oluşturur, FrontEndPortConfig01 adlandırır ve $FrontEndIpConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="92b8d-141">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="92b8d-142">Yedinci komutu, önceden oluşturulmuş $FrontEndIpConfig $FrontEndPort kullanarak dinleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-142">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="92b8d-143">Sekizinci komutu dinleyici için bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-143">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="92b8d-144">Dokuzuncu komutu STB 'yi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="92b8d-144">The ninth command sets the SKU.</span></span>
<span data-ttu-id="92b8d-145">Onuncu komutu, önceki komutların kullandığı nesneleri kullanarak ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="92b8d-145">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

### <span data-ttu-id="92b8d-146">Örnek 2: Kullanıcı tarafından atanan kimlik ile uygulama ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="92b8d-146">Example 2: Create an application gateway with UserAssigned Identity</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Identity = New-AzUserAssignedIdentity -Name "Identity01" -ResourceGroupName "ResourceGroup01" -Location "West US"
PS C:\> $AppgwIdentity = New-AzApplicationGatewayIdentity -UserAssignedIdentity $Identity.Id
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -Identity $AppgwIdentity -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

## <span data-ttu-id="92b8d-147">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="92b8d-147">PARAMETERS</span></span>

### <span data-ttu-id="92b8d-148">-Iş</span><span class="sxs-lookup"><span data-stu-id="92b8d-148">-AsJob</span></span>
<span data-ttu-id="92b8d-149">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="92b8d-149">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="92b8d-150">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="92b8d-150">-AuthenticationCertificates</span></span>
<span data-ttu-id="92b8d-151">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-151">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-152">-Otomatik ölçek yapılandırması</span><span class="sxs-lookup"><span data-stu-id="92b8d-152">-AutoscaleConfiguration</span></span>
<span data-ttu-id="92b8d-153">Otomatik ölçeklendirme yapılandırması</span><span class="sxs-lookup"><span data-stu-id="92b8d-153">Autoscale Configuration</span></span>

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

### <span data-ttu-id="92b8d-154">-Backendaddresspoir</span><span class="sxs-lookup"><span data-stu-id="92b8d-154">-BackendAddressPools</span></span>
<span data-ttu-id="92b8d-155">Uygulama ağ geçidi için arka uç adres havuzlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-155">Specifies the list of back-end address pools for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-156">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="92b8d-156">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="92b8d-157">Uygulama ağ geçidi için arka uç HTTP ayarlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-157">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-158">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="92b8d-158">-CustomErrorConfiguration</span></span>
<span data-ttu-id="92b8d-159">Uygulama ağ geçidinde müşteri hatası</span><span class="sxs-lookup"><span data-stu-id="92b8d-159">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="92b8d-160">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92b8d-160">-DefaultProfile</span></span>
<span data-ttu-id="92b8d-161">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="92b8d-161">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92b8d-162">-Enablefıps</span><span class="sxs-lookup"><span data-stu-id="92b8d-162">-EnableFIPS</span></span>
<span data-ttu-id="92b8d-163">FIPS 'nın etkin olup olmadığı.</span><span class="sxs-lookup"><span data-stu-id="92b8d-163">Whether FIPS is enabled.</span></span>

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

### <span data-ttu-id="92b8d-164">-EnableHttp2</span><span class="sxs-lookup"><span data-stu-id="92b8d-164">-EnableHttp2</span></span>
<span data-ttu-id="92b8d-165">HTTP2 etkinleştirilip etkinleştirilmeyeceğini.</span><span class="sxs-lookup"><span data-stu-id="92b8d-165">Whether HTTP2 is enabled.</span></span>

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

### <span data-ttu-id="92b8d-166">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="92b8d-166">-FirewallPolicy</span></span>
<span data-ttu-id="92b8d-167">Güvenlik duvarı yapılandırması</span><span class="sxs-lookup"><span data-stu-id="92b8d-167">Firewall configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-168">-Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="92b8d-168">-FirewallPolicyId</span></span>
<span data-ttu-id="92b8d-169">Firewallpolicyıd</span><span class="sxs-lookup"><span data-stu-id="92b8d-169">FirewallPolicyId</span></span>

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

### <span data-ttu-id="92b8d-170">-Force</span><span class="sxs-lookup"><span data-stu-id="92b8d-170">-Force</span></span>
<span data-ttu-id="92b8d-171">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="92b8d-171">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92b8d-172">-Frontendıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="92b8d-172">-FrontendIPConfigurations</span></span>
<span data-ttu-id="92b8d-173">Uygulama ağ geçidi için ön uç IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-173">Specifies a list of front-end IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-174">-Frontenvseçports</span><span class="sxs-lookup"><span data-stu-id="92b8d-174">-FrontendPorts</span></span>
<span data-ttu-id="92b8d-175">Uygulama ağ geçidi için ön uç bağlantı noktalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-175">Specifies a list of front-end ports for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-176">-Gatewayıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="92b8d-176">-GatewayIPConfigurations</span></span>
<span data-ttu-id="92b8d-177">Uygulama ağ geçidi için IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-177">Specifies a list of IP configurations for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-178">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="92b8d-178">-HttpListeners</span></span>
<span data-ttu-id="92b8d-179">Uygulama ağ geçidi için HTTP dinleyicilerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-179">Specifies a list of HTTP listeners for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-180">-Kimlik</span><span class="sxs-lookup"><span data-stu-id="92b8d-180">-Identity</span></span>
<span data-ttu-id="92b8d-181">Uygulama ağ geçidine atanacak uygulama ağ geçidi kimliği.</span><span class="sxs-lookup"><span data-stu-id="92b8d-181">Application Gateway Identity to be assigned to Application Gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: IdentityByIdentityObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-182">-Konum</span><span class="sxs-lookup"><span data-stu-id="92b8d-182">-Location</span></span>
<span data-ttu-id="92b8d-183">Uygulama ağ geçidinin oluşturulacağı bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-183">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="92b8d-184">-Ad</span><span class="sxs-lookup"><span data-stu-id="92b8d-184">-Name</span></span>
<span data-ttu-id="92b8d-185">Uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-185">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="92b8d-186">-Sondaları</span><span class="sxs-lookup"><span data-stu-id="92b8d-186">-Probes</span></span>
<span data-ttu-id="92b8d-187">Uygulama ağ geçidi için yoklamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-187">Specifies probes for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-188">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="92b8d-188">-RedirectConfigurations</span></span>
<span data-ttu-id="92b8d-189">Yönlendirme yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="92b8d-189">The list of redirect configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-190">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="92b8d-190">-RequestRoutingRules</span></span>
<span data-ttu-id="92b8d-191">Uygulama ağ geçidi için istek yönlendirme kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-191">Specifies a list of request routing rules for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92b8d-192">-ResourceGroupName</span></span>
<span data-ttu-id="92b8d-193">Uygulama ağ geçidinin oluşturulacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-193">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="92b8d-194">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="92b8d-194">-RewriteRuleSet</span></span>
<span data-ttu-id="92b8d-195">Rewriter listesi</span><span class="sxs-lookup"><span data-stu-id="92b8d-195">The list of RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-196">-SKU</span><span class="sxs-lookup"><span data-stu-id="92b8d-196">-Sku</span></span>
<span data-ttu-id="92b8d-197">Uygulama ağ geçidinin stok tutma birimini (STB) belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-197">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="92b8d-198">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="92b8d-198">-SslCertificates</span></span>
<span data-ttu-id="92b8d-199">Uygulama ağ geçidi için Güvenli Yuva Katmanı (SSL) sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-199">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-200">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="92b8d-200">-SslPolicy</span></span>
<span data-ttu-id="92b8d-201">Uygulama ağ geçidi için bir SSL ilkesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-201">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="92b8d-202">Etiketli</span><span class="sxs-lookup"><span data-stu-id="92b8d-202">-Tag</span></span>
<span data-ttu-id="92b8d-203">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="92b8d-203">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="92b8d-204">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="92b8d-204">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="92b8d-205">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="92b8d-205">-TrustedRootCertificate</span></span>
<span data-ttu-id="92b8d-206">Güvenilir kök sertifikaları listesi</span><span class="sxs-lookup"><span data-stu-id="92b8d-206">The list of trusted root certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-207">-Urlyoleşlemleri</span><span class="sxs-lookup"><span data-stu-id="92b8d-207">-UrlPathMaps</span></span>
<span data-ttu-id="92b8d-208">Uygulama ağ geçidi için URL yol eşlemelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-208">Specifies URL path maps for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-209">-Useratandidentityıd</span><span class="sxs-lookup"><span data-stu-id="92b8d-209">-UserAssignedIdentityId</span></span>
<span data-ttu-id="92b8d-210">Uygulama ağ geçidine atanacak Kullanıcı tarafından atanan kimliğin RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="92b8d-210">ResourceId of the user assigned identity to be assigned to Application Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: IdentityByUserAssignedIdentityId
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-211">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="92b8d-211">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="92b8d-212">Web uygulaması güvenlik duvarı (WAF) yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-212">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="92b8d-213">WAF almak için Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="92b8d-213">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="92b8d-214">-Bölge</span><span class="sxs-lookup"><span data-stu-id="92b8d-214">-Zone</span></span>
<span data-ttu-id="92b8d-215">Uygulama ağ geçidinin nereden gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="92b8d-215">A list of availability zones denoting where the application gateway needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92b8d-216">-Onay</span><span class="sxs-lookup"><span data-stu-id="92b8d-216">-Confirm</span></span>
<span data-ttu-id="92b8d-217">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="92b8d-217">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92b8d-218">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92b8d-218">-WhatIf</span></span>
<span data-ttu-id="92b8d-219">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="92b8d-219">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92b8d-220">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="92b8d-220">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92b8d-221">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92b8d-221">CommonParameters</span></span>
<span data-ttu-id="92b8d-222">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="92b8d-222">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92b8d-223">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92b8d-223">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92b8d-224">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="92b8d-224">INPUTS</span></span>

### <span data-ttu-id="92b8d-225">System. String</span><span class="sxs-lookup"><span data-stu-id="92b8d-225">System.String</span></span>

### <span data-ttu-id="92b8d-226">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="92b8d-226">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

### <span data-ttu-id="92b8d-227">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="92b8d-227">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

### <span data-ttu-id="92b8d-228">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="92b8d-228">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration[]</span></span>

### <span data-ttu-id="92b8d-229">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewaySslCertificate []</span><span class="sxs-lookup"><span data-stu-id="92b8d-229">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate[]</span></span>

### <span data-ttu-id="92b8d-230">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAuthenticationCertificate []</span><span class="sxs-lookup"><span data-stu-id="92b8d-230">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]</span></span>

### <span data-ttu-id="92b8d-231">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayTrustedRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="92b8d-231">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]</span></span>

### <span data-ttu-id="92b8d-232">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="92b8d-232">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="92b8d-233">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayFrontendPort []</span><span class="sxs-lookup"><span data-stu-id="92b8d-233">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort[]</span></span>

### <span data-ttu-id="92b8d-234">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe []</span><span class="sxs-lookup"><span data-stu-id="92b8d-234">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe[]</span></span>

### <span data-ttu-id="92b8d-235">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="92b8d-235">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="92b8d-236">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings []</span><span class="sxs-lookup"><span data-stu-id="92b8d-236">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings[]</span></span>

### <span data-ttu-id="92b8d-237">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayHttpListener []</span><span class="sxs-lookup"><span data-stu-id="92b8d-237">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener[]</span></span>

### <span data-ttu-id="92b8d-238">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayUrlPathMap []</span><span class="sxs-lookup"><span data-stu-id="92b8d-238">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap[]</span></span>

### <span data-ttu-id="92b8d-239">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRequestRoutingRule []</span><span class="sxs-lookup"><span data-stu-id="92b8d-239">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule[]</span></span>

### <span data-ttu-id="92b8d-240">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRewriteRuleSet []</span><span class="sxs-lookup"><span data-stu-id="92b8d-240">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet[]</span></span>

### <span data-ttu-id="92b8d-241">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayRedirectConfiguration []</span><span class="sxs-lookup"><span data-stu-id="92b8d-241">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration[]</span></span>

### <span data-ttu-id="92b8d-242">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="92b8d-242">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

### <span data-ttu-id="92b8d-243">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="92b8d-243">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

### <span data-ttu-id="92b8d-244">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="92b8d-244">System.Collections.Hashtable</span></span>

## <span data-ttu-id="92b8d-245">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="92b8d-245">OUTPUTS</span></span>

### <span data-ttu-id="92b8d-246">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="92b8d-246">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="92b8d-247">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="92b8d-247">NOTES</span></span>

## <span data-ttu-id="92b8d-248">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="92b8d-248">RELATED LINKS</span></span>

[<span data-ttu-id="92b8d-249">Yeni-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="92b8d-249">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="92b8d-250">Yeni-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="92b8d-250">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="92b8d-251">Yeni-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="92b8d-251">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="92b8d-252">Yeni-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="92b8d-252">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="92b8d-253">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="92b8d-253">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="92b8d-254">Yeni-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="92b8d-254">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="92b8d-255">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="92b8d-255">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="92b8d-256">Yeni-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="92b8d-256">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="92b8d-257">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="92b8d-257">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="92b8d-258">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="92b8d-258">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
