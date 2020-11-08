---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4c8dd4df4c3dd2d9aac8491b3d04e1755e6b4c38
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097971"
---
# <span data-ttu-id="b4d1d-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4d1d-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="b4d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d1d-103">Ağ arabiriminin IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="b4d1d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4d1d-104">SYNTAX</span></span>

### <span data-ttu-id="b4d1d-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b4d1d-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4d1d-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="b4d1d-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4d1d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4d1d-107">DESCRIPTION</span></span>
<span data-ttu-id="b4d1d-108">**Set-Aznetworkınterfaceipconfig** cmdlet 'i, bir ağ arabiriminin IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="b4d1d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4d1d-109">EXAMPLES</span></span>

### <span data-ttu-id="b4d1d-110">1: IP yapılandırmasının IP adresini değiştirme</span><span class="sxs-lookup"><span data-stu-id="b4d1d-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="b4d1d-111">İlk iki komut myvnet adlı bir sanal ağ ve mysubnet adlı bir alt ağ alır ve bunu değişkenler $vnet ve $subnet sırayla depolar.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="b4d1d-112">Üçüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="b4d1d-113">Üçüncü komut, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="b4d1d-114">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="b4d1d-115">2: bir uygulama güvenlik grubuyla bir IP yapılandırmasını ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="b4d1d-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="b4d1d-116">Bu örnekte, $asg değişkeni uygulama güvenlik grubuna başvuru içerir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="b4d1d-117">Dördüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="b4d1d-118">Set-AzNetworkInterfaceIpConfig, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar ve alınan uygulama güvenlik grubuyla bir ilişki oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="b4d1d-119">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="b4d1d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4d1d-120">PARAMETERS</span></span>

### <span data-ttu-id="b4d1d-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4d1d-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="b4d1d-122">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b4d1d-123">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="b4d1d-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="b4d1d-124">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b4d1d-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4d1d-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="b4d1d-126">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b4d1d-127">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="b4d1d-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="b4d1d-128">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b4d1d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d1d-129">-DefaultProfile</span></span>
<span data-ttu-id="b4d1d-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4d1d-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b4d1d-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="b4d1d-132">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b4d1d-133">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="b4d1d-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="b4d1d-134">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b4d1d-135">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="b4d1d-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="b4d1d-136">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b4d1d-137">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="b4d1d-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="b4d1d-138">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="b4d1d-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="b4d1d-139">-Name</span></span>
<span data-ttu-id="b4d1d-140">Bu cmdlet 'in ayarladığı ağ IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="b4d1d-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b4d1d-141">-NetworkInterface</span></span>
<span data-ttu-id="b4d1d-142">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="b4d1d-143">Bu cmdlet, bu parametrenin belirttiği nesneye ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4d1d-144">-Birincil</span><span class="sxs-lookup"><span data-stu-id="b4d1d-144">-Primary</span></span>
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

### <span data-ttu-id="b4d1d-145">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="b4d1d-145">-PrivateIpAddress</span></span>
<span data-ttu-id="b4d1d-146">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="b4d1d-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="b4d1d-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="b4d1d-148">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="b4d1d-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b4d1d-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b4d1d-150">'Ü</span><span class="sxs-lookup"><span data-stu-id="b4d1d-150">IPv4</span></span>
- <span data-ttu-id="b4d1d-151">'Yı</span><span class="sxs-lookup"><span data-stu-id="b4d1d-151">IPv6</span></span>

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

### <span data-ttu-id="b4d1d-152">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b4d1d-152">-PublicIpAddress</span></span>
<span data-ttu-id="b4d1d-153">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="b4d1d-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="b4d1d-155">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="b4d1d-155">-PublicIpAddressId</span></span>
<span data-ttu-id="b4d1d-156">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="b4d1d-157">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="b4d1d-157">-Subnet</span></span>
<span data-ttu-id="b4d1d-158">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="b4d1d-159">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="b4d1d-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b4d1d-160">-SubnetId</span></span>
<span data-ttu-id="b4d1d-161">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="b4d1d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d1d-162">CommonParameters</span></span>
<span data-ttu-id="b4d1d-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4d1d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d1d-164">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d1d-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d1d-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4d1d-165">INPUTS</span></span>

### <span data-ttu-id="b4d1d-166">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="b4d1d-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="b4d1d-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="b4d1d-167">System.String[]</span></span>

### <span data-ttu-id="b4d1d-168">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="b4d1d-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="b4d1d-169">Microsoft. Azure. Commands. Network. model. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="b4d1d-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="b4d1d-170">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="b4d1d-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="b4d1d-171">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="b4d1d-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="b4d1d-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4d1d-172">OUTPUTS</span></span>

### <span data-ttu-id="b4d1d-173">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="b4d1d-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="b4d1d-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4d1d-174">NOTES</span></span>
* <span data-ttu-id="b4d1d-175">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="b4d1d-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b4d1d-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4d1d-176">RELATED LINKS</span></span>

[<span data-ttu-id="b4d1d-177">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="b4d1d-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b4d1d-178">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="b4d1d-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b4d1d-179">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="b4d1d-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b4d1d-180">Remove-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="b4d1d-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)