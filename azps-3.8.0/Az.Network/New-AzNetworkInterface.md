---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: feefe02c5056556d360a54819ea429cd39b84b62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097614"
---
# <span data-ttu-id="32a7d-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="32a7d-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="32a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="32a7d-103">Ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a7d-103">Creates a network interface.</span></span>

## <span data-ttu-id="32a7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32a7d-104">SYNTAX</span></span>

### <span data-ttu-id="32a7d-105">SetByIpConfigurationResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32a7d-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a7d-106">Setbyipconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="32a7d-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a7d-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="32a7d-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32a7d-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="32a7d-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <PSBackendAddressPool[]>] [-LoadBalancerInboundNatRule <PSInboundNatRule[]>]
 [-ApplicationGatewayBackendAddressPool <PSApplicationGatewayBackendAddressPool[]>]
 [-ApplicationSecurityGroup <PSApplicationSecurityGroup[]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>] [-EnableIPForwarding]
 [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32a7d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="32a7d-109">DESCRIPTION</span></span>
<span data-ttu-id="32a7d-110">**New-AzNetworkInterface** cmdlet 'ı bir Azure ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a7d-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="32a7d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32a7d-111">EXAMPLES</span></span>

### <span data-ttu-id="32a7d-112">Örnek 1: Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="32a7d-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="32a7d-113">Bu komut, VirtualNetwork1 adındaki sanal ağda dinamik olarak atanmış özel bir IP adresine sahip NetworkInterface001 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a7d-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="32a7d-114">Komut ayrıca ağ arabirimine iki DNS sunucusu atar.</span><span class="sxs-lookup"><span data-stu-id="32a7d-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="32a7d-115">IPConfiguration1 adı kullanılarak IP yapılandırması alt kaynağı otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="32a7d-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="32a7d-116">Örnek 2: IP yapılandırma nesnesini kullanarak Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="32a7d-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="32a7d-117">Bu örnek, IP yapılandırma nesnesi kullanan yeni bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a7d-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="32a7d-118">IP yapılandırma nesnesi statik özel bir IPv4 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="32a7d-119">İlk komut, ikinci komutta alt ağı atamak için kullanılan, mevcut belirtilen sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="32a7d-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="32a7d-120">İkinci komut IPConfig1 adlı bir ağ arabirimi IP yapılandırması oluşturur ve $IPconfig adlı değişkende yapılandırmayı depolar.</span><span class="sxs-lookup"><span data-stu-id="32a7d-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="32a7d-121">Üçüncü komut, $IPconfig adlı değişkende depolanan ağ arabirimi IP yapılandırmasını kullanan NetworkInterface1 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a7d-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="32a7d-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32a7d-122">PARAMETERS</span></span>

### <span data-ttu-id="32a7d-123">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="32a7d-123">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="32a7d-124">**Applicationgatewaybackendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-124">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="32a7d-125">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="32a7d-125">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="32a7d-126">**Applicationgatewaybackendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-126">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="32a7d-127">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32a7d-127">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="32a7d-128">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-128">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="32a7d-129">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="32a7d-129">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="32a7d-130">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-130">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="32a7d-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="32a7d-131">-AsJob</span></span>
<span data-ttu-id="32a7d-132">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="32a7d-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32a7d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32a7d-133">-DefaultProfile</span></span>
<span data-ttu-id="32a7d-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32a7d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32a7d-135">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="32a7d-135">-DnsServer</span></span>
<span data-ttu-id="32a7d-136">Ağ arabiriminin DNS sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-136">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="32a7d-137">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="32a7d-137">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="32a7d-138">Hızlandırılmış ağı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-138">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="32a7d-139">-Enableipiletme</span><span class="sxs-lookup"><span data-stu-id="32a7d-139">-EnableIPForwarding</span></span>
<span data-ttu-id="32a7d-140">Bu cmdlet 'in ağ arabiriminin IP iletimini etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-140">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="32a7d-141">IP yönlendirme, sanal makinenin diğer hedeflere yönlendirilen trafiği almasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="32a7d-141">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="32a7d-142">-Force</span><span class="sxs-lookup"><span data-stu-id="32a7d-142">-Force</span></span>
<span data-ttu-id="32a7d-143">Aynı ada sahip bir ağ arabirimi olsa bile ağ arabirimini oluşturmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="32a7d-143">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="32a7d-144">-Internaldnsnamelabel</span><span class="sxs-lookup"><span data-stu-id="32a7d-144">-InternalDnsNameLabel</span></span>
<span data-ttu-id="32a7d-145">Yeni ağ arabiriminin iç DNS adı etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-145">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-146">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="32a7d-146">-IpConfiguration</span></span>
<span data-ttu-id="32a7d-147">Bu cmdlet 'in ağ arabirimi için kullandığı IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-147">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-148">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="32a7d-148">-IpConfigurationName</span></span>
<span data-ttu-id="32a7d-149">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-149">Specifies the name of an IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-150">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="32a7d-150">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="32a7d-151">**Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-151">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="32a7d-152">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="32a7d-152">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="32a7d-153">**Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-153">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="32a7d-154">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="32a7d-154">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="32a7d-155">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-155">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="32a7d-156">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="32a7d-156">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="32a7d-157">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-157">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="32a7d-158">-Konum</span><span class="sxs-lookup"><span data-stu-id="32a7d-158">-Location</span></span>
<span data-ttu-id="32a7d-159">Ağ arabiriminin bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-159">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="32a7d-160">-Ad</span><span class="sxs-lookup"><span data-stu-id="32a7d-160">-Name</span></span>
<span data-ttu-id="32a7d-161">Oluşturulacak ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-161">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="32a7d-162">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32a7d-162">-NetworkSecurityGroup</span></span>
<span data-ttu-id="32a7d-163">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-163">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-164">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="32a7d-164">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="32a7d-165">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-165">Specifies the ID of a network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-166">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="32a7d-166">-PrivateIpAddress</span></span>
<span data-ttu-id="32a7d-167">Bu ağ arabirimine atanacak statik bir IPv4 IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-167">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-168">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="32a7d-168">-PublicIpAddress</span></span>
<span data-ttu-id="32a7d-169">Ağ arabirimine atanacak **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-169">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-170">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="32a7d-170">-PublicIpAddressId</span></span>
<span data-ttu-id="32a7d-171">Ağ arabirimine atanacak **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-171">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32a7d-172">-ResourceGroupName</span></span>
<span data-ttu-id="32a7d-173">Ağ arabiriminin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-173">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="32a7d-174">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="32a7d-174">-Subnet</span></span>
<span data-ttu-id="32a7d-175">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-175">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="32a7d-176">Bu cmdlet, bu parametrenin belirttiği alt ağ için bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32a7d-176">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-177">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="32a7d-177">-SubnetId</span></span>
<span data-ttu-id="32a7d-178">Ağ arabirimi oluşturulacak alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-178">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a7d-179">Etiketli</span><span class="sxs-lookup"><span data-stu-id="32a7d-179">-Tag</span></span>
<span data-ttu-id="32a7d-180">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="32a7d-180">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="32a7d-181">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="32a7d-181">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="32a7d-182">-Onay</span><span class="sxs-lookup"><span data-stu-id="32a7d-182">-Confirm</span></span>
<span data-ttu-id="32a7d-183">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32a7d-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32a7d-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32a7d-184">-WhatIf</span></span>
<span data-ttu-id="32a7d-185">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32a7d-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32a7d-186">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32a7d-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32a7d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a7d-187">CommonParameters</span></span>
<span data-ttu-id="32a7d-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32a7d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a7d-189">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a7d-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a7d-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32a7d-190">INPUTS</span></span>

### <span data-ttu-id="32a7d-191">System. String</span><span class="sxs-lookup"><span data-stu-id="32a7d-191">System.String</span></span>

### <span data-ttu-id="32a7d-192">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp Yapılandırması []</span><span class="sxs-lookup"><span data-stu-id="32a7d-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="32a7d-193">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="32a7d-193">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="32a7d-194">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="32a7d-194">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="32a7d-195">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32a7d-195">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="32a7d-196">System. String []</span><span class="sxs-lookup"><span data-stu-id="32a7d-196">System.String[]</span></span>

### <span data-ttu-id="32a7d-197">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="32a7d-197">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="32a7d-198">Microsoft. Azure. Commands. Network. model. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="32a7d-198">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="32a7d-199">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="32a7d-199">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="32a7d-200">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="32a7d-200">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="32a7d-201">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="32a7d-201">System.Collections.Hashtable</span></span>

## <span data-ttu-id="32a7d-202">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32a7d-202">OUTPUTS</span></span>

### <span data-ttu-id="32a7d-203">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="32a7d-203">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="32a7d-204">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32a7d-204">NOTES</span></span>

## <span data-ttu-id="32a7d-205">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32a7d-205">RELATED LINKS</span></span>

[<span data-ttu-id="32a7d-206">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="32a7d-206">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="32a7d-207">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="32a7d-207">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="32a7d-208">Set-Azağinterface</span><span class="sxs-lookup"><span data-stu-id="32a7d-208">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
