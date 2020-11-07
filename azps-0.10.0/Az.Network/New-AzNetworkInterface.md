---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: a4a40f67eef901cd1e93ac004fa01a3224ab222e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935383"
---
# <span data-ttu-id="2b93d-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2b93d-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="2b93d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b93d-102">SYNOPSIS</span></span>
<span data-ttu-id="2b93d-103">Ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b93d-103">Creates a network interface.</span></span>

## <span data-ttu-id="2b93d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b93d-104">SYNTAX</span></span>

### <span data-ttu-id="2b93d-105">SetByIpConfigurationResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b93d-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b93d-106">Setbyipconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="2b93d-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b93d-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2b93d-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b93d-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2b93d-108">SetByResource</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 [-PublicIpAddress <PSPublicIpAddress>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b93d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b93d-109">DESCRIPTION</span></span>
<span data-ttu-id="2b93d-110">**New-AzNetworkInterface** cmdlet 'ı bir Azure ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b93d-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="2b93d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b93d-111">EXAMPLES</span></span>

### <span data-ttu-id="2b93d-112">Örnek 1: Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b93d-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="2b93d-113">Bu komut, VirtualNetwork1 adındaki sanal ağda dinamik olarak atanmış özel bir IP adresine sahip NetworkInterface001 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b93d-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="2b93d-114">Komut ayrıca ağ arabirimine iki DNS sunucusu atar.</span><span class="sxs-lookup"><span data-stu-id="2b93d-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="2b93d-115">IPConfiguration1 adı kullanılarak IP yapılandırması alt kaynağı otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2b93d-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="2b93d-116">Örnek 2: IP yapılandırma nesnesini kullanarak Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b93d-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="2b93d-117">Bu örnek, IP yapılandırma nesnesi kullanan yeni bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b93d-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="2b93d-118">IP yapılandırma nesnesi statik özel bir IPv4 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="2b93d-119">İlk komut, IPConfig1 adlı bir ağ arabirimi IP yapılandırması oluşturur ve yapılandırmayı $IPconfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="2b93d-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="2b93d-120">İkinci komut, $IPconfig adlı değişkende depolanan ağ arabirimi IP yapılandırmasını kullanan NetworkInterface1 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b93d-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="2b93d-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b93d-121">PARAMETERS</span></span>

### <span data-ttu-id="2b93d-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2b93d-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="2b93d-123">**Applicationgatewaybackendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2b93d-124">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="2b93d-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="2b93d-125">**Applicationgatewaybackendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2b93d-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b93d-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="2b93d-127">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="2b93d-128">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="2b93d-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="2b93d-129">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="2b93d-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="2b93d-130">-AsJob</span></span>
<span data-ttu-id="2b93d-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2b93d-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b93d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b93d-132">-DefaultProfile</span></span>
<span data-ttu-id="2b93d-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b93d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b93d-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="2b93d-134">-DnsServer</span></span>
<span data-ttu-id="2b93d-135">Ağ arabiriminin DNS sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="2b93d-136">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="2b93d-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="2b93d-137">Hızlandırılmış ağı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="2b93d-138">-Enableipiletme</span><span class="sxs-lookup"><span data-stu-id="2b93d-138">-EnableIPForwarding</span></span>
<span data-ttu-id="2b93d-139">Bu cmdlet 'in ağ arabiriminin IP iletimini etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="2b93d-140">IP yönlendirme, sanal makinenin diğer hedeflere yönlendirilen trafiği almasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2b93d-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="2b93d-141">-Force</span><span class="sxs-lookup"><span data-stu-id="2b93d-141">-Force</span></span>
<span data-ttu-id="2b93d-142">Aynı ada sahip bir ağ arabirimi olsa bile ağ arabirimini oluşturmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2b93d-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="2b93d-143">-Internaldnsnamelabel</span><span class="sxs-lookup"><span data-stu-id="2b93d-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="2b93d-144">Yeni ağ arabiriminin iç DNS adı etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-144">Specifies the internal DNS name label for the new network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-145">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2b93d-145">-IpConfiguration</span></span>
<span data-ttu-id="2b93d-146">Bu cmdlet 'in ağ arabirimi için kullandığı IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="2b93d-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="2b93d-147">-IpConfigurationName</span></span>
<span data-ttu-id="2b93d-148">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-148">Specifies the name of an IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2b93d-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="2b93d-150">**Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2b93d-151">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="2b93d-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="2b93d-152">**Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2b93d-153">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="2b93d-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="2b93d-154">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="2b93d-155">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="2b93d-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="2b93d-156">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="2b93d-157">-Konum</span><span class="sxs-lookup"><span data-stu-id="2b93d-157">-Location</span></span>
<span data-ttu-id="2b93d-158">Ağ arabiriminin bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-158">Specifies the region for a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b93d-159">-Name</span></span>
<span data-ttu-id="2b93d-160">Oluşturulacak ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-160">Specifies the name of the network interface to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2b93d-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2b93d-162">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-162">Specifies a **NetworkSecurityGroup** object.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: SetByIpConfigurationResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-163">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="2b93d-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2b93d-164">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-164">Specifies the ID of a network security group.</span></span>

```yaml
Type: String
Parameter Sets: SetByIpConfigurationResourceId, SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-165">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="2b93d-165">-PrivateIpAddress</span></span>
<span data-ttu-id="2b93d-166">Bu ağ arabirimine atanacak statik bir IPv4 IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-167">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="2b93d-167">-PublicIpAddress</span></span>
<span data-ttu-id="2b93d-168">Ağ arabirimine atanacak **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-169">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="2b93d-169">-PublicIpAddressId</span></span>
<span data-ttu-id="2b93d-170">Ağ arabirimine atanacak **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b93d-171">-ResourceGroupName</span></span>
<span data-ttu-id="2b93d-172">Ağ arabiriminin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-173">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="2b93d-173">-Subnet</span></span>
<span data-ttu-id="2b93d-174">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="2b93d-175">Bu cmdlet, bu parametrenin belirttiği alt ağ için bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b93d-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2b93d-176">-SubnetId</span></span>
<span data-ttu-id="2b93d-177">Ağ arabirimi oluşturulacak alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b93d-178">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2b93d-178">-Tag</span></span>
<span data-ttu-id="2b93d-179">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="2b93d-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2b93d-180">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="2b93d-180">For example:</span></span>

<span data-ttu-id="2b93d-181">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="2b93d-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2b93d-182">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b93d-182">-Confirm</span></span>
<span data-ttu-id="2b93d-183">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b93d-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b93d-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b93d-184">-WhatIf</span></span>
<span data-ttu-id="2b93d-185">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b93d-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b93d-186">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b93d-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b93d-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b93d-187">CommonParameters</span></span>
<span data-ttu-id="2b93d-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b93d-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b93d-189">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b93d-189">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b93d-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b93d-190">INPUTS</span></span>

## <span data-ttu-id="2b93d-191">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b93d-191">OUTPUTS</span></span>

### <span data-ttu-id="2b93d-192">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="2b93d-192">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2b93d-193">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b93d-193">NOTES</span></span>

## <span data-ttu-id="2b93d-194">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b93d-194">RELATED LINKS</span></span>

[<span data-ttu-id="2b93d-195">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2b93d-195">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="2b93d-196">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2b93d-196">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="2b93d-197">Set-Azağinterface</span><span class="sxs-lookup"><span data-stu-id="2b93d-197">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
