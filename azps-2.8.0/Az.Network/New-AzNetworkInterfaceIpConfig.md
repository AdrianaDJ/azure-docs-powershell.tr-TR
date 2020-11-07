---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: daf136e5f0954aca32fce1c3f92f5ea5580dae16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918244"
---
# <span data-ttu-id="af5ce-101">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="af5ce-101">New-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="af5ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="af5ce-103">Ağ arabirimi IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-103">Creates a network interface IP configuration.</span></span>

## <span data-ttu-id="af5ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af5ce-104">SYNTAX</span></span>

### <span data-ttu-id="af5ce-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="af5ce-105">SetByResource (Default)</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af5ce-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="af5ce-106">SetByResourceId</span></span>
```
New-AzNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>]
 [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af5ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="af5ce-107">DESCRIPTION</span></span>
<span data-ttu-id="af5ce-108">**New-Aznetworkınterfaceipconfig** cmdlet 'i ağ arabirimi Için bir Azure ağ arabirimi IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-108">The **New-AzNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="af5ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af5ce-109">EXAMPLES</span></span>

### <span data-ttu-id="af5ce-110">1: ağ arabirimi için genel IP adresiyle bir IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="af5ce-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="af5ce-111">İlk iki komut myvnet adlı bir sanal ağ ve önceden oluşturulmuş olan mysubnet adlı bir alt ağ alır.</span><span class="sxs-lookup"><span data-stu-id="af5ce-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="af5ce-112">Bunlar sırasıyla $vnet ve $Subnet depolanır.</span><span class="sxs-lookup"><span data-stu-id="af5ce-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="af5ce-113">Üçüncü komut PIP1 adındaki önceden oluşturulmuş bir genel IP adresini alır.</span><span class="sxs-lookup"><span data-stu-id="af5ce-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="af5ce-114">İleri komutu, birincil IP yapılandırması olarak "IPConfig-1" adlı yeni bir IP yapılandırması oluşturur ve onunla ilişkilendirilmiş ortak bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="af5ce-115">Son komut, bu IP yapılandırmasını kullanarak mynic1 adındaki bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="af5ce-116">2: özel bir IP adresiyle bir IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="af5ce-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="af5ce-117">İlk iki komut myvnet adlı bir sanal ağ ve önceden oluşturulmuş olan mysubnet adlı bir alt ağ alır.</span><span class="sxs-lookup"><span data-stu-id="af5ce-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="af5ce-118">Bunlar sırasıyla $vnet ve $Subnet depolanır.</span><span class="sxs-lookup"><span data-stu-id="af5ce-118">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="af5ce-119">Üçüncü komut kendisiyle ilişkilendirilmiş özel bir IP adresi 10.0.0.5 ile "IPConfig-2" adlı yeni bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="af5ce-120">Son komut, bu IP yapılandırmasını kullanarak mynic1 adındaki bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="af5ce-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af5ce-121">PARAMETERS</span></span>

### <span data-ttu-id="af5ce-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af5ce-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="af5ce-123">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-124">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="af5ce-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="af5ce-125">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="af5ce-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="af5ce-127">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-128">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="af5ce-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="af5ce-129">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af5ce-130">-DefaultProfile</span></span>
<span data-ttu-id="af5ce-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af5ce-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af5ce-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="af5ce-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="af5ce-133">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-134">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="af5ce-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="af5ce-135">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-136">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="af5ce-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="af5ce-137">Bu ağ arabirimi IP yapılandırması 'nın ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-138">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="af5ce-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="af5ce-139">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="af5ce-140">-Name</span></span>
<span data-ttu-id="af5ce-141">Ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-141">Specifies the name of the network interface IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-142">-Birincil</span><span class="sxs-lookup"><span data-stu-id="af5ce-142">-Primary</span></span>
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

### <span data-ttu-id="af5ce-143">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="af5ce-143">-PrivateIpAddress</span></span>
<span data-ttu-id="af5ce-144">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-144">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="af5ce-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="af5ce-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="af5ce-146">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-146">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="af5ce-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="af5ce-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="af5ce-148">'Ü</span><span class="sxs-lookup"><span data-stu-id="af5ce-148">IPv4</span></span>
- <span data-ttu-id="af5ce-149">'Yı</span><span class="sxs-lookup"><span data-stu-id="af5ce-149">IPv6</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-150">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="af5ce-150">-PublicIpAddress</span></span>
<span data-ttu-id="af5ce-151">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="af5ce-152">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-153">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="af5ce-153">-PublicIpAddressId</span></span>
<span data-ttu-id="af5ce-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="af5ce-155">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="af5ce-155">-Subnet</span></span>
<span data-ttu-id="af5ce-156">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="af5ce-157">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="af5ce-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af5ce-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="af5ce-158">-SubnetId</span></span>
<span data-ttu-id="af5ce-159">Bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa bir başvuru belirtir.</span><span class="sxs-lookup"><span data-stu-id="af5ce-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="af5ce-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af5ce-160">CommonParameters</span></span>
<span data-ttu-id="af5ce-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af5ce-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af5ce-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af5ce-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af5ce-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af5ce-163">INPUTS</span></span>

### <span data-ttu-id="af5ce-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="af5ce-164">System.String[]</span></span>

### <span data-ttu-id="af5ce-165">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="af5ce-165">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="af5ce-166">Microsoft. Azure. Commands. Network. model. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="af5ce-166">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="af5ce-167">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="af5ce-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="af5ce-168">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="af5ce-168">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="af5ce-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af5ce-169">OUTPUTS</span></span>

### <span data-ttu-id="af5ce-170">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="af5ce-170">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="af5ce-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af5ce-171">NOTES</span></span>
* <span data-ttu-id="af5ce-172">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="af5ce-172">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="af5ce-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af5ce-173">RELATED LINKS</span></span>

[<span data-ttu-id="af5ce-174">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="af5ce-174">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="af5ce-175">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="af5ce-175">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="af5ce-176">Remove-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="af5ce-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="af5ce-177">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="af5ce-177">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
