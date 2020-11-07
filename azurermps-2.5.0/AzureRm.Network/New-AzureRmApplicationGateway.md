---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1F5066C6-9756-47B4-886C-C52755809926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 73b72c6585fb4c7487b43dc99b3494cdc99bf7a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939306"
---
# <span data-ttu-id="05e4d-101">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05e4d-101">New-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="05e4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05e4d-102">SYNOPSIS</span></span>
<span data-ttu-id="05e4d-103">Uygulama ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-103">Creates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05e4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05e4d-104">SYNTAX</span></span>

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
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05e4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="05e4d-105">DESCRIPTION</span></span>
<span data-ttu-id="05e4d-106">**New-AzureRmApplicationGateway** cmdlet 'ı bir Azure Application Gateway oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-106">The **New-AzureRmApplicationGateway** cmdlet creates an Azure application gateway.</span></span>

<span data-ttu-id="05e4d-107">Uygulama ağ geçidi aşağıdakileri gerektirir:</span><span class="sxs-lookup"><span data-stu-id="05e4d-107">An application gateway requires the following:</span></span>

- <span data-ttu-id="05e4d-108">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="05e4d-108">A resource group.</span></span>
- <span data-ttu-id="05e4d-109">Sanal ağ.</span><span class="sxs-lookup"><span data-stu-id="05e4d-109">A virtual network.</span></span>
- <span data-ttu-id="05e4d-110">Arka uç sunucuların IP adreslerini içeren bir arka uç sunucu havuzu.</span><span class="sxs-lookup"><span data-stu-id="05e4d-110">A back-end server pool, containing the IP addresses of the back-end servers.</span></span>
- <span data-ttu-id="05e4d-111">Arka uç sunucu havuzu ayarları.</span><span class="sxs-lookup"><span data-stu-id="05e4d-111">Back-end server pool settings.</span></span> <span data-ttu-id="05e4d-112">Her havuzda, havuz içindeki tüm sunuculara uygulanan bağlantı noktası, protokol ve tanımlama bilgisi tabanlı benzeşim gibi ayarlar vardır.</span><span class="sxs-lookup"><span data-stu-id="05e4d-112">Each pool has settings such as port, protocol and cookie-based affinity, that are applied to all servers within the pool.</span></span>
- <span data-ttu-id="05e4d-113">Uygulama ağ geçidinde açılan IP adresleri olan ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="05e4d-113">Front-end IP addresses, which are the IP addresses opened on the application gateway.</span></span> <span data-ttu-id="05e4d-114">Ön uç IP adresi ortak bir IP adresi veya iç IP adresi olabilir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-114">A front-end IP address can be a public IP address or an internal IP address.</span></span>
- <span data-ttu-id="05e4d-115">Uygulama ağ geçidinde açık olan ortak bağlantı noktaları olan ön uç bağlantı noktaları.</span><span class="sxs-lookup"><span data-stu-id="05e4d-115">Front-end ports, which are the public ports opened on the application gateway.</span></span> <span data-ttu-id="05e4d-116">Bu bağlantı noktaları ile eşleşen trafik arka uç sunucularına yönlendirilir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-116">Traffic that hits these ports is redirected to the back-end servers.</span></span>
- <span data-ttu-id="05e4d-117">Dinleyiciyi ve arka uç sunucu havuzunu bağlayan bir istek yönlendirme kuralı.</span><span class="sxs-lookup"><span data-stu-id="05e4d-117">A request routing rule that binds the listener and the back-end server pool.</span></span> <span data-ttu-id="05e4d-118">Kural, trafiğin belirli bir dinleyiciyi ziyaret edildiğinde hangi arka uç sunucu havuzunun yönlendirilmelidir?</span><span class="sxs-lookup"><span data-stu-id="05e4d-118">The rule defines which back-end server pool the traffic should be directed to when it hits a particular listener.</span></span>

<span data-ttu-id="05e4d-119">Bir dinleyicinin ön uç bağlantı noktası, ön uç IP adresi, protokol (HTTP veya HTTPS) ve Güvenli Yuva Katmanı (SSL) sertifikası adı (SSL boşaltması yapılandırıyorsanız) bulunur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-119">A listener has a front-end port, front-end IP address, protocol (HTTP or HTTPS) and Secure Sockets Layer (SSL) certificate name (if configuring SSL offload).</span></span>

