---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGateway.md
ms.openlocfilehash: b6a7854d3ddf3c3d444418e08717577a8a2ac172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763101"
---
# <span data-ttu-id="4c7f6-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c7f6-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="4c7f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7f6-103">Uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c7f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c7f6-104">SYNTAX</span></span>

```
New-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> -Location <String>
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
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c7f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c7f6-105">DESCRIPTION</span></span>
<span data-ttu-id="4c7f6-106">**New-AzureRmApplicationGateway** cmdlet 'ı bir Azure Application Gateway oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="4c7f6-107">Uygulama ağ geçidi aşağıdakileri gerektirir:</span><span class="sxs-lookup"><span data-stu-id="4c7f6-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="4c7f6-108">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-108">A resource group.</span></span>
- <span data-ttu-id="4c7f6-109">Sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-109">A virtual network.</span></span>
- <span data-ttu-id="4c7f6-110">Arka uç sunucuların IP adreslerini içeren bir arka uç sunucu havuzu.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="4c7f6-111">Arka uç sunucu havuzu ayarları.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-111">Back-end server pool settings.</span></span> <span data-ttu-id="4c7f6-112">Her havuzda, havuz içindeki tüm sunuculara uygulanan bağlantı noktası, protokol ve tanımlama bilgisi tabanlı benzeşim gibi ayarlar vardır.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="4c7f6-113">Uygulama ağ geçidinde açılan IP adresleri olan ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="4c7f6-114">Ön uç IP adresi ortak bir IP adresi veya iç IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="4c7f6-115">Uygulama ağ geçidinde açık olan ortak bağlantı noktaları olan ön uç bağlantı noktaları.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="4c7f6-116">Bu bağlantı noktaları ile eşleşen trafik arka uç sunucularına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="4c7f6-117">Dinleyiciyi ve arka uç sunucu havuzunu bağlayan bir istek yönlendirme kuralı.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="4c7f6-118">Kural, trafiğin belirli bir dinleyiciyi ziyaret edildiğinde hangi arka uç sunucu havuzunun yönlendirilmelidir?</span><span class="sxs-lookup"><span data-stu-id="4c7f6-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="4c7f6-119">Bir dinleyicinin ön uç bağlantı noktası, ön uç IP adresi, protokol (HTTP veya HTTPS) ve Güvenli Yuva Katmanı (SSL) sertifikası adı (SSL boşaltması yapılandırıyorsanız) bulunur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="4c7f6-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c7f6-120">EXAMPLES</span></span>

### <span data-ttu-id="4c7f6-121">Örnek 1: uygulama ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4c7f6-121">Example 1: Create an application gateway</span></span>
```
PS C:\>$ResourceGroup = New-AzureRmResourceGroup -Name "ResourceGroup01" -Location "West US" -Tag @{Name = "Department"; Value = "Marketing"} PS C:\>$Subnet = New-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -AddressPrefix 10.0.0.0/24
PS C:\> $VNet = New-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01" -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $Subnet
PS C:\> $VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name $Subnet01 -VirtualNetwork $VNet PS C:\>$GatewayIPconfig = New-AzureRmApplicationGatewayIPConfiguration -Name "GatewayIp01" -Subnet $Subnet
PS C:\> $Pool = New-AzureRmApplicationGatewayBackendAddressPool -Name "Pool01" -BackendIPAddresses 10.10.10.1, 10.10.10.2, 10.10.10.3
PS C:\> $PoolSetting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "PoolSetting01"  -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01"  -Port 80
# Create a public IP address
PS C:\> $PublicIp = New-AzureRmPublicIpAddress -ResourceGroupName "ResourceGroup01" -Name $PublicIpName -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $FrontEndIpConfig = New-AzureRmApplicationGatewayFrontendIPConfig -Name "FrontEndConfig01" -PublicIPAddress $PublicIp
PS C:\> $Listener = New-AzureRmApplicationGatewayHttpListener -Name $listenerName  -Protocol "Http" -FrontendIpConfiguration $FrontEndIpConfig -FrontendPort $ FrontEndPort
PS C:\> $Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType basic -BackendHttpSettings $PoolSetting -HttpListener $Listener -BackendAddressPool $Pool
PS C:\> $Sku = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier Standard -Capacity 2
PS C:\> $Gateway = New-AzureRmApplicationGateway -Name "AppGateway01" -ResourceGroupName "ResourceGroup01" -Location "West US" -BackendAddressPools $Pool -BackendHttpSettingsCollection $PoolSetting -FrontendIpConfigurations $FrontEndIpConfig  -GatewayIpConfigurations $GatewayIpConfig -FrontendPorts $FrontEndPort -HttpListeners $Listener -RequestRoutingRules $Rule -Sku $Sku
```

<span data-ttu-id="4c7f6-122">Aşağıdaki örnekte, önce bir kaynak grubu ve bir sanal ağ oluşturularak aşağıdaki gibi bir uygulama ağ geçidi oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="4c7f6-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="4c7f6-123">Arka uç sunucu havuzu</span><span class="sxs-lookup"><span data-stu-id="4c7f6-123">A back-end server pool</span></span>
- <span data-ttu-id="4c7f6-124">Arka uç sunucu havuzu ayarları</span><span class="sxs-lookup"><span data-stu-id="4c7f6-124">Back-end server pool settings</span></span>
- <span data-ttu-id="4c7f6-125">Ön uç bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="4c7f6-125">Front-end ports</span></span>
- <span data-ttu-id="4c7f6-126">Ön uç IP adresleri</span><span class="sxs-lookup"><span data-stu-id="4c7f6-126">Front-end IP addresses</span></span>
- <span data-ttu-id="4c7f6-127">İstek yönlendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="4c7f6-127">A request routing rule</span></span>

<span data-ttu-id="4c7f6-128">Bu dört komut sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="4c7f6-129">İlk komut bir alt ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="4c7f6-130">İkinci komut sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="4c7f6-131">Üçüncü komut, alt ağ yapılandırmasını doğrular ve dördüncü komut sanal ağın başarıyla oluşturulduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="4c7f6-132">Aşağıdaki komutlar uygulama ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="4c7f6-133">İlk komut daha önce oluşturulan alt ağ için GatewayIp01 adlı bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="4c7f6-134">İkinci komut, arka uç IP adresleri Pool01 adlı bir arka uç sunucu havuzu oluşturur ve havuzu $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="4c7f6-135">Üçüncü komut arka uç sunucu havuzunun ayarlarını oluşturur ve $PoolSetting değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="4c7f6-136">İleri komutu bağlantı noktası 80 üzerinde ön uç bir bağlantı noktası oluşturur, bunu FrontEndPort01 adlandırır ve $FrontEndPort değişkeninde bağlantı noktasını depolar.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="4c7f6-137">Beşinci komut, New-Azurermpublicıpaddress kullanarak genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="4c7f6-138">Altıncı komut $PublicIp kullanarak ön uç IP yapılandırması oluşturur, FrontEndPortConfig01 adlandırır ve $FrontEndIpConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="4c7f6-139">Yedinci komutu, önceden oluşturulmuş $FrontEndIpConfig $FrontEndPort kullanarak dinleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="4c7f6-140">Sekizinci komutu dinleyici için bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="4c7f6-141">Dokuzuncu komutu STB 'yi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="4c7f6-142">Onuncu komutu, önceki komutların kullandığı nesneleri kullanarak ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="4c7f6-143">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c7f6-143">PARAMETERS</span></span>

### <span data-ttu-id="4c7f6-144">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="4c7f6-144">-AuthenticationCertificates</span></span>
<span data-ttu-id="4c7f6-145">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-145">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-146">-Backendaddresspoir</span><span class="sxs-lookup"><span data-stu-id="4c7f6-146">-BackendAddressPools</span></span>
<span data-ttu-id="4c7f6-147">Uygulama ağ geçidi için arka uç adres havuzlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-147">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-148">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="4c7f6-148">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="4c7f6-149">Uygulama ağ geçidi için arka uç HTTP ayarlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-149">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-150">-Force</span><span class="sxs-lookup"><span data-stu-id="4c7f6-150">-Force</span></span>
<span data-ttu-id="4c7f6-151">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-151">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4c7f6-152">-Frontendıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="4c7f6-152">-FrontendIPConfigurations</span></span>
<span data-ttu-id="4c7f6-153">Uygulama ağ geçidi için ön uç IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-153">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-154">-Frontenvseçports</span><span class="sxs-lookup"><span data-stu-id="4c7f6-154">-FrontendPorts</span></span>
<span data-ttu-id="4c7f6-155">Uygulama ağ geçidi için ön uç bağlantı noktalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-155">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-156">-Gatewayıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="4c7f6-156">-GatewayIPConfigurations</span></span>
<span data-ttu-id="4c7f6-157">Uygulama ağ geçidi için IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-157">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-158">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="4c7f6-158">-HttpListeners</span></span>
<span data-ttu-id="4c7f6-159">Uygulama ağ geçidi için HTTP dinleyicilerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-159">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-160">-Konum</span><span class="sxs-lookup"><span data-stu-id="4c7f6-160">-Location</span></span>
<span data-ttu-id="4c7f6-161">Uygulama ağ geçidinin oluşturulacağı bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-161">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-162">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c7f6-162">-Name</span></span>
<span data-ttu-id="4c7f6-163">Uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-163">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-164">-Sondaları</span><span class="sxs-lookup"><span data-stu-id="4c7f6-164">-Probes</span></span>
<span data-ttu-id="4c7f6-165">Uygulama ağ geçidi için yoklamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-165">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-166">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="4c7f6-166">-RedirectConfigurations</span></span>
<span data-ttu-id="4c7f6-167">Yönlendirme yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="4c7f6-167">The list of redirect configuration</span></span>

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

### <span data-ttu-id="4c7f6-168">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="4c7f6-168">-RequestRoutingRules</span></span>
<span data-ttu-id="4c7f6-169">Uygulama ağ geçidi için istek yönlendirme kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-169">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c7f6-170">-ResourceGroupName</span></span>
<span data-ttu-id="4c7f6-171">Uygulama ağ geçidinin oluşturulacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-171">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-172">-SKU</span><span class="sxs-lookup"><span data-stu-id="4c7f6-172">-Sku</span></span>
<span data-ttu-id="4c7f6-173">Uygulama ağ geçidinin stok tutma birimini (STB) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-173">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-174">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="4c7f6-174">-SslCertificates</span></span>
<span data-ttu-id="4c7f6-175">Uygulama ağ geçidi için Güvenli Yuva Katmanı (SSL) sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-175">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-176">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="4c7f6-176">-SslPolicy</span></span>
<span data-ttu-id="4c7f6-177">Uygulama ağ geçidi için bir SSL ilkesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-177">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-178">Etiketli</span><span class="sxs-lookup"><span data-stu-id="4c7f6-178">-Tag</span></span>
<span data-ttu-id="4c7f6-179">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4c7f6-180">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4c7f6-180">For example:</span></span>

<span data-ttu-id="4c7f6-181">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4c7f6-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4c7f6-182">-Urlyoleşlemleri</span><span class="sxs-lookup"><span data-stu-id="4c7f6-182">-UrlPathMaps</span></span>
<span data-ttu-id="4c7f6-183">Uygulama ağ geçidi için URL yol eşlemelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-183">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="4c7f6-184">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c7f6-184">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="4c7f6-185">Web uygulaması güvenlik duvarı (WAF) yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-185">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="4c7f6-186">WAF almak için Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-186">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="4c7f6-187">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c7f6-187">-Confirm</span></span>
<span data-ttu-id="4c7f6-188">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c7f6-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c7f6-189">-WhatIf</span></span>
<span data-ttu-id="4c7f6-190">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c7f6-191">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c7f6-192">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7f6-192">-DefaultProfile</span></span>
<span data-ttu-id="4c7f6-193">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-193">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c7f6-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7f6-194">CommonParameters</span></span>
<span data-ttu-id="4c7f6-195">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c7f6-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c7f6-196">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c7f6-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7f6-197">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c7f6-197">INPUTS</span></span>

## <span data-ttu-id="4c7f6-198">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c7f6-198">OUTPUTS</span></span>

### <span data-ttu-id="4c7f6-199">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c7f6-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c7f6-200">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c7f6-200">NOTES</span></span>

## <span data-ttu-id="4c7f6-201">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c7f6-201">RELATED LINKS</span></span>

[<span data-ttu-id="4c7f6-202">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4c7f6-202">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4c7f6-203">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4c7f6-203">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="4c7f6-204">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="4c7f6-204">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="4c7f6-205">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4c7f6-205">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4c7f6-206">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="4c7f6-206">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="4c7f6-207">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c7f6-207">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="4c7f6-208">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4c7f6-208">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4c7f6-209">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="4c7f6-209">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="4c7f6-210">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4c7f6-210">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="4c7f6-211">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="4c7f6-211">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
