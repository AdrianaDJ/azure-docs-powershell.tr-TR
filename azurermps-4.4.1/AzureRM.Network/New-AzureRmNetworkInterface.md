---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 75e16da63a5348b47a5b67042a2fb1e2078206c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763683"
---
# <span data-ttu-id="cfa0e-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cfa0e-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="cfa0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfa0e-102">SYNOPSIS</span></span>
<span data-ttu-id="cfa0e-103">Ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfa0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfa0e-104">SYNTAX</span></span>

### <span data-ttu-id="cfa0e-105">SetByIpConfigurationResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cfa0e-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa0e-106">Setbyipconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="cfa0e-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa0e-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="cfa0e-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfa0e-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="cfa0e-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfa0e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfa0e-109">DESCRIPTION</span></span>
<span data-ttu-id="cfa0e-110">**New-Azurermnetworkınterface** cmdlet 'ı bir Azure ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="cfa0e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfa0e-111">EXAMPLES</span></span>

### <span data-ttu-id="cfa0e-112">Örnek 1: Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="cfa0e-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="cfa0e-113">Bu komut, VirtualNetwork1 adındaki sanal ağda dinamik olarak atanmış özel bir IP adresine sahip NetworkInterface001 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="cfa0e-114">Komut ayrıca ağ arabirimine iki DNS sunucusu atar.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="cfa0e-115">IPConfiguration1 adı kullanılarak IP yapılandırması alt kaynağı otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="cfa0e-116">Örnek 2: IP yapılandırma nesnesini kullanarak Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="cfa0e-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="cfa0e-117">Bu örnek, IP yapılandırma nesnesi kullanan yeni bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="cfa0e-118">IP yapılandırma nesnesi statik özel bir IPv4 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="cfa0e-119">İlk komut, IPConfig1 adlı bir ağ arabirimi IP yapılandırması oluşturur ve yapılandırmayı $IPconfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="cfa0e-120">İkinci komut, $IPconfig adlı değişkende depolanan ağ arabirimi IP yapılandırmasını kullanan NetworkInterface1 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="cfa0e-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfa0e-121">PARAMETERS</span></span>

