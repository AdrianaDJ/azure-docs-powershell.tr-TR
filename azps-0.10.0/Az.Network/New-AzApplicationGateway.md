---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGateway.md
ms.openlocfilehash: 1945ceb84f6ccc9af38f4336ab12b01e0021f337
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935448"
---
# <span data-ttu-id="21f3a-101">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21f3a-101">New-AzApplicationGateway</span></span>

## <span data-ttu-id="21f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="21f3a-103">Uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-103">Creates an application gateway.</span></span>

## <span data-ttu-id="21f3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21f3a-104">SYNTAX</span></span>

```
New-AzApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
 -Sku <PSApplicationGatewaySku> [-SslPolicy <PSApplicationGatewaySslPolicy>]
 -GatewayIPConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration]>
 [-SslCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate]>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
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
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21f3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="21f3a-106">**Yeni-AzApplicationGateway** cmdlet 'ı bir Azure Application Gateway oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-106">The **New-AzApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="21f3a-107">Uygulama ağ geçidi aşağıdakileri gerektirir:</span><span class="sxs-lookup"><span data-stu-id="21f3a-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="21f3a-108">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="21f3a-108">A resource group.</span></span>
- <span data-ttu-id="21f3a-109">Sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="21f3a-109">A virtual network.</span></span>
- <span data-ttu-id="21f3a-110">Arka uç sunucuların IP adreslerini içeren bir arka uç sunucu havuzu.</span><span class="sxs-lookup"><span data-stu-id="21f3a-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="21f3a-111">Arka uç sunucu havuzu ayarları.</span><span class="sxs-lookup"><span data-stu-id="21f3a-111">Back-end server pool settings.</span></span> <span data-ttu-id="21f3a-112">Her havuzda, havuz içindeki tüm sunuculara uygulanan bağlantı noktası, protokol ve tanımlama bilgisi tabanlı benzeşim gibi ayarlar vardır.</span><span class="sxs-lookup"><span data-stu-id="21f3a-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="21f3a-113">Uygulama ağ geçidinde açılan IP adresleri olan ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="21f3a-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="21f3a-114">Ön uç IP adresi ortak bir IP adresi veya iç IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="21f3a-115">Uygulama ağ geçidinde açık olan ortak bağlantı noktaları olan ön uç bağlantı noktaları.</span><span class="sxs-lookup"><span data-stu-id="21f3a-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="21f3a-116">Bu bağlantı noktaları ile eşleşen trafik arka uç sunucularına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="21f3a-117">Dinleyiciyi ve arka uç sunucu havuzunu bağlayan bir istek yönlendirme kuralı.</span><span class="sxs-lookup"><span data-stu-id="21f3a-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="21f3a-118">Kural, trafiğin belirli bir dinleyiciyi ziyaret edildiğinde hangi arka uç sunucu havuzunun yönlendirilmelidir?</span><span class="sxs-lookup"><span data-stu-id="21f3a-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="21f3a-119">Bir dinleyicinin ön uç bağlantı noktası, ön uç IP adresi, protokol (HTTP veya HTTPS) ve Güvenli Yuva Katmanı (SSL) sertifikası adı (SSL boşaltması yapılandırıyorsanız) bulunur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="21f3a-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21f3a-120">EXAMPLES</span></span>

### <span data-ttu-id="21f3a-121">Örnek 1: uygulama ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="21f3a-121">Example 1: Create an application gateway</span></span>
```
PS C:\> $ResourceGroup = New-AzResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} 
PS C:\> $Subnet = New-AzVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet 
PS C:\> $GatewayIPconfig = New-AzApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzApplicationGatewayBackendHttpSetting -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name "PublicIpName01" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "ListenerName01"  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $FrontEndPort
PS C:\> $Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="21f3a-122">Aşağıdaki örnekte, önce bir kaynak grubu ve bir sanal ağ oluşturularak aşağıdaki gibi bir uygulama ağ geçidi oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="21f3a-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="21f3a-123">Arka uç sunucu havuzu</span><span class="sxs-lookup"><span data-stu-id="21f3a-123">A back-end server pool</span></span>
- <span data-ttu-id="21f3a-124">Arka uç sunucu havuzu ayarları</span><span class="sxs-lookup"><span data-stu-id="21f3a-124">Back-end server pool settings</span></span>
- <span data-ttu-id="21f3a-125">Ön uç bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="21f3a-125">Front-end ports</span></span>
- <span data-ttu-id="21f3a-126">Ön uç IP adresleri</span><span class="sxs-lookup"><span data-stu-id="21f3a-126">Front-end IP addresses</span></span>
- <span data-ttu-id="21f3a-127">İstek yönlendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="21f3a-127">A request routing rule</span></span>

