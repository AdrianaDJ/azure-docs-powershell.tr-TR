---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: 75857d2c97ace9b06e3f7cdd7f672ac35a6fe34e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918179"
---
# <span data-ttu-id="17941-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="17941-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="17941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17941-102">SYNOPSIS</span></span>
<span data-ttu-id="17941-103">Sanal ağ geçidi oluşturur</span><span class="sxs-lookup"><span data-stu-id="17941-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="17941-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17941-104">SYNTAX</span></span>

### <span data-ttu-id="17941-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17941-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17941-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="17941-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17941-107">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="17941-107">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -AadTenantUri <String>
 -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17941-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="17941-108">DESCRIPTION</span></span>
<span data-ttu-id="17941-109">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="17941-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="17941-110">**New-AzVirtualNetworkGateway** cmdlet 'ı, ad, kaynak grubu adı, konumu ve IP yapılandırmasına bağlı olarak, ağ geçidinizin nesnesini, ağ geçidi türü ve VPN, VPN türü olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17941-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="17941-111">Ağ Geçidi SKU 'SU de yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17941-111">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="17941-112">Bu ağ geçidi Noktadan siteye bağlantılarda kullanılıyorsa, istemcilere bağlanmak için adres atanacak ve ağ geçidine bağlanan VPN istemcilerinin kimlik doğrulaması için kullanılan VPN Istemcisi kök sertifikasının bulunduğu VPN Istemcisi adres havuzunu da eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="17941-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="17941-113">Ayrıca, BGP ve etkin-etkin gibi diğer özellikleri de eklemeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17941-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="17941-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17941-114">EXAMPLES</span></span>

### <span data-ttu-id="17941-115">1: sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="17941-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="17941-116">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17941-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="17941-117">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="17941-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="17941-118">2: dış RADIUS yapılandırması ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="17941-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="17941-119">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17941-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="17941-120">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="17941-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="17941-121">Ayrıca, "TestRadiusServer" adresine sahip dış bir RADIUS sunucusu da ekler.</span><span class="sxs-lookup"><span data-stu-id="17941-121">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="17941-122">Ayrıca, ağ geçidinde müşteriler tarafından belirtilen özel rotaları de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="17941-122">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="17941-123">3: P2S ayarları ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="17941-123">3: Create a Virtual Network Gateway with P2S settings</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$rootCert = New-AzVpnClientRootCertificate -Name $clientRootCertName -PublicCertData $samplePublicCertData
$vpnclientipsecpolicy = New-AzVpnClientIpsecPolicy -IpsecEncryption AES256 -IpsecIntegrity SHA256 -SALifeTimeSeconds 86471 -SADataSizeKilobytes 429496 -IkeEncryption AES256 -IkeIntegrity SHA384 -DhGroup DHGroup2 -PfsGroup PFS2

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol IkeV2 -VpnClientAddressPool 201.169.0.0/16 -VpnClientRootCertificates $rootCert -VpnClientIpsecPolicy $vpnclientipsecpolicy -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="17941-124">Yukarıdaki, bir kaynak grubu oluşturur, genel bir IP adresi ister, sanal ağ ve alt ağ oluşturun ve P2S ayarları (. VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, Vpnclientıpsecpolicy vb.) içeren bir sanal ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17941-124">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="17941-125">Ağ Geçidi, "INGILTERE Batı" kaynak grubunda "Işgal-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "VpnGw1", VPN türü "VPN" ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="17941-125">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="17941-126">VPN ayarları, bir ağ geçidinde, Ikev2 olarak ayarlanan VpnProtocol, VpnClientAddressPool olarak "201.169.0.0/16", VpnClientRootCertificate olarak ayarlanır ve nesne: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="17941-126">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="17941-127">Ayrıca, ağ geçidinde müşteriler tarafından belirtilen özel rotaları de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="17941-127">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="17941-128">4: sanal ağ geçidi 'nin VpnClient için AAD kimlik doğrulama yapılandırması ile sanal ağ geçidi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="17941-128">4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="17941-129">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17941-129">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="17941-130">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="17941-130">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="17941-131">Ayrıca, sanal ağ geçidi 'nin VpnClient için AAD kimlik doğrulama yapılandırmalarını yapılandırır: AadTenantUri, Aadıssueruri ve Aadaudıenceıd.</span><span class="sxs-lookup"><span data-stu-id="17941-131">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="17941-132">5: VpnGatewayGeneration ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="17941-132">5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="17941-133">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17941-133">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="17941-134">Ağ Geçidi, "BK Batı" adlı "VNET-Gateway" kaynak grubunun içinde "Übgw" adlı kaynak konfigürasyonda "ngwIPConfig", "VpnGw4", VPN türü "" ve VpnGatewayGeneration Generation2 etkinleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="17941-134">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="17941-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17941-135">PARAMETERS</span></span>