### <span data-ttu-id="cfa0e-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cfa0e-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="cfa0e-123">**Applicationgatewaybackendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-124">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="cfa0e-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="cfa0e-125">**Applicationgatewaybackendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cfa0e-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="cfa0e-127">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-128">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="cfa0e-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="cfa0e-129">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfa0e-130">-DefaultProfile</span></span>
<span data-ttu-id="cfa0e-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfa0e-132">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="cfa0e-132">-DnsServer</span></span>
<span data-ttu-id="cfa0e-133">Ağ arabiriminin DNS sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-133">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="cfa0e-134">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="cfa0e-134">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="cfa0e-135">Hızlandırılmış ağı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-135">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="cfa0e-136">-Enableipiletme</span><span class="sxs-lookup"><span data-stu-id="cfa0e-136">-EnableIPForwarding</span></span>
<span data-ttu-id="cfa0e-137">Bu cmdlet 'in ağ arabiriminin IP iletimini etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-137">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="cfa0e-138">IP yönlendirme, sanal makinenin diğer hedeflere yönlendirilen trafiği almasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-138">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="cfa0e-139">-Force</span><span class="sxs-lookup"><span data-stu-id="cfa0e-139">-Force</span></span>
<span data-ttu-id="cfa0e-140">Aynı ada sahip bir ağ arabirimi olsa bile ağ arabirimini oluşturmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-140">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="cfa0e-141">-Internaldnsnamelabel</span><span class="sxs-lookup"><span data-stu-id="cfa0e-141">-InternalDnsNameLabel</span></span>
<span data-ttu-id="cfa0e-142">Yeni ağ arabiriminin iç DNS adı etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-142">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="cfa0e-143">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="cfa0e-143">-IpConfiguration</span></span>
<span data-ttu-id="cfa0e-144">Bu cmdlet 'in ağ arabirimi için kullandığı IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-144">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]
Parameter Sets: SetByIpConfigurationResource, SetByIpConfigurationResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-145">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cfa0e-145">-IpConfigurationName</span></span>
<span data-ttu-id="cfa0e-146">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-146">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="cfa0e-147">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cfa0e-147">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="cfa0e-148">**Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-148">Specifies a **BackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-149">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="cfa0e-149">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="cfa0e-150">**Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-150">Specifies the ID of a **BackendAddressPool** object.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-151">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="cfa0e-151">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="cfa0e-152">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-152">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-153">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="cfa0e-153">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="cfa0e-154">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-154">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfa0e-155">-Konum</span><span class="sxs-lookup"><span data-stu-id="cfa0e-155">-Location</span></span>
<span data-ttu-id="cfa0e-156">Ağ arabiriminin bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-156">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="cfa0e-157">-Ad</span><span class="sxs-lookup"><span data-stu-id="cfa0e-157">-Name</span></span>
<span data-ttu-id="cfa0e-158">Oluşturulacak ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-158">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="cfa0e-159">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="cfa0e-159">-NetworkSecurityGroup</span></span>
<span data-ttu-id="cfa0e-160">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-160">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="cfa0e-161">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="cfa0e-161">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="cfa0e-162">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-162">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="cfa0e-163">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="cfa0e-163">-PrivateIpAddress</span></span>
<span data-ttu-id="cfa0e-164">Bu ağ arabirimine atanacak statik bir IPv4 IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-164">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="cfa0e-165">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="cfa0e-165">-PublicIpAddress</span></span>
<span data-ttu-id="cfa0e-166">Ağ arabirimine atanacak **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-166">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="cfa0e-167">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="cfa0e-167">-PublicIpAddressId</span></span>
<span data-ttu-id="cfa0e-168">Ağ arabirimine atanacak **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-168">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="cfa0e-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfa0e-169">-ResourceGroupName</span></span>
<span data-ttu-id="cfa0e-170">Ağ arabiriminin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-170">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="cfa0e-171">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="cfa0e-171">-Subnet</span></span>
<span data-ttu-id="cfa0e-172">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-172">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="cfa0e-173">Bu cmdlet, bu parametrenin belirttiği alt ağ için bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-173">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="cfa0e-174">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cfa0e-174">-SubnetId</span></span>
<span data-ttu-id="cfa0e-175">Ağ arabirimi oluşturulacak alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-175">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="cfa0e-176">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cfa0e-176">-Tag</span></span>
<span data-ttu-id="cfa0e-177">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-177">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cfa0e-178">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="cfa0e-178">For example:</span></span>

<span data-ttu-id="cfa0e-179">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="cfa0e-179">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cfa0e-180">-Onay</span><span class="sxs-lookup"><span data-stu-id="cfa0e-180">-Confirm</span></span>
<span data-ttu-id="cfa0e-181">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfa0e-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfa0e-182">-WhatIf</span></span>
<span data-ttu-id="cfa0e-183">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfa0e-184">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfa0e-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfa0e-185">CommonParameters</span></span>
<span data-ttu-id="cfa0e-186">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfa0e-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfa0e-187">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfa0e-187">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfa0e-188">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfa0e-188">INPUTS</span></span>

## <span data-ttu-id="cfa0e-189">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfa0e-189">OUTPUTS</span></span>

### <span data-ttu-id="cfa0e-190">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="cfa0e-190">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cfa0e-191">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfa0e-191">NOTES</span></span>

## <span data-ttu-id="cfa0e-192">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfa0e-192">RELATED LINKS</span></span>

[<span data-ttu-id="cfa0e-193">Get-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="cfa0e-193">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="cfa0e-194">Remove-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="cfa0e-194">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="cfa0e-195">Set-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="cfa0e-195">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