<span data-ttu-id="21f3a-128">Bu dört komut sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="21f3a-129">İlk komut bir alt ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="21f3a-130">İkinci komut sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="21f3a-131">Üçüncü komut, alt ağ yapılandırmasını doğrular ve dördüncü komut sanal ağın başarıyla oluşturulduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="21f3a-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="21f3a-132">Aşağıdaki komutlar uygulama ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="21f3a-133">İlk komut daha önce oluşturulan alt ağ için GatewayIp01 adlı bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="21f3a-134">İkinci komut, arka uç IP adresleri Pool01 adlı bir arka uç sunucu havuzu oluşturur ve havuzu $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="21f3a-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="21f3a-135">Üçüncü komut arka uç sunucu havuzunun ayarlarını oluşturur ve $PoolSetting değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="21f3a-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="21f3a-136">İleri komutu bağlantı noktası 80 üzerinde ön uç bir bağlantı noktası oluşturur, bunu FrontEndPort01 adlandırır ve $FrontEndPort değişkeninde bağlantı noktasını depolar.</span><span class="sxs-lookup"><span data-stu-id="21f3a-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="21f3a-137">Beşinci komut, New-Azpublicıpaddress kullanarak genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-137">The fifth command creates a public IP address by using New-AzPublicIpAddress.</span></span>
<span data-ttu-id="21f3a-138">Altıncı komut $PublicIp kullanarak ön uç IP yapılandırması oluşturur, FrontEndPortConfig01 adlandırır ve $FrontEndIpConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="21f3a-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="21f3a-139">Yedinci komutu, önceden oluşturulmuş $FrontEndIpConfig $FrontEndPort kullanarak dinleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="21f3a-140">Sekizinci komutu dinleyici için bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="21f3a-141">Dokuzuncu komutu STB 'yi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="21f3a-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="21f3a-142">Onuncu komutu, önceki komutların kullandığı nesneleri kullanarak ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21f3a-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="21f3a-143">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21f3a-143">PARAMETERS</span></span>

### <span data-ttu-id="21f3a-144">-Iş</span><span class="sxs-lookup"><span data-stu-id="21f3a-144">-AsJob</span></span>
<span data-ttu-id="21f3a-145">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="21f3a-145">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="21f3a-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="21f3a-147">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-147">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-148">-Backendaddresspoir</span><span class="sxs-lookup"><span data-stu-id="21f3a-148">-BackendAddressPools</span></span>
<span data-ttu-id="21f3a-149">Uygulama ağ geçidi için arka uç adres havuzlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-149">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="21f3a-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="21f3a-151">Uygulama ağ geçidi için arka uç HTTP ayarlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f3a-152">-DefaultProfile</span></span>
<span data-ttu-id="21f3a-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21f3a-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21f3a-154">-Force</span><span class="sxs-lookup"><span data-stu-id="21f3a-154">-Force</span></span>
<span data-ttu-id="21f3a-155">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="21f3a-155">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-156">-Frontendıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="21f3a-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="21f3a-157">Uygulama ağ geçidi için ön uç IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-158">-Frontenvseçports</span><span class="sxs-lookup"><span data-stu-id="21f3a-158">-FrontendPorts</span></span>
<span data-ttu-id="21f3a-159">Uygulama ağ geçidi için ön uç bağlantı noktalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-159">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-160">-Gatewayıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="21f3a-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="21f3a-161">Uygulama ağ geçidi için IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-161">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="21f3a-162">-HttpListeners</span></span>
<span data-ttu-id="21f3a-163">Uygulama ağ geçidi için HTTP dinleyicilerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-164">-Konum</span><span class="sxs-lookup"><span data-stu-id="21f3a-164">-Location</span></span>
<span data-ttu-id="21f3a-165">Uygulama ağ geçidinin oluşturulacağı bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-165">Specifies the region in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-166">-Ad</span><span class="sxs-lookup"><span data-stu-id="21f3a-166">-Name</span></span>
<span data-ttu-id="21f3a-167">Uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-167">Specifies the name of application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-168">-Sondaları</span><span class="sxs-lookup"><span data-stu-id="21f3a-168">-Probes</span></span>
<span data-ttu-id="21f3a-169">Uygulama ağ geçidi için yoklamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-169">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="21f3a-170">-RedirectConfigurations</span></span>
<span data-ttu-id="21f3a-171">Yönlendirme yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="21f3a-171">The list of redirect configuration</span></span>

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

