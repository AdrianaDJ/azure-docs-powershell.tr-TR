---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: c6c3e7826b7b9c8aa80e362ad579c1875d53bbce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274354"
---
# <span data-ttu-id="7314e-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7314e-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="7314e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7314e-102">SYNOPSIS</span></span>
<span data-ttu-id="7314e-103">Sanal ağ geçidi oluşturur</span><span class="sxs-lookup"><span data-stu-id="7314e-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="7314e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7314e-104">SYNTAX</span></span>

### <span data-ttu-id="7314e-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7314e-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7314e-106">MultipleRadiusServersConfiguration</span><span class="sxs-lookup"><span data-stu-id="7314e-106">MultipleRadiusServersConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerList <PSRadiusServer[]> [-CustomRoute <String[]>] [-VpnGatewayGeneration <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7314e-107">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="7314e-107">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -RadiusServerAddress <String> -RadiusServerSecret <SecureString> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7314e-108">AadAuthenticationConfiguration</span><span class="sxs-lookup"><span data-stu-id="7314e-108">AadAuthenticationConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <PSVirtualNetworkGatewayIpConfiguration[]>] [-GatewayType <String>] [-VpnType <String>]
 [-EnableBgp <Boolean>] [-EnableActiveActiveFeature] [-EnablePrivateIpAddress] [-GatewaySku <String>]
 [-GatewayDefaultSite <PSLocalNetworkGateway>] [-VpnClientAddressPool <String[]>]
 [-VpnClientProtocol <String[]>] [-VpnClientRootCertificates <PSVpnClientRootCertificate[]>]
 [-VpnClientRevokedCertificates <PSVpnClientRevokedCertificate[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>]
 [-IpConfigurationBgpPeeringAddresses <PSIpConfigurationBgpPeeringAddress[]>] [-Tag <Hashtable>] [-Force]
 -AadTenantUri <String> -AadAudienceId <String> -AadIssuerUri <String> [-CustomRoute <String[]>]
 [-VpnGatewayGeneration <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7314e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="7314e-109">DESCRIPTION</span></span>
<span data-ttu-id="7314e-110">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="7314e-110">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="7314e-111">**New-AzVirtualNetworkGateway** cmdlet 'ı, ad, kaynak grubu adı, konumu ve IP yapılandırmasına bağlı olarak, ağ geçidinizin nesnesini, ağ geçidi türü ve VPN, VPN türü olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7314e-111">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="7314e-112">Ağ Geçidi SKU 'SU de yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7314e-112">You can also name the Gateway SKU.</span></span>
<span data-ttu-id="7314e-113">Bu ağ geçidi Noktadan siteye bağlantılarda kullanılıyorsa, istemcilere bağlanmak için adres atanacak ve ağ geçidine bağlanan VPN istemcilerinin kimlik doğrulaması için kullanılan VPN Istemcisi kök sertifikasının bulunduğu VPN Istemcisi adres havuzunu da eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7314e-113">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>
<span data-ttu-id="7314e-114">Ayrıca, BGP ve etkin-etkin gibi diğer özellikleri de eklemeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7314e-114">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="7314e-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7314e-115">EXAMPLES</span></span>

### <span data-ttu-id="7314e-116">Örnek 1: sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7314e-116">Example 1: Create a Virtual Network Gateway</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="7314e-117">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7314e-117">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7314e-118">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="7314e-118">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="7314e-119">Örnek 2: dış RADIUS yapılandırması ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7314e-119">Example 2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd -CustomRoute 192.168.0.0/24
```

<span data-ttu-id="7314e-120">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7314e-120">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7314e-121">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="7314e-121">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="7314e-122">Ayrıca, "TestRadiusServer" adresine sahip dış bir RADIUS sunucusu da ekler.</span><span class="sxs-lookup"><span data-stu-id="7314e-122">It also adds an external radius server with address "TestRadiusServer".</span></span> <span data-ttu-id="7314e-123">Ayrıca, ağ geçidinde müşteriler tarafından belirtilen özel rotaları de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7314e-123">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="7314e-124">Örnek 3: P2S ayarları ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7314e-124">Example 3: Create a Virtual Network Gateway with P2S settings</span></span>
```powershell
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

<span data-ttu-id="7314e-125">Yukarıdaki, bir kaynak grubu oluşturur, genel bir IP adresi ister, sanal ağ ve alt ağ oluşturun ve P2S ayarları (. VpnProtocol, VpnClientAddressPool, VpnClientRootCertificates, Vpnclientıpsecpolicy vb.) içeren bir sanal ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7314e-125">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway with P2S settings e.g. VpnProtocol,VpnClientAddressPool,VpnClientRootCertificates,VpnClientIpsecPolicy etc. in Azure.</span></span>
<span data-ttu-id="7314e-126">Ağ Geçidi, "INGILTERE Batı" kaynak grubunda "Işgal-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "VpnGw1", VPN türü "VPN" ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="7314e-126">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "VpnGw1."</span></span> <span data-ttu-id="7314e-127">VPN ayarları, bir ağ geçidinde, Ikev2 olarak ayarlanan VpnProtocol, VpnClientAddressPool olarak "201.169.0.0/16", VpnClientRootCertificate olarak ayarlanır ve nesne: $vpnclientipsecpolicy</span><span class="sxs-lookup"><span data-stu-id="7314e-127">Vpn settings will be set on Gateway such as VpnProtocol set as Ikev2, VpnClientAddressPool as "201.169.0.0/16", VpnClientRootCertificate set as passed one: clientRootCertName and custom vpn ipsec policy passed in object:$vpnclientipsecpolicy</span></span>  
<span data-ttu-id="7314e-128">Ayrıca, ağ geçidinde müşteriler tarafından belirtilen özel rotaları de ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7314e-128">It will also set custom routes specified by customers on gateway.</span></span>

### <span data-ttu-id="7314e-129">Örnek 4: sanal ağ geçidi 'nin VpnClient için AAD kimlik doğrulama yapılandırması ile sanal ağ geçidi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="7314e-129">Example 4: Create a Virtual Network Gateway with AAD authentication Configuration for VpnClient of virtual network gateway.</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw1" -VpnClientProtocol OpenVPN   -VpnClientAddressPool 201.169.0.0/16 -AadTenantUri "https://login.microsoftonline.com/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4" -AadIssuerUri "https://sts.windows.net/0ab2c4f4-81e6-44cc-a0b2-b3a47a1443f4/" -AadAudienceId "a21fce82-76af-45e6-8583-a08cb3b956f9"
```

<span data-ttu-id="7314e-130">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7314e-130">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7314e-131">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="7314e-131">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="7314e-132">Ayrıca, sanal ağ geçidi 'nin VpnClient için AAD kimlik doğrulama yapılandırmalarını yapılandırır: AadTenantUri, Aadıssueruri ve Aadaudıenceıd.</span><span class="sxs-lookup"><span data-stu-id="7314e-132">It also configures AAD authentication configurations: AadTenantUri, AadIssuerUri and AadAudienceId for VpnClient of virtual network gateway.</span></span>

### <span data-ttu-id="7314e-133">Örnek 5: VpnGatewayGeneration ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7314e-133">Example 5: Create a Virtual Network Gateway with VpnGatewayGeneration</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="7314e-134">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7314e-134">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7314e-135">Ağ Geçidi, "BK Batı" adlı "VNET-Gateway" kaynak grubunun içinde "Übgw" adlı kaynak konfigürasyonda "ngwIPConfig", "VpnGw4", VPN türü "" ve VpnGatewayGeneration Generation2 etkinleştirilmiş</span><span class="sxs-lookup"><span data-stu-id="7314e-135">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

### <span data-ttu-id="7314e-136">Örnek 6: ıpconfigurationbgppeeringaddresses ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7314e-136">Example 6: Create a Virtual Network Gateway with IpConfigurationBgpPeeringAddresses</span></span>
```powershell
New-AzResourceGroup -Location "UK West" -Name "resourcegroup1"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "resourcegroup1" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "resourcegroup1" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ipconfig1 -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

$ipconfigurationId1 = ngwipconfig.id
$addresslist1 = @('169.254.21.10')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1

New-AzVirtualNetworkGateway -Name gateway1 -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig -IpConfigurationBgpPeeringAddresses $gw1ipconfBgp1 -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "VpnGw4" -VpnGatewayGeneration "Generation2"
```

<span data-ttu-id="7314e-137">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7314e-137">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="7314e-138">ipconfigurationId1, ngwipconfig 'te oluşturulan ve depolanan ağ geçidi yapılandırması.</span><span class="sxs-lookup"><span data-stu-id="7314e-138">ipconfigurationId1 of gateway ipconfiguration just created and stored in ngwipconfig.</span></span>
<span data-ttu-id="7314e-139">Ağ Geçidi "resourcegroup1resourcegroup1" kaynak grubunda "" kaynak grubunda "" kaynak grubunda, "gateway1", "" gw1ipconfBgp1 ", ağ geçidi türü" VPN ", VPN türü" ", SKU" VpnGw4 "ve VpnGatewayGeneration Generation2 etkin gibi</span><span class="sxs-lookup"><span data-stu-id="7314e-139">The gateway will be called "gateway1" within the resource group "resourcegroup1resourcegroup1" in the location "UK West" with the previously created IP configurations Bgppeering address saved in the variable "gw1ipconfBgp1," the gateway type of "VPN", the vpn type "RouteBased", the sku "VpnGw4" and VpnGatewayGeneration Generation2 enabled.</span></span>

## <span data-ttu-id="7314e-140">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7314e-140">PARAMETERS</span></span>

### <span data-ttu-id="7314e-141">-Aadaudienceıd</span><span class="sxs-lookup"><span data-stu-id="7314e-141">-AadAudienceId</span></span>
<span data-ttu-id="7314e-142">P2S AAD kimlik doğrulama seçeneği: Aadaudienceıd.</span><span class="sxs-lookup"><span data-stu-id="7314e-142">P2S AAD authentication option:AadAudienceId.</span></span>

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

### <span data-ttu-id="7314e-143">-Aadıssueruri</span><span class="sxs-lookup"><span data-stu-id="7314e-143">-AadIssuerUri</span></span>
<span data-ttu-id="7314e-144">P2S AAD kimlik doğrulama seçeneği: Aadıssueruri.</span><span class="sxs-lookup"><span data-stu-id="7314e-144">P2S AAD authentication option:AadIssuerUri.</span></span>

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

### <span data-ttu-id="7314e-145">-AadTenantUri</span><span class="sxs-lookup"><span data-stu-id="7314e-145">-AadTenantUri</span></span>
<span data-ttu-id="7314e-146">P2S AAD kimlik doğrulama seçeneği: AadTenantUri.</span><span class="sxs-lookup"><span data-stu-id="7314e-146">P2S AAD authentication option:AadTenantUri.</span></span>

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

### <span data-ttu-id="7314e-147">-Iş</span><span class="sxs-lookup"><span data-stu-id="7314e-147">-AsJob</span></span>
<span data-ttu-id="7314e-148">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7314e-148">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7314e-149">-ASN</span><span class="sxs-lookup"><span data-stu-id="7314e-149">-Asn</span></span>
<span data-ttu-id="7314e-150">VPN üzerinden BGP için sanal ağ geçidinin ASN</span><span class="sxs-lookup"><span data-stu-id="7314e-150">The virtual network gateway's ASN for BGP over VPN</span></span>

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

### <span data-ttu-id="7314e-151">-CustomRoute</span><span class="sxs-lookup"><span data-stu-id="7314e-151">-CustomRoute</span></span>
<span data-ttu-id="7314e-152">Müşteri tarafından belirtilen özel rotalar adres havuzu</span><span class="sxs-lookup"><span data-stu-id="7314e-152">Custom routes AddressPool specified by customer</span></span>

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

### <span data-ttu-id="7314e-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7314e-153">-DefaultProfile</span></span>
<span data-ttu-id="7314e-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7314e-154">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7314e-155">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="7314e-155">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="7314e-156">Sanal ağ geçidinde etkin etkin özelliği etkinleştirme bayrağı</span><span class="sxs-lookup"><span data-stu-id="7314e-156">Flag to enable Active Active feature on virtual network gateway</span></span>

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

### <span data-ttu-id="7314e-157">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="7314e-157">-EnableBgp</span></span>
<span data-ttu-id="7314e-158">EnableBgp bayrağı</span><span class="sxs-lookup"><span data-stu-id="7314e-158">EnableBgp Flag</span></span>

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

### <span data-ttu-id="7314e-159">-Enableprivateıpaddress</span><span class="sxs-lookup"><span data-stu-id="7314e-159">-EnablePrivateIpAddress</span></span>
<span data-ttu-id="7314e-160">Sanal ağ geçidinde özel IPAddress 'i etkinleştirme bayrağı</span><span class="sxs-lookup"><span data-stu-id="7314e-160">Flag to enable private IPAddress on virtual network gateway</span></span>

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

### <span data-ttu-id="7314e-161">-Force</span><span class="sxs-lookup"><span data-stu-id="7314e-161">-Force</span></span>
<span data-ttu-id="7314e-162">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="7314e-162">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7314e-163">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7314e-163">-GatewayDefaultSite</span></span>
<span data-ttu-id="7314e-164">GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="7314e-164">GatewayDefaultSite</span></span>

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

### <span data-ttu-id="7314e-165">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="7314e-165">-GatewaySku</span></span>
<span data-ttu-id="7314e-166">Ağ Geçidi SKU katmanı</span><span class="sxs-lookup"><span data-stu-id="7314e-166">The Gateway Sku Tier</span></span>

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

### <span data-ttu-id="7314e-167">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="7314e-167">-GatewayType</span></span>
<span data-ttu-id="7314e-168">Bu sanal ağ geçidinin türü: VPN, ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7314e-168">The type of this virtual network gateway: Vpn, ExpressRoute</span></span>

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

### <span data-ttu-id="7314e-169">-IpConfigurationBgpPeeringAddresses</span><span class="sxs-lookup"><span data-stu-id="7314e-169">-IpConfigurationBgpPeeringAddresses</span></span>
<span data-ttu-id="7314e-170">Sanal ağ geçidi bıgpsettings için BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="7314e-170">The BgpPeeringAddresses for Virtual network gateway bgpsettings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7314e-171">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="7314e-171">-IpConfigurations</span></span>
<span data-ttu-id="7314e-172">Sanal ağ geçidi için ıpconfigurations.</span><span class="sxs-lookup"><span data-stu-id="7314e-172">The IpConfigurations for Virtual network gateway.</span></span>

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

### <span data-ttu-id="7314e-173">-Konum</span><span class="sxs-lookup"><span data-stu-id="7314e-173">-Location</span></span>
<span data-ttu-id="7314e-174">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="7314e-174">location.</span></span>

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

### <span data-ttu-id="7314e-175">-Ad</span><span class="sxs-lookup"><span data-stu-id="7314e-175">-Name</span></span>
<span data-ttu-id="7314e-176">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="7314e-176">The resource name.</span></span>

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

### <span data-ttu-id="7314e-177">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="7314e-177">-PeerWeight</span></span>
<span data-ttu-id="7314e-178">Bu sanal ağ ağ geçidinden BGP üzerinden öğrenilen yollara yapılan ağırlık</span><span class="sxs-lookup"><span data-stu-id="7314e-178">The weight added to routes learned over BGP from this virtual network gateway</span></span>

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

### <span data-ttu-id="7314e-179">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="7314e-179">-RadiusServerAddress</span></span>
<span data-ttu-id="7314e-180">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="7314e-180">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="7314e-181">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="7314e-181">-RadiusServerList</span></span>
<span data-ttu-id="7314e-182">Birden çok dış RADIUS sunucu P2S.</span><span class="sxs-lookup"><span data-stu-id="7314e-182">P2S multiple external Radius server servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: MultipleRadiusServersConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7314e-183">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="7314e-183">-RadiusServerSecret</span></span>
<span data-ttu-id="7314e-184">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="7314e-184">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="7314e-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7314e-185">-ResourceGroupName</span></span>
<span data-ttu-id="7314e-186">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7314e-186">The resource group name.</span></span>

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

### <span data-ttu-id="7314e-187">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7314e-187">-Tag</span></span>
<span data-ttu-id="7314e-188">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="7314e-188">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="7314e-189">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="7314e-189">-VpnClientAddressPool</span></span>
<span data-ttu-id="7314e-190">P2S VpnClient AddressPool</span><span class="sxs-lookup"><span data-stu-id="7314e-190">P2S VpnClient AddressPool</span></span>

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

### <span data-ttu-id="7314e-191">-Vpnclientıpsecpolicy</span><span class="sxs-lookup"><span data-stu-id="7314e-191">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="7314e-192">P2S VPN istemcisi tünel protokollerinin IPSec ilkelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="7314e-192">A list of IPSec policies for P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="7314e-193">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="7314e-193">-VpnClientProtocol</span></span>
<span data-ttu-id="7314e-194">P2S VPN istemci tünel protokolleri listesi</span><span class="sxs-lookup"><span data-stu-id="7314e-194">The list of P2S VPN client tunneling protocols</span></span>

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

### <span data-ttu-id="7314e-195">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="7314e-195">-VpnClientRevokedCertificates</span></span>
<span data-ttu-id="7314e-196">İptal edilecek VpnClientCertificates listesi.</span><span class="sxs-lookup"><span data-stu-id="7314e-196">The list of VpnClientCertificates to be revoked.</span></span>

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

### <span data-ttu-id="7314e-197">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="7314e-197">-VpnClientRootCertificates</span></span>
<span data-ttu-id="7314e-198">Eklenecek VpnClientRootCertificates listesi.</span><span class="sxs-lookup"><span data-stu-id="7314e-198">The list of VpnClientRootCertificates to be added.</span></span>

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

### <span data-ttu-id="7314e-199">-VpnGatewayGeneration</span><span class="sxs-lookup"><span data-stu-id="7314e-199">-VpnGatewayGeneration</span></span>
<span data-ttu-id="7314e-200">Bu VirtualNetwork VPN ağ geçidi için oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="7314e-200">The generation for this VirtualNetwork VPN gateway.</span></span>
<span data-ttu-id="7314e-201">GatewayType VPN değilse None olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7314e-201">Must be None if GatewayType is not VPN.</span></span>

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

### <span data-ttu-id="7314e-202">-VpnType</span><span class="sxs-lookup"><span data-stu-id="7314e-202">-VpnType</span></span>
<span data-ttu-id="7314e-203">VPN türü: PolicyBased/RouteBased</span><span class="sxs-lookup"><span data-stu-id="7314e-203">The type of the Vpn:PolicyBased/RouteBased</span></span>

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

### <span data-ttu-id="7314e-204">-Onay</span><span class="sxs-lookup"><span data-stu-id="7314e-204">-Confirm</span></span>
<span data-ttu-id="7314e-205">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7314e-205">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7314e-206">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7314e-206">-WhatIf</span></span>
<span data-ttu-id="7314e-207">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7314e-207">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7314e-208">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7314e-208">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7314e-209">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7314e-209">CommonParameters</span></span>
<span data-ttu-id="7314e-210">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7314e-210">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7314e-211">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7314e-211">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7314e-212">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7314e-212">INPUTS</span></span>

### <span data-ttu-id="7314e-213">System. String</span><span class="sxs-lookup"><span data-stu-id="7314e-213">System.String</span></span>

### <span data-ttu-id="7314e-214">Microsoft. Azure. Commands. Network. model. Psvirtualnetworkgatewaynetworkservice []</span><span class="sxs-lookup"><span data-stu-id="7314e-214">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration[]</span></span>

### <span data-ttu-id="7314e-215">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7314e-215">System.Boolean</span></span>

### <span data-ttu-id="7314e-216">Microsoft. Azure. Commands. Network. model. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7314e-216">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

### <span data-ttu-id="7314e-217">System. String []</span><span class="sxs-lookup"><span data-stu-id="7314e-217">System.String[]</span></span>

### <span data-ttu-id="7314e-218">Microsoft. Azure. Commands. Network. model. PSVpnClientRootCertificate []</span><span class="sxs-lookup"><span data-stu-id="7314e-218">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate[]</span></span>

### <span data-ttu-id="7314e-219">Microsoft. Azure. Commands. Network. model. Psvpnclientiptal edilmiş sertifika []</span><span class="sxs-lookup"><span data-stu-id="7314e-219">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate[]</span></span>

### <span data-ttu-id="7314e-220">Microsoft. Azure. Commands. Network. model. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="7314e-220">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="7314e-221">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="7314e-221">System.UInt32</span></span>

### <span data-ttu-id="7314e-222">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7314e-222">System.Int32</span></span>

### <span data-ttu-id="7314e-223">Microsoft. Azure. Commands. Network. model. PSIpConfigurationBgpPeeringAddress []</span><span class="sxs-lookup"><span data-stu-id="7314e-223">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress[]</span></span>

### <span data-ttu-id="7314e-224">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7314e-224">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7314e-225">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="7314e-225">System.Security.SecureString</span></span>

## <span data-ttu-id="7314e-226">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7314e-226">OUTPUTS</span></span>

### <span data-ttu-id="7314e-227">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7314e-227">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7314e-228">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7314e-228">NOTES</span></span>

## <span data-ttu-id="7314e-229">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7314e-229">RELATED LINKS</span></span>