### <span data-ttu-id="17941-136">-Aadaudienceıd</span><span class="sxs-lookup"><span data-stu-id="17941-136">-AadAudienceId</span></span>
<span data-ttu-id="17941-137">P2S AAD kimlik doğrulama seçeneği: Aadaudienceıd.</span><span class="sxs-lookup"><span data-stu-id="17941-137">P2S AAD authentication option:AadAudienceId.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-138">-Aadıssueruri</span><span class="sxs-lookup"><span data-stu-id="17941-138">-AadIssuerUri</span></span>
<span data-ttu-id="17941-139">P2S AAD kimlik doğrulama seçeneği: Aadıssueruri.</span><span class="sxs-lookup"><span data-stu-id="17941-139">P2S AAD authentication option:AadIssuerUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-140">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="17941-140">-AadTenantUri</span></span>
<span data-ttu-id="17941-141">P2S AAD kimlik doğrulama seçeneği: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="17941-141">P2S AAD authentication option:AadTenantUri.</span></span>

```yaml
Type: System.String
Parameter Sets: AadAuthenticationConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-142">-Iş</span><span class="sxs-lookup"><span data-stu-id="17941-142">-AsJob</span></span>
<span data-ttu-id="17941-143">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="17941-143">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17941-144">-ASN</span><span class="sxs-lookup"><span data-stu-id="17941-144">-Asn</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-145">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="17941-145">-CustomRoute</span></span>
<span data-ttu-id="17941-146">Müşteri tarafından belirtilen özel rotalar adres havuzu</span><span class="sxs-lookup"><span data-stu-id="17941-146">Custom routes AddressPool specified by customer</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17941-147">-DefaultProfile</span></span>
<span data-ttu-id="17941-148">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17941-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17941-149">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="17941-149">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="17941-150">Etkin özelliği etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="17941-150">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="17941-151">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="17941-151">-EnableBgp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-152">-Force</span><span class="sxs-lookup"><span data-stu-id="17941-152">-Force</span></span>
<span data-ttu-id="17941-153">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="17941-153">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17941-154">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="17941-154">-GatewayDefaultSite</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-155">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="17941-155">-GatewaySku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3, VpnGw4, VpnGw5, VpnGw1AZ, VpnGw2AZ, VpnGw3AZ, VpnGw4AZ, VpnGw5AZ, ErGw1AZ, ErGw2AZ, ErGw3AZ

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-156">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="17941-156">-GatewayType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-157">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="17941-157">-IpConfigurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-158">-Konum</span><span class="sxs-lookup"><span data-stu-id="17941-158">-Location</span></span>

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

### <span data-ttu-id="17941-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="17941-159">-Name</span></span>

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

### <span data-ttu-id="17941-160">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="17941-160">-PeerWeight</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-161">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="17941-161">-RadiusServerAddress</span></span>
<span data-ttu-id="17941-162">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="17941-162">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-163">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="17941-163">-RadiusServerSecret</span></span>
<span data-ttu-id="17941-164">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="17941-164">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17941-165">-ResourceGroupName</span></span>

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

### <span data-ttu-id="17941-166">Etiketli</span><span class="sxs-lookup"><span data-stu-id="17941-166">-Tag</span></span>
<span data-ttu-id="17941-167">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="17941-167">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="17941-168">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="17941-168">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="17941-169">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="17941-169">-VpnClientAddressPool</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-170">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="17941-170">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="17941-171">P2S VPN istemcisi tünel protokollerinin IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="17941-171">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-172">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="17941-172">-VpnClientProtocol</span></span>
<span data-ttu-id="17941-173">P2S VPN istemci tünel protokolleri listesi</span><span class="sxs-lookup"><span data-stu-id="17941-173">The list of P2S VPN client tunneling protocols</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: SSTP, IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-174">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="17941-174">-VpnClientRevokedCertificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-175">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="17941-175">-VpnClientRootCertificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-176">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="17941-176">-VpnGatewayGeneration</span></span>
<span data-ttu-id="17941-177">Bu VirtualNetwork VPN ağ geçidi için oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="17941-177">The generation for this VirtualNetwork VPN gateway.</span></span> <span data-ttu-id="17941-178">GatewayType VPN değilse None olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="17941-178">Must be None if GatewayType is not VPN.</span></span> <span data-ttu-id="17941-179">Bu özellik, ağ geçidinin kullanım süresi boyunca değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="17941-179">Once set, this property cannot be changed over the lifetime of the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: None, Generation1, Generation2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17941-180">-VpnType</span><span class="sxs-lookup"><span data-stu-id="17941-180">-VpnType</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17941-181">-Onay</span><span class="sxs-lookup"><span data-stu-id="17941-181">-Confirm</span></span>
<span data-ttu-id="17941-182">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17941-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17941-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17941-183">-WhatIf</span></span>
<span data-ttu-id="17941-184">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17941-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17941-185">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17941-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17941-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17941-186">CommonParameters</span></span>
<span data-ttu-id="17941-187">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17941-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17941-188">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17941-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17941-189">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17941-189">INPUTS</span></span>

### <span data-ttu-id="17941-190">System. String</span><span class="sxs-lookup"><span data-stu-id="17941-190">System.String</span></span>

### <span data-ttu-id="17941-191">Microsoft. Azure. Commands. Network. model. Psvirtualnetworkgatewaynetworkservice []</span><span class="sxs-lookup"><span data-stu-id="17941-191">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="17941-192">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="17941-192">System.Boolean</span></span>

### <span data-ttu-id="17941-193">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="17941-193">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="17941-194">System. String []</span><span class="sxs-lookup"><span data-stu-id="17941-194">System.String[]</span></span>

### <span data-ttu-id="17941-195">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="17941-195">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="17941-196">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifika []</span><span class="sxs-lookup"><span data-stu-id="17941-196">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="17941-197">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="17941-197">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="17941-198">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="17941-198">System.UInt32</span></span>

### <span data-ttu-id="17941-199">System. Int32</span><span class="sxs-lookup"><span data-stu-id="17941-199">System.Int32</span></span>

### <span data-ttu-id="17941-200">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="17941-200">System.Collections.Hashtable</span></span>

### <span data-ttu-id="17941-201">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="17941-201">System.Security.SecureString</span></span>

## <span data-ttu-id="17941-202">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17941-202">OUTPUTS</span></span>

### <span data-ttu-id="17941-203">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="17941-203">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="17941-204">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17941-204">NOTES</span></span>

## <span data-ttu-id="17941-205">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17941-205">RELATED LINKS</span></span>

[<span data-ttu-id="17941-206">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="17941-206">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="17941-207">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="17941-207">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="17941-208">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="17941-208">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="17941-209">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="17941-209">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="17941-210">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="17941-210">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