### <span data-ttu-id="21f3a-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="21f3a-172">-RequestRoutingRules</span></span>
<span data-ttu-id="21f3a-173">Uygulama ağ geçidi için istek yönlendirme kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-173">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f3a-174">-ResourceGroupName</span></span>
<span data-ttu-id="21f3a-175">Uygulama ağ geçidinin oluşturulacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-176">-SKU</span><span class="sxs-lookup"><span data-stu-id="21f3a-176">-Sku</span></span>
<span data-ttu-id="21f3a-177">Uygulama ağ geçidinin stok tutma birimini (STB) belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySku
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="21f3a-178">-SslCertificates</span></span>
<span data-ttu-id="21f3a-179">Uygulama ağ geçidi için Güvenli Yuva Katmanı (SSL) sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="21f3a-180">-SslPolicy</span></span>
<span data-ttu-id="21f3a-181">Uygulama ağ geçidi için bir SSL ilkesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-181">Specifies an SSL policy for the application gateway.</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-182">Etiketli</span><span class="sxs-lookup"><span data-stu-id="21f3a-182">-Tag</span></span>
<span data-ttu-id="21f3a-183">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="21f3a-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="21f3a-184">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="21f3a-184">For example:</span></span>

<span data-ttu-id="21f3a-185">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="21f3a-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-186">-Urlyoleşlemleri</span><span class="sxs-lookup"><span data-stu-id="21f3a-186">-UrlPathMaps</span></span>
<span data-ttu-id="21f3a-187">Uygulama ağ geçidi için URL yol eşlemelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-187">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="21f3a-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="21f3a-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="21f3a-189">Web uygulaması güvenlik duvarı (WAF) yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="21f3a-190">WAF almak için Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="21f3a-190">You can use the Get-AzApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

```yaml
Type: PSApplicationGatewayWebApplicationFirewallConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-191">-Onay</span><span class="sxs-lookup"><span data-stu-id="21f3a-191">-Confirm</span></span>
<span data-ttu-id="21f3a-192">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21f3a-192">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f3a-193">-WhatIf</span></span>
<span data-ttu-id="21f3a-194">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21f3a-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f3a-195">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21f3a-195">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21f3a-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f3a-196">CommonParameters</span></span>
<span data-ttu-id="21f3a-197">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21f3a-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21f3a-198">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f3a-198">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f3a-199">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21f3a-199">INPUTS</span></span>

## <span data-ttu-id="21f3a-200">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21f3a-200">OUTPUTS</span></span>

### <span data-ttu-id="21f3a-201">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21f3a-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="21f3a-202">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21f3a-202">NOTES</span></span>

## <span data-ttu-id="21f3a-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21f3a-203">RELATED LINKS</span></span>

[<span data-ttu-id="21f3a-204">Yeni-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21f3a-204">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="21f3a-205">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="21f3a-205">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="21f3a-206">Yeni-Azapplicationgatewayfrontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="21f3a-206">New-AzApplicationGatewayFrontendIPConfig</span></span>](./New-AzApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="21f3a-207">Yeni-Azapplicationgatewayfrontenvseçport</span><span class="sxs-lookup"><span data-stu-id="21f3a-207">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="21f3a-208">Yeni-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="21f3a-208">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="21f3a-209">Yeni-Azapplicationgatewayıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="21f3a-209">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="21f3a-210">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="21f3a-210">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="21f3a-211">Yeni-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="21f3a-211">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="21f3a-212">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="21f3a-212">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="21f3a-213">New-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="21f3a-213">New-AzVirtualNetworkSubnetConfig</span></span>](./New-AzVirtualNetworkSubnetConfig.md)
