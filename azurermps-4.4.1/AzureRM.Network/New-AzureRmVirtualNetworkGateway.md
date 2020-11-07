---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5784FD44-91D4-4537-84F3-4F03CCBA355F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 55ed36aa2ea09e871d4e109a35207f12c43f57d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764810"
---
# <span data-ttu-id="195fe-101">New-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195fe-101">New-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="195fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="195fe-102">SYNOPSIS</span></span>
<span data-ttu-id="195fe-103">Sanal ağ geçidi oluşturur</span><span class="sxs-lookup"><span data-stu-id="195fe-103">Creates a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="195fe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="195fe-104">SYNTAX</span></span>

### <span data-ttu-id="195fe-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="195fe-105">Default (Default)</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="195fe-106">Radiusserveryapılandırması</span><span class="sxs-lookup"><span data-stu-id="195fe-106">RadiusServerConfiguration</span></span>
```
New-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="195fe-107">SetByResource</span><span class="sxs-lookup"><span data-stu-id="195fe-107">SetByResource</span></span>
```
New-AzureRmVirtualNetworkGateway
 [-IpConfigurations <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayIpConfiguration]>]
 [-GatewayType <String>] [-VpnType <String>] [-EnableBgp <Boolean>] [-EnableActiveActiveFeature]
 [-GatewaySku <String>] [-GatewayDefaultSite <PSLocalNetworkGateway>]
 [-VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientProtocol <System.Collections.Generic.List`1[System.String]>]
 [-VpnClientRootCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate]>]
 [-VpnClientRevokedCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate]>]
 [-Asn <UInt32>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="195fe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="195fe-108">DESCRIPTION</span></span>
<span data-ttu-id="195fe-109">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="195fe-109">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="195fe-110">**Yeni-AzureRmVirtualNetworkGateway** cmdlet 'ı, ad, kaynak grubu adı, konumu ve IP yapılandırmasına (ve VPN, VPN türü) dayalı olarak Azure 'da ağ geçidinizin nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="195fe-110">The **New-AzureRmVirtualNetworkGateway** cmdlet creates the object of your gateway in Azure based on the Name, Resource Group Name, Location, and IP configuration, as well as the Gateway Type and if VPN, the VPN Type.</span></span> <span data-ttu-id="195fe-111">Ağ Geçidi SKU 'SU de yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="195fe-111">You can also name the Gateway SKU.</span></span>

<span data-ttu-id="195fe-112">Bu ağ geçidi Noktadan siteye bağlantılarda kullanılıyorsa, istemcilere bağlanmak için adres atanacak ve ağ geçidine bağlanan VPN istemcilerinin kimlik doğrulaması için kullanılan VPN Istemcisi kök sertifikasının bulunduğu VPN Istemcisi adres havuzunu da eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="195fe-112">If this Gateway is being used for Point-to-Site connections, you will also need to include the VPN Client Address Pool from which to assign addresses to connecting clients and the VPN Client Root Certificate used to authenticate VPN clients connecting to the Gateway.</span></span>

<span data-ttu-id="195fe-113">Ayrıca, BGP ve etkin-etkin gibi diğer özellikleri de eklemeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="195fe-113">You can also choose to include other features like BGP and Active-Active.</span></span>

## <span data-ttu-id="195fe-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="195fe-114">EXAMPLES</span></span>

### <span data-ttu-id="195fe-115">1: sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="195fe-115">1: Create a Virtual Network Gateway</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic"
```

<span data-ttu-id="195fe-116">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="195fe-116">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="195fe-117">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="195fe-117">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span>

### <span data-ttu-id="195fe-118">2: dış RADIUS yapılandırması ile sanal ağ geçidi oluşturma</span><span class="sxs-lookup"><span data-stu-id="195fe-118">2: Create a Virtual Network Gateway with External Radius Configuration</span></span>
```
New-AzureRmResourceGroup -Location "UK West" -Name "vnet-gateway"
New-AzureRMVirtualNetworkSubnetConfig -Name 'gatewaysubnet' -AddressPrefix '10.254.0.0/27'

$ngwpip = New-AzureRMPublicIpAddress -Name ngwpip -ResourceGroupName "vnet-gateway" -Location "UK West" -AllocationMethod Dynamic
$vnet = New-AzureRmVirtualNetwork -AddressPrefix "10.254.0.0/27" -Location "UK West" -Name vnet-gateway -ResourceGroupName "vnet-gateway" -Subnet $subnet
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -name 'gatewaysubnet' -VirtualNetwork $vnet
$ngwipconfig = New-AzureRMVirtualNetworkGatewayIpConfig -Name ngwipconfig -SubnetId $subnet.Id -PublicIpAddressId $ngwpip.Id
$Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force

New-AzureRmVirtualNetworkGateway -Name myNGW -ResourceGroupName vnet-gateway -Location "UK West" -IpConfigurations $ngwIpConfig  -GatewayType "Vpn" -VpnType "RouteBased" -GatewaySku "Basic" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="195fe-119">Yukarıdaki, bir kaynak grubu oluşturur, genel IP adresi ister, sanal ağ ve alt ağ oluşturur ve Azure 'da sanal ağ ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="195fe-119">The above will create a resource group, request a Public IP Address, create a Virtual Network and subnet and create a Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="195fe-120">Ağ Geçidi, "UK Batı" kaynak grubunun içinde "VNET-Gateway" kaynak grubunda "Übgw" adlı "Übgw", VPN türü "", ", VPN türü" VPN "ağ geçidi türü</span><span class="sxs-lookup"><span data-stu-id="195fe-120">The gateway will be called "myNGW" within the resource group "vnet-gateway" in the location "UK West" with the previously created IP configurations saved in the variable "ngwIPConfig," the gateway type of "VPN," the vpn type "RouteBased," and the sku "Basic."</span></span> <span data-ttu-id="195fe-121">Ayrıca, "TestRadiusServer" adresine sahip dış bir RADIUS sunucusu da ekler</span><span class="sxs-lookup"><span data-stu-id="195fe-121">It also adds an external radius server with address "TestRadiusServer"</span></span>

## <span data-ttu-id="195fe-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="195fe-122">PARAMETERS</span></span>

### <span data-ttu-id="195fe-123">-ASN</span><span class="sxs-lookup"><span data-stu-id="195fe-123">-Asn</span></span>
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

### <span data-ttu-id="195fe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195fe-124">-DefaultProfile</span></span>
<span data-ttu-id="195fe-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="195fe-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="195fe-126">-EnableActiveActiveFeature</span><span class="sxs-lookup"><span data-stu-id="195fe-126">-EnableActiveActiveFeature</span></span>
<span data-ttu-id="195fe-127">Etkin özelliği etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="195fe-127">Enables the active-active feature.</span></span>

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

### <span data-ttu-id="195fe-128">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="195fe-128">-EnableBgp</span></span>
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

### <span data-ttu-id="195fe-129">-Force</span><span class="sxs-lookup"><span data-stu-id="195fe-129">-Force</span></span>
<span data-ttu-id="195fe-130">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="195fe-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="195fe-131">-GatewayDefaultSite</span><span class="sxs-lookup"><span data-stu-id="195fe-131">-GatewayDefaultSite</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195fe-132">-GatewaySku</span><span class="sxs-lookup"><span data-stu-id="195fe-132">-GatewaySku</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, HighPerformance, UltraPerformance, VpnGw1, VpnGw2, VpnGw3

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195fe-133">-GatewayType</span><span class="sxs-lookup"><span data-stu-id="195fe-133">-GatewayType</span></span>
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

### <span data-ttu-id="195fe-134">-IpConfigurations</span><span class="sxs-lookup"><span data-stu-id="195fe-134">-IpConfigurations</span></span>
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

### <span data-ttu-id="195fe-135">-Konum</span><span class="sxs-lookup"><span data-stu-id="195fe-135">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195fe-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="195fe-136">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195fe-137">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="195fe-137">-PeerWeight</span></span>
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

### <span data-ttu-id="195fe-138">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="195fe-138">-RadiusServerAddress</span></span>
<span data-ttu-id="195fe-139">P2S dış RADIUS sunucusu adresi.</span><span class="sxs-lookup"><span data-stu-id="195fe-139">P2S External Radius server address.</span></span>
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

### <span data-ttu-id="195fe-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="195fe-140">-RadiusServerSecret</span></span>
<span data-ttu-id="195fe-141">Dış RADIUS sunucusu gizliliğini P2S.</span><span class="sxs-lookup"><span data-stu-id="195fe-141">P2S External Radius server secret.</span></span>
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

### <span data-ttu-id="195fe-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195fe-142">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: Default, RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="195fe-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="195fe-143">-Tag</span></span>
<span data-ttu-id="195fe-144">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="195fe-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="195fe-145">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="195fe-145">For example:</span></span>

<span data-ttu-id="195fe-146">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="195fe-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="195fe-147">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="195fe-147">-VpnClientAddressPool</span></span>
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

### <span data-ttu-id="195fe-148">-VpnClientProtocol</span><span class="sxs-lookup"><span data-stu-id="195fe-148">-VpnClientProtocol</span></span>
<span data-ttu-id="195fe-149">P2S VPN istemci tünel protokolleri listesi</span><span class="sxs-lookup"><span data-stu-id="195fe-149">The list of P2S VPN client tunneling protocols</span></span>
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

### <span data-ttu-id="195fe-150">-Vpnclientiptal sertifikaları</span><span class="sxs-lookup"><span data-stu-id="195fe-150">-VpnClientRevokedCertificates</span></span>
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

### <span data-ttu-id="195fe-151">-VpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="195fe-151">-VpnClientRootCertificates</span></span>
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

### <span data-ttu-id="195fe-152">-VpnType</span><span class="sxs-lookup"><span data-stu-id="195fe-152">-VpnType</span></span>
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

### <span data-ttu-id="195fe-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="195fe-153">-Confirm</span></span>
<span data-ttu-id="195fe-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="195fe-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195fe-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195fe-155">-WhatIf</span></span>
<span data-ttu-id="195fe-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="195fe-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195fe-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="195fe-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195fe-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195fe-158">CommonParameters</span></span>
<span data-ttu-id="195fe-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="195fe-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195fe-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="195fe-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195fe-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="195fe-161">INPUTS</span></span>

## <span data-ttu-id="195fe-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="195fe-162">OUTPUTS</span></span>

### <span data-ttu-id="195fe-163">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195fe-163">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="195fe-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="195fe-164">NOTES</span></span>

## <span data-ttu-id="195fe-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="195fe-165">RELATED LINKS</span></span>

[<span data-ttu-id="195fe-166">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195fe-166">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="195fe-167">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195fe-167">Remove-AzureRmVirtualNetworkGateway</span></span>](./Remove-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="195fe-168">Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195fe-168">Reset-AzureRmVirtualNetworkGateway</span></span>](./Reset-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="195fe-169">Resize-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195fe-169">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="195fe-170">Set-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195fe-170">Set-AzureRmVirtualNetworkGateway</span></span>](./Set-AzureRmVirtualNetworkGateway.md)
