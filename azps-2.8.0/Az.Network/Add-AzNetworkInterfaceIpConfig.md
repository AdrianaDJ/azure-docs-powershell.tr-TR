---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 7aed72b3d219bf8a8c4f930d0b575fca4338ffc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932089"
---
# <span data-ttu-id="07235-101">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="07235-101">Add-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="07235-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07235-102">SYNOPSIS</span></span>
<span data-ttu-id="07235-103">Ağ arabirimine ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="07235-103">Adds a network interface IP configuration to a network interface.</span></span>

## <span data-ttu-id="07235-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="07235-104">SYNTAX</span></span>

### <span data-ttu-id="07235-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="07235-105">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07235-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="07235-106">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07235-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="07235-107">DESCRIPTION</span></span>
<span data-ttu-id="07235-108">**Add-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabirimine ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="07235-108">The **Add-AzNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="07235-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="07235-109">EXAMPLES</span></span>

### <span data-ttu-id="07235-110">Örnek 1: uygulama güvenlik grubuyla yeni bir IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="07235-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzVirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US" -Subnet $vnet.Subnets[0]

$asg = New-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface

$nic | Add-AzNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzNetworkInterface
```

<span data-ttu-id="07235-111">Bu örnekte, MyVNET adlı yeni sanal ağdaki bir alt ağa ait yeni bir ağ arabirimi oluşturduk.</span><span class="sxs-lookup"><span data-stu-id="07235-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="07235-112">Ayrıca, ağ arabirimindeki IP yapılandırmalarıyla ilişkilendirilecek bir boş uygulama güvenlik grubu da oluşturduk.</span><span class="sxs-lookup"><span data-stu-id="07235-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="07235-113">Her iki nesne de oluşturulduğunda, varsayılan IP yapılandırmasını MyASG nesnesiyle bağlantılıyoruz.</span><span class="sxs-lookup"><span data-stu-id="07235-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="07235-114">Son olarak, ağ arabiriminde, uygulama güvenlik grubu nesnesine bağlanan yeni bir IP yapılandırması oluşturmamız.</span><span class="sxs-lookup"><span data-stu-id="07235-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="07235-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="07235-115">PARAMETERS</span></span>

### <span data-ttu-id="07235-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="07235-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="07235-117">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="07235-118">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="07235-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="07235-119">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="07235-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="07235-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="07235-121">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="07235-122">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="07235-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="07235-123">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="07235-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07235-124">-DefaultProfile</span></span>
<span data-ttu-id="07235-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="07235-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07235-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="07235-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="07235-127">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="07235-128">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="07235-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="07235-129">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="07235-130">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="07235-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="07235-131">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="07235-132">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="07235-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="07235-133">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="07235-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="07235-134">-Name</span></span>
<span data-ttu-id="07235-135">Ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="07235-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="07235-136">-NetworkInterface</span></span>
<span data-ttu-id="07235-137">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="07235-138">Bu cmdlet, bu parametrenin belirttiği nesneye ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="07235-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07235-139">-Birincil</span><span class="sxs-lookup"><span data-stu-id="07235-139">-Primary</span></span>
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

### <span data-ttu-id="07235-140">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="07235-140">-PrivateIpAddress</span></span>
<span data-ttu-id="07235-141">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="07235-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="07235-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="07235-143">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="07235-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="07235-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="07235-145">'Ü</span><span class="sxs-lookup"><span data-stu-id="07235-145">IPv4</span></span>
- <span data-ttu-id="07235-146">'Yı</span><span class="sxs-lookup"><span data-stu-id="07235-146">IPv6</span></span>

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

### <span data-ttu-id="07235-147">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="07235-147">-PublicIpAddress</span></span>
<span data-ttu-id="07235-148">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="07235-149">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07235-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="07235-150">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="07235-150">-PublicIpAddressId</span></span>
<span data-ttu-id="07235-151">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07235-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="07235-152">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="07235-152">-Subnet</span></span>
<span data-ttu-id="07235-153">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="07235-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="07235-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07235-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="07235-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="07235-155">-SubnetId</span></span>
<span data-ttu-id="07235-156">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="07235-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="07235-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07235-157">CommonParameters</span></span>
<span data-ttu-id="07235-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="07235-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07235-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07235-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07235-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="07235-160">INPUTS</span></span>

### <span data-ttu-id="07235-161">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="07235-161">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="07235-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="07235-162">System.String[]</span></span>

### <span data-ttu-id="07235-163">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="07235-163">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="07235-164">Microsoft. Azure. Commands. Network. model. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="07235-164">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="07235-165">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="07235-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="07235-166">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="07235-166">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="07235-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="07235-167">OUTPUTS</span></span>

### <span data-ttu-id="07235-168">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="07235-168">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="07235-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="07235-169">NOTES</span></span>
* <span data-ttu-id="07235-170">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="07235-170">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="07235-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="07235-171">RELATED LINKS</span></span>

[<span data-ttu-id="07235-172">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="07235-172">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="07235-173">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="07235-173">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="07235-174">Remove-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="07235-174">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="07235-175">Set-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="07235-175">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
