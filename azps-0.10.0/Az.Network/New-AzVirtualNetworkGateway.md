---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVirtualNetworkGateway.md
ms.openlocfilehash: a19cc1484a00b60eb27723621e05aa67634e8732
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935352"
---
# <span data-ttu-id="1bf0c-101">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bf0c-101">New-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="1bf0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bf0c-102">SYNOPSIS</span></span>
<span data-ttu-id="1bf0c-103">Sanal ağ geçidi oluşturur</span><span class="sxs-lookup"><span data-stu-id="1bf0c-103">Creates a Virtual Network Gateway</span></span>

## <span data-ttu-id="1bf0c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1bf0c-104">SYNTAX</span></span>

### <span data-ttu-id="1bf0c-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1bf0c-105">Default (Default)</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bf0c-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="1bf0c-106">RadiusServerConfiguration</span></span>
```
New-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bf0c-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1bf0c-107">SetByResource</span></span>
```
New-AzVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bf0c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bf0c-108">DESCRIPTION</span></span>
<span data-ttu-id="1bf0c-109">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="1bf0c-110">**New-AzVirtualNetworkGateway** cmdlet 'ı, ad, kaynak grubu adı, konumu ve IP yapılandırmasına bağlı olarak, ağ geçidinizin nesnesini, ağ geçidi türü ve VPN, VPN türü olarak oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-110">The **New-AzVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="1bf0c-111">Ağ Geçidi SKU 'SU de yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="1bf0c-112">Bu ağ geçidi Noktadan siteye bağlantılarda kullanılıyorsa, istemcilere bağlanmak için adres atanacak ve ağ geçidine bağlanan VPN istemcilerinin kimlik doğrulaması için kullanılan VPN Istemcisi kök sertifikasının bulunduğu VPN Istemcisi adres havuzunu da eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="1bf0c-113">Ayrıca, BGP ve etkin-etkin gibi diğer özellikleri de eklemeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="1bf0c-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1bf0c-114">EXAMPLES</span></span>

### <span data-ttu-id="1bf0c-115">1: sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1bf0c-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
$subnet = New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="1bf0c-116">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="1bf0c-117">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="1bf0c-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="1bf0c-118">2: dış RADIUS yapılandırması ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1bf0c-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="1bf0c-119">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="1bf0c-120">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="1bf0c-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="1bf0c-121">Ayrıca, "TestRadiusServer" adresine sahip dış bir RADIUS sunucusu da ekler</span><span class="sxs-lookup"><span data-stu-id="1bf0c-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="1bf0c-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1bf0c-122">PARAMETERS</span></span>

### <span data-ttu-id="1bf0c-123">-Iş</span><span class="sxs-lookup"><span data-stu-id="1bf0c-123">-AsJob</span></span>
<span data-ttu-id="1bf0c-124">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1bf0c-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1bf0c-125">-ASN</span><span class="sxs-lookup"><span data-stu-id="1bf0c-125">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bf0c-126">-DefaultProfile</span></span>
<span data-ttu-id="1bf0c-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="1bf0c-128">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="1bf0c-128">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="1bf0c-129">Etkin özelliği etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-129">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="1bf0c-130">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="1bf0c-130">-EnableBgp</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-131">-Force</span><span class="sxs-lookup"><span data-stu-id="1bf0c-131">-Force</span></span>
<span data-ttu-id="1bf0c-132">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1bf0c-133">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="1bf0c-133">-GatewayDefaultSite</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-134">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="1bf0c-134">-GatewaySku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-135">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="1bf0c-135">-GatewayType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Vpn, ExpressRoute

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-136">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="1bf0c-136">-IpConfigurations</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-137">-Konum</span><span class="sxs-lookup"><span data-stu-id="1bf0c-137">-Location</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="1bf0c-138">-Name</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-139">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="1bf0c-139">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-140">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="1bf0c-140">-RadiusServerAddress</span></span>
<span data-ttu-id="1bf0c-141">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-141">P2S External Radius server address.</span></span>
```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="1bf0c-142">-RadiusServerSecret</span></span>
<span data-ttu-id="1bf0c-143">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-143">P2S External Radius server secret.</span></span>
```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bf0c-144">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-145">Etiketli</span><span class="sxs-lookup"><span data-stu-id="1bf0c-145">-Tag</span></span>
<span data-ttu-id="1bf0c-146">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-146">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1bf0c-147">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="1bf0c-147">For example:</span></span>

<span data-ttu-id="1bf0c-148">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1bf0c-148">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1bf0c-149">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="1bf0c-149">-VpnClientAddressPool</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-150">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="1bf0c-150">-VpnClientProtocol</span></span>
<span data-ttu-id="1bf0c-151">P2S VPN istemci tünel protokolleri listesi</span><span class="sxs-lookup"><span data-stu-id="1bf0c-151">The list of P2S VPN client tunneling protocols</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 
Accepted values: SSTP, IkeV2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-152">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="1bf0c-152">-VpnClientRevokedCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-153">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="1bf0c-153">-VpnClientRootCertificates</span></span>
```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-154">-VpnType</span><span class="sxs-lookup"><span data-stu-id="1bf0c-154">-VpnType</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PolicyBased, RouteBased

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bf0c-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="1bf0c-155">-Confirm</span></span>
<span data-ttu-id="1bf0c-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bf0c-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bf0c-157">-WhatIf</span></span>
<span data-ttu-id="1bf0c-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bf0c-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bf0c-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bf0c-160">CommonParameters</span></span>
<span data-ttu-id="1bf0c-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bf0c-162">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bf0c-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bf0c-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1bf0c-163">INPUTS</span></span>

## <span data-ttu-id="1bf0c-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1bf0c-164">OUTPUTS</span></span>

### <span data-ttu-id="1bf0c-165">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bf0c-165">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="1bf0c-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1bf0c-166">NOTES</span></span>

## <span data-ttu-id="1bf0c-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1bf0c-167">RELATED LINKS</span></span>

[<span data-ttu-id="1bf0c-168">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bf0c-168">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1bf0c-169">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bf0c-169">Remove-AzVirtualNetworkGateway</span></span>](./Remove-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1bf0c-170">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bf0c-170">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1bf0c-171">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bf0c-171">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="1bf0c-172">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1bf0c-172">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)