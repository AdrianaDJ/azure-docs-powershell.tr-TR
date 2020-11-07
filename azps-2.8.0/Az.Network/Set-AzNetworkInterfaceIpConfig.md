---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0b6c0c850f389dba27e483f5de4e4aee1fca7450
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917892"
---
# <span data-ttu-id="d29c6-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d29c6-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d29c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d29c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d29c6-103">Ağ arabiriminin IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-103">Updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="d29c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d29c6-104">SYNTAX</span></span>

### <span data-ttu-id="d29c6-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d29c6-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>] [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>]
 [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d29c6-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="d29c6-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>] [-LoadBalancerBackendAddressPoolId <String[]>]
 [-LoadBalancerInboundNatRuleId <String[]>] [-ApplicationGatewayBackendAddressPoolId <String[]>]
 [-ApplicationSecurityGroupId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d29c6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d29c6-107">DESCRIPTION</span></span>
<span data-ttu-id="d29c6-108">**Set-Aznetworkınterfaceipconfig** cmdlet 'i, bir ağ arabiriminin IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet updates an IP configuration for a network interface.</span></span>

## <span data-ttu-id="d29c6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d29c6-109">EXAMPLES</span></span>

### <span data-ttu-id="d29c6-110">1: IP yapılandırmasının IP adresini değiştirme</span><span class="sxs-lookup"><span data-stu-id="d29c6-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="d29c6-111">İlk iki komut myvnet adlı bir sanal ağ ve mysubnet adlı bir alt ağ alır ve bunu değişkenler $vnet ve $subnet sırayla depolar.</span><span class="sxs-lookup"><span data-stu-id="d29c6-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="d29c6-112">Üçüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="d29c6-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="d29c6-113">Üçüncü komut, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d29c6-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="d29c6-114">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="d29c6-115">2: bir uygulama güvenlik grubuyla bir IP yapılandırmasını ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="d29c6-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="d29c6-116">Bu örnekte, $asg değişkeni uygulama güvenlik grubuna başvuru içerir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="d29c6-117">Dördüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="d29c6-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="d29c6-118">Set-AzNetworkInterfaceIpConfig, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar ve alınan uygulama güvenlik grubuyla bir ilişki oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d29c6-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="d29c6-119">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="d29c6-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d29c6-120">PARAMETERS</span></span>

### <span data-ttu-id="d29c6-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d29c6-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="d29c6-122">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d29c6-123">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="d29c6-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="d29c6-124">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d29c6-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d29c6-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="d29c6-126">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d29c6-127">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="d29c6-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="d29c6-128">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d29c6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29c6-129">-DefaultProfile</span></span>
<span data-ttu-id="d29c6-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d29c6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d29c6-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d29c6-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="d29c6-132">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d29c6-133">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="d29c6-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="d29c6-134">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d29c6-135">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="d29c6-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="d29c6-136">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d29c6-137">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="d29c6-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="d29c6-138">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="d29c6-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="d29c6-139">-Name</span></span>
<span data-ttu-id="d29c6-140">Bu cmdlet 'in ayarladığı ağ IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="d29c6-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d29c6-141">-NetworkInterface</span></span>
<span data-ttu-id="d29c6-142">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="d29c6-143">Bu cmdlet, bu parametrenin belirttiği nesneye ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="d29c6-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="d29c6-144">-Birincil</span><span class="sxs-lookup"><span data-stu-id="d29c6-144">-Primary</span></span>
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

### <span data-ttu-id="d29c6-145">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="d29c6-145">-PrivateIpAddress</span></span>
<span data-ttu-id="d29c6-146">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="d29c6-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="d29c6-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="d29c6-148">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="d29c6-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d29c6-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d29c6-150">'Ü</span><span class="sxs-lookup"><span data-stu-id="d29c6-150">IPv4</span></span>
- <span data-ttu-id="d29c6-151">'Yı</span><span class="sxs-lookup"><span data-stu-id="d29c6-151">IPv6</span></span>

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

### <span data-ttu-id="d29c6-152">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="d29c6-152">-PublicIpAddress</span></span>
<span data-ttu-id="d29c6-153">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="d29c6-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d29c6-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="d29c6-155">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="d29c6-155">-PublicIpAddressId</span></span>
<span data-ttu-id="d29c6-156">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d29c6-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="d29c6-157">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="d29c6-157">-Subnet</span></span>
<span data-ttu-id="d29c6-158">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d29c6-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="d29c6-159">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d29c6-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="d29c6-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d29c6-160">-SubnetId</span></span>
<span data-ttu-id="d29c6-161">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d29c6-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="d29c6-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29c6-162">CommonParameters</span></span>
<span data-ttu-id="d29c6-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d29c6-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29c6-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d29c6-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29c6-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d29c6-165">INPUTS</span></span>

### <span data-ttu-id="d29c6-166">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d29c6-166">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="d29c6-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="d29c6-167">System.String[]</span></span>

### <span data-ttu-id="d29c6-168">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="d29c6-168">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="d29c6-169">Microsoft. Azure. Commands. Network. model. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="d29c6-169">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="d29c6-170">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="d29c6-170">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="d29c6-171">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="d29c6-171">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

## <span data-ttu-id="d29c6-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d29c6-172">OUTPUTS</span></span>

### <span data-ttu-id="d29c6-173">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="d29c6-173">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d29c6-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d29c6-174">NOTES</span></span>
* <span data-ttu-id="d29c6-175">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="d29c6-175">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d29c6-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d29c6-176">RELATED LINKS</span></span>

[<span data-ttu-id="d29c6-177">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d29c6-177">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d29c6-178">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d29c6-178">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d29c6-179">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d29c6-179">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d29c6-180">Remove-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="d29c6-180">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)