## <span data-ttu-id="05e4d-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05e4d-120">EXAMPLES</span></span>

### <span data-ttu-id="05e4d-121">Örnek 1: uygulama ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="05e4d-121">Example 1: Create an application gateway</span></span>
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

<span data-ttu-id="05e4d-122">Aşağıdaki örnekte, önce bir kaynak grubu ve bir sanal ağ oluşturularak aşağıdaki gibi bir uygulama ağ geçidi oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="05e4d-122">The following example creates an application gateway by first creating a resource group and a virtual network, as well as the following:</span></span>

- <span data-ttu-id="05e4d-123">Arka uç sunucu havuzu</span><span class="sxs-lookup"><span data-stu-id="05e4d-123">A back-end server pool</span></span>
- <span data-ttu-id="05e4d-124">Arka uç sunucu havuzu ayarları</span><span class="sxs-lookup"><span data-stu-id="05e4d-124">Back-end server pool settings</span></span>
- <span data-ttu-id="05e4d-125">Ön uç bağlantı noktaları</span><span class="sxs-lookup"><span data-stu-id="05e4d-125">Front-end ports</span></span>
- <span data-ttu-id="05e4d-126">Ön uç IP adresleri</span><span class="sxs-lookup"><span data-stu-id="05e4d-126">Front-end IP addresses</span></span>
- <span data-ttu-id="05e4d-127">İstek yönlendirme kuralı</span><span class="sxs-lookup"><span data-stu-id="05e4d-127">A request routing rule</span></span>

<span data-ttu-id="05e4d-128">Bu dört komut sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-128">These four commands create a virtual network.</span></span>
<span data-ttu-id="05e4d-129">İlk komut bir alt ağ yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-129">The first command creates a subnet configuration.</span></span>
<span data-ttu-id="05e4d-130">İkinci komut sanal bir ağ oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-130">The second command creates a virtual network.</span></span>
<span data-ttu-id="05e4d-131">Üçüncü komut, alt ağ yapılandırmasını doğrular ve dördüncü komut sanal ağın başarıyla oluşturulduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="05e4d-131">The third command verifies the subnet configuration and the fourth command verifies that the virtual network is created successfully.</span></span>

<span data-ttu-id="05e4d-132">Aşağıdaki komutlar uygulama ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-132">The following commands create the application gateway.</span></span>
<span data-ttu-id="05e4d-133">İlk komut daha önce oluşturulan alt ağ için GatewayIp01 adlı bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-133">The first command creates an IP configuration named GatewayIp01 for the subnet created previously.</span></span>
<span data-ttu-id="05e4d-134">İkinci komut, arka uç IP adresleri Pool01 adlı bir arka uç sunucu havuzu oluşturur ve havuzu $Pool değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="05e4d-134">The second command creates a back-end server pool named Pool01 with a list of back-end IP addresses and stores the pool in the $Pool variable.</span></span>
<span data-ttu-id="05e4d-135">Üçüncü komut arka uç sunucu havuzunun ayarlarını oluşturur ve $PoolSetting değişkeninde ayarları depolar.</span><span class="sxs-lookup"><span data-stu-id="05e4d-135">The third command creates the settings for the back-end server pool and stores the settings in the $PoolSetting variable.</span></span>
<span data-ttu-id="05e4d-136">İleri komutu bağlantı noktası 80 üzerinde ön uç bir bağlantı noktası oluşturur, bunu FrontEndPort01 adlandırır ve $FrontEndPort değişkeninde bağlantı noktasını depolar.</span><span class="sxs-lookup"><span data-stu-id="05e4d-136">The forth command creates a front-end port on port 80, names it FrontEndPort01, and stores the port in the $FrontEndPort variable.</span></span>
<span data-ttu-id="05e4d-137">Beşinci komut, New-Azurermpublicıpaddress kullanarak genel bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-137">The fifth command creates a public IP address by using New-AzureRmPublicIpAddress.</span></span>
<span data-ttu-id="05e4d-138">Altıncı komut $PublicIp kullanarak ön uç IP yapılandırması oluşturur, FrontEndPortConfig01 adlandırır ve $FrontEndIpConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="05e4d-138">The sixth command creates a front-end IP configuration using $PublicIp, names it FrontEndPortConfig01, and stores it in the $FrontEndIpConfig variable.</span></span>
<span data-ttu-id="05e4d-139">Yedinci komutu, önceden oluşturulmuş $FrontEndIpConfig $FrontEndPort kullanarak dinleyici oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-139">The seventh command creates a listener using the previously created $FrontEndIpConfig $FrontEndPort.</span></span>
<span data-ttu-id="05e4d-140">Sekizinci komutu dinleyici için bir kural oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-140">The eighth command creates a rule for the listener.</span></span>
<span data-ttu-id="05e4d-141">Dokuzuncu komutu STB 'yi ayarlar.</span><span class="sxs-lookup"><span data-stu-id="05e4d-141">The ninth command sets the SKU.</span></span>
<span data-ttu-id="05e4d-142">Onuncu komutu, önceki komutların kullandığı nesneleri kullanarak ağ geçidini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="05e4d-142">The tenth command creates the gateway using the objects set by the previous commands.</span></span>

## <span data-ttu-id="05e4d-143">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05e4d-143">PARAMETERS</span></span>

### <span data-ttu-id="05e4d-144">-Iş</span><span class="sxs-lookup"><span data-stu-id="05e4d-144">-AsJob</span></span>
<span data-ttu-id="05e4d-145">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="05e4d-145">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05e4d-146">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="05e4d-146">-AuthenticationCertificates</span></span>
<span data-ttu-id="05e4d-147">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-147">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-148">-Backendaddresspoir</span><span class="sxs-lookup"><span data-stu-id="05e4d-148">-BackendAddressPools</span></span>
<span data-ttu-id="05e4d-149">Uygulama ağ geçidi için arka uç adres havuzlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-149">Specifies the list of back-end address pools for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-150">-BackendHttpSettingsCollection</span><span class="sxs-lookup"><span data-stu-id="05e4d-150">-BackendHttpSettingsCollection</span></span>
<span data-ttu-id="05e4d-151">Uygulama ağ geçidi için arka uç HTTP ayarlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-151">Specifies the list of back-end HTTP settings for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e4d-152">-DefaultProfile</span></span>
<span data-ttu-id="05e4d-153">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05e4d-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05e4d-154">-Force</span><span class="sxs-lookup"><span data-stu-id="05e4d-154">-Force</span></span>
<span data-ttu-id="05e4d-155">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="05e4d-155">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05e4d-156">-Frontendıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="05e4d-156">-FrontendIPConfigurations</span></span>
<span data-ttu-id="05e4d-157">Uygulama ağ geçidi için ön uç IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-157">Specifies a list of front-end IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-158">-Frontenvseçports</span><span class="sxs-lookup"><span data-stu-id="05e4d-158">-FrontendPorts</span></span>
<span data-ttu-id="05e4d-159">Uygulama ağ geçidi için ön uç bağlantı noktalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-159">Specifies a list of front-end ports for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-160">-Gatewayıpconfigurations</span><span class="sxs-lookup"><span data-stu-id="05e4d-160">-GatewayIPConfigurations</span></span>
<span data-ttu-id="05e4d-161">Uygulama ağ geçidi için IP yapılandırmalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-161">Specifies a list of IP configurations for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-162">-HttpListeners</span><span class="sxs-lookup"><span data-stu-id="05e4d-162">-HttpListeners</span></span>
<span data-ttu-id="05e4d-163">Uygulama ağ geçidi için HTTP dinleyicilerinin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-163">Specifies a list of HTTP listeners for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-164">-Konum</span><span class="sxs-lookup"><span data-stu-id="05e4d-164">-Location</span></span>
<span data-ttu-id="05e4d-165">Uygulama ağ geçidinin oluşturulacağı bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-165">Specifies the region in which to create the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-166">-Ad</span><span class="sxs-lookup"><span data-stu-id="05e4d-166">-Name</span></span>
<span data-ttu-id="05e4d-167">Uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-167">Specifies the name of application gateway.</span></span>

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

### <span data-ttu-id="05e4d-168">-Sondaları</span><span class="sxs-lookup"><span data-stu-id="05e4d-168">-Probes</span></span>
<span data-ttu-id="05e4d-169">Uygulama ağ geçidi için yoklamı belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-169">Specifies probes for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-170">-RedirectConfigurations</span><span class="sxs-lookup"><span data-stu-id="05e4d-170">-RedirectConfigurations</span></span>
<span data-ttu-id="05e4d-171">Yönlendirme yapılandırması listesi</span><span class="sxs-lookup"><span data-stu-id="05e4d-171">The list of redirect configuration</span></span>

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

### <span data-ttu-id="05e4d-172">-RequestRoutingRules</span><span class="sxs-lookup"><span data-stu-id="05e4d-172">-RequestRoutingRules</span></span>
<span data-ttu-id="05e4d-173">Uygulama ağ geçidi için istek yönlendirme kuralları listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-173">Specifies a list of request routing rules for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e4d-174">-ResourceGroupName</span></span>
<span data-ttu-id="05e4d-175">Uygulama ağ geçidinin oluşturulacağı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-175">Specifies the name of the resource group in which to create the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-176">-SKU</span><span class="sxs-lookup"><span data-stu-id="05e4d-176">-Sku</span></span>
<span data-ttu-id="05e4d-177">Uygulama ağ geçidinin stok tutma birimini (STB) belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-177">Specifies the stock keeping unit (SKU) of the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-178">-SslCertificates</span><span class="sxs-lookup"><span data-stu-id="05e4d-178">-SslCertificates</span></span>
<span data-ttu-id="05e4d-179">Uygulama ağ geçidi için Güvenli Yuva Katmanı (SSL) sertifikalarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-179">Specifies the list of Secure Sockets Layer (SSL) certificates for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-180">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="05e4d-180">-SslPolicy</span></span>
<span data-ttu-id="05e4d-181">Uygulama ağ geçidi için bir SSL ilkesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-181">Specifies an SSL policy for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-182">Etiketli</span><span class="sxs-lookup"><span data-stu-id="05e4d-182">-Tag</span></span>
<span data-ttu-id="05e4d-183">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="05e4d-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="05e4d-184">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="05e4d-184">For example:</span></span>

<span data-ttu-id="05e4d-185">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="05e4d-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="05e4d-186">-Urlyoleşlemleri</span><span class="sxs-lookup"><span data-stu-id="05e4d-186">-UrlPathMaps</span></span>
<span data-ttu-id="05e4d-187">Uygulama ağ geçidi için URL yol eşlemelerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-187">Specifies URL path maps for the application gateway.</span></span>

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

### <span data-ttu-id="05e4d-188">-WebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="05e4d-188">-WebApplicationFirewallConfiguration</span></span>
<span data-ttu-id="05e4d-189">Web uygulaması güvenlik duvarı (WAF) yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-189">Specifies a web application firewall (WAF) configuration.</span></span> <span data-ttu-id="05e4d-190">WAF almak için Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="05e4d-190">You can use the Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration cmdlet to get a WAF.</span></span>

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

### <span data-ttu-id="05e4d-191">-Onay</span><span class="sxs-lookup"><span data-stu-id="05e4d-191">-Confirm</span></span>
<span data-ttu-id="05e4d-192">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="05e4d-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05e4d-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05e4d-193">-WhatIf</span></span>
<span data-ttu-id="05e4d-194">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="05e4d-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05e4d-195">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="05e4d-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05e4d-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e4d-196">CommonParameters</span></span>
<span data-ttu-id="05e4d-197">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05e4d-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e4d-198">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e4d-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e4d-199">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05e4d-199">INPUTS</span></span>

## <span data-ttu-id="05e4d-200">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05e4d-200">OUTPUTS</span></span>

### <span data-ttu-id="05e4d-201">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="05e4d-201">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="05e4d-202">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05e4d-202">NOTES</span></span>

## <span data-ttu-id="05e4d-203">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05e4d-203">RELATED LINKS</span></span>

[<span data-ttu-id="05e4d-204">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="05e4d-204">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="05e4d-205">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="05e4d-205">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="05e4d-206">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="05e4d-206">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="05e4d-207">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="05e4d-207">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="05e4d-208">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="05e4d-208">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="05e4d-209">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="05e4d-209">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="05e4d-210">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="05e4d-210">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="05e4d-211">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="05e4d-211">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="05e4d-212">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="05e4d-212">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="05e4d-213">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="05e4d-213">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)
