---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkInterface.md
ms.openlocfilehash: 23d0b2eacb5e4053cbed2c08101e225d861311de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276888"
---
# <span data-ttu-id="346a2-101">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="346a2-101">New-AzNetworkInterface</span></span>

## <span data-ttu-id="346a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="346a2-102">SYNOPSIS</span></span>
<span data-ttu-id="346a2-103">Ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="346a2-103">Creates a network interface.</span></span>

## <span data-ttu-id="346a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="346a2-104">SYNTAX</span></span>

### <span data-ttu-id="346a2-105">SetByIpConfigurationResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="346a2-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346a2-106">Setbyipconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="346a2-106">SetByIpConfigurationResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <PSNetworkInterfaceIPConfiguration[]> [-NetworkSecurityGroupId <String>]
 [-NetworkSecurityGroup <PSNetworkSecurityGroup>] [-DnsServer <String[]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346a2-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="346a2-107">SetByResourceId</span></span>
```
New-AzNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <String[]>] [-LoadBalancerInboundNatRuleId <String[]>]
 [-ApplicationGatewayBackendAddressPoolId <String[]>] [-ApplicationSecurityGroupId <String[]>]
 [-PrivateIpAddress <String>] [-IpConfigurationName <String>] [-DnsServer <String[]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="346a2-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="346a2-108">SetByResource</span></span>
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

## <span data-ttu-id="346a2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="346a2-109">DESCRIPTION</span></span>
<span data-ttu-id="346a2-110">**New-AzNetworkInterface** cmdlet 'ı bir Azure ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="346a2-110">The **New-AzNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="346a2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="346a2-111">EXAMPLES</span></span>

### <span data-ttu-id="346a2-112">Örnek 1: Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="346a2-112">Example 1: Create an Azure network interface</span></span>
```powershell
PS C:\>New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="346a2-113">Bu komut, VirtualNetwork1 adındaki sanal ağda dinamik olarak atanmış özel bir IP adresine sahip NetworkInterface001 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="346a2-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="346a2-114">Komut ayrıca ağ arabirimine iki DNS sunucusu atar.</span><span class="sxs-lookup"><span data-stu-id="346a2-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="346a2-115">IPConfiguration1 adı kullanılarak IP yapılandırması alt kaynağı otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="346a2-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="346a2-116">Örnek 2: IP yapılandırma nesnesini kullanarak Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="346a2-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```powershell
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "VirtualNetwork1" -ResourceGroupName "ResourceGroup1" 
PS C:\>$IPconfig = New-AzNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId $Subnet.Subnets[0].Id
PS C:\> New-AzNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="346a2-117">Bu örnek, IP yapılandırma nesnesi kullanan yeni bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="346a2-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="346a2-118">IP yapılandırma nesnesi statik özel bir IPv4 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-118">The IP configuration object specifies a static private IPv4 address.</span></span>
<span data-ttu-id="346a2-119">İlk komut, ikinci komutta alt ağı atamak için kullanılan, mevcut belirtilen sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="346a2-119">The first command retrieves an existing specified virtual network used to assign the subnet in the second command.</span></span>
<span data-ttu-id="346a2-120">İkinci komut IPConfig1 adlı bir ağ arabirimi IP yapılandırması oluşturur ve $IPconfig adlı değişkende yapılandırmayı depolar.</span><span class="sxs-lookup"><span data-stu-id="346a2-120">The second command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>
<span data-ttu-id="346a2-121">Üçüncü komut, $IPconfig adlı değişkende depolanan ağ arabirimi IP yapılandırmasını kullanan NetworkInterface1 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="346a2-121">The third command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

### <span data-ttu-id="346a2-122">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="346a2-122">Example 3</span></span>

<span data-ttu-id="346a2-123">Ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="346a2-123">Creates a network interface.</span></span> <span data-ttu-id="346a2-124">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="346a2-124">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzNetworkInterface -Location 'West US' -Name 'NetworkInterface1' -PrivateIpAddress '10.0.1.10' -ResourceGroupName 'ResourceGroup1' -SubnetId '/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1'
```

## <span data-ttu-id="346a2-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="346a2-125">PARAMETERS</span></span>

### <span data-ttu-id="346a2-126">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="346a2-126">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="346a2-127">**Applicationgatewaybackendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-127">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="346a2-128">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="346a2-128">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="346a2-129">**Applicationgatewaybackendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-129">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="346a2-130">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="346a2-130">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="346a2-131">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-131">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="346a2-132">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="346a2-132">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="346a2-133">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-133">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="346a2-134">-Iş</span><span class="sxs-lookup"><span data-stu-id="346a2-134">-AsJob</span></span>
<span data-ttu-id="346a2-135">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="346a2-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="346a2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346a2-136">-DefaultProfile</span></span>
<span data-ttu-id="346a2-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="346a2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="346a2-138">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="346a2-138">-DnsServer</span></span>
<span data-ttu-id="346a2-139">Ağ arabiriminin DNS sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-139">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="346a2-140">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="346a2-140">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="346a2-141">Hızlandırılmış ağı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="346a2-141">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="346a2-142">-Enableipiletme</span><span class="sxs-lookup"><span data-stu-id="346a2-142">-EnableIPForwarding</span></span>
<span data-ttu-id="346a2-143">Bu cmdlet 'in ağ arabiriminin IP iletimini etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-143">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="346a2-144">IP yönlendirme, sanal makinenin diğer hedeflere yönlendirilen trafiği almasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="346a2-144">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="346a2-145">-Force</span><span class="sxs-lookup"><span data-stu-id="346a2-145">-Force</span></span>
<span data-ttu-id="346a2-146">Aynı ada sahip bir ağ arabirimi olsa bile ağ arabirimini oluşturmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="346a2-146">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="346a2-147">-Internaldnsnamelabel</span><span class="sxs-lookup"><span data-stu-id="346a2-147">-InternalDnsNameLabel</span></span>
<span data-ttu-id="346a2-148">Yeni ağ arabiriminin iç DNS adı etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-148">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="346a2-149">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="346a2-149">-IpConfiguration</span></span>
<span data-ttu-id="346a2-150">Bu cmdlet 'in ağ arabirimi için kullandığı IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-150">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="346a2-151">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="346a2-151">-IpConfigurationName</span></span>
<span data-ttu-id="346a2-152">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-152">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="346a2-153">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="346a2-153">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="346a2-154">**Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-154">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="346a2-155">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="346a2-155">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="346a2-156">**Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-156">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="346a2-157">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="346a2-157">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="346a2-158">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-158">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="346a2-159">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="346a2-159">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="346a2-160">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-160">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="346a2-161">-Konum</span><span class="sxs-lookup"><span data-stu-id="346a2-161">-Location</span></span>
<span data-ttu-id="346a2-162">Ağ arabiriminin bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-162">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="346a2-163">-Ad</span><span class="sxs-lookup"><span data-stu-id="346a2-163">-Name</span></span>
<span data-ttu-id="346a2-164">Oluşturulacak ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-164">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="346a2-165">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="346a2-165">-NetworkSecurityGroup</span></span>
<span data-ttu-id="346a2-166">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-166">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="346a2-167">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="346a2-167">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="346a2-168">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-168">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="346a2-169">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="346a2-169">-PrivateIpAddress</span></span>
<span data-ttu-id="346a2-170">Bu ağ arabirimine atanacak statik bir IPv4 IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-170">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="346a2-171">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="346a2-171">-PublicIpAddress</span></span>
<span data-ttu-id="346a2-172">Ağ arabirimine atanacak **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-172">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="346a2-173">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="346a2-173">-PublicIpAddressId</span></span>
<span data-ttu-id="346a2-174">Ağ arabirimine atanacak **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-174">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="346a2-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="346a2-175">-ResourceGroupName</span></span>
<span data-ttu-id="346a2-176">Ağ arabiriminin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-176">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="346a2-177">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="346a2-177">-Subnet</span></span>
<span data-ttu-id="346a2-178">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-178">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="346a2-179">Bu cmdlet, bu parametrenin belirttiği alt ağ için bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="346a2-179">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="346a2-180">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="346a2-180">-SubnetId</span></span>
<span data-ttu-id="346a2-181">Ağ arabirimi oluşturulacak alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="346a2-181">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="346a2-182">Etiketli</span><span class="sxs-lookup"><span data-stu-id="346a2-182">-Tag</span></span>
<span data-ttu-id="346a2-183">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="346a2-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="346a2-184">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="346a2-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="346a2-185">-Onay</span><span class="sxs-lookup"><span data-stu-id="346a2-185">-Confirm</span></span>
<span data-ttu-id="346a2-186">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="346a2-186">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="346a2-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="346a2-187">-WhatIf</span></span>
<span data-ttu-id="346a2-188">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="346a2-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="346a2-189">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="346a2-189">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="346a2-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346a2-190">CommonParameters</span></span>
<span data-ttu-id="346a2-191">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="346a2-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346a2-192">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="346a2-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346a2-193">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="346a2-193">INPUTS</span></span>

### <span data-ttu-id="346a2-194">System. String</span><span class="sxs-lookup"><span data-stu-id="346a2-194">System.String</span></span>

### <span data-ttu-id="346a2-195">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp Yapılandırması []</span><span class="sxs-lookup"><span data-stu-id="346a2-195">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration[]</span></span>

### <span data-ttu-id="346a2-196">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="346a2-196">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="346a2-197">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="346a2-197">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

### <span data-ttu-id="346a2-198">Microsoft. Azure. Commands. Network. model. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="346a2-198">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

### <span data-ttu-id="346a2-199">System. String []</span><span class="sxs-lookup"><span data-stu-id="346a2-199">System.String[]</span></span>

### <span data-ttu-id="346a2-200">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="346a2-200">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool[]</span></span>

### <span data-ttu-id="346a2-201">Microsoft. Azure. Commands. Network. model. PSInboundNatRule []</span><span class="sxs-lookup"><span data-stu-id="346a2-201">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule[]</span></span>

### <span data-ttu-id="346a2-202">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool []</span><span class="sxs-lookup"><span data-stu-id="346a2-202">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool[]</span></span>

### <span data-ttu-id="346a2-203">Microsoft. Azure. Commands. Network. modeller. PSApplicationSecurityGroup []</span><span class="sxs-lookup"><span data-stu-id="346a2-203">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup[]</span></span>

### <span data-ttu-id="346a2-204">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="346a2-204">System.Collections.Hashtable</span></span>

## <span data-ttu-id="346a2-205">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="346a2-205">OUTPUTS</span></span>

### <span data-ttu-id="346a2-206">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="346a2-206">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="346a2-207">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="346a2-207">NOTES</span></span>

## <span data-ttu-id="346a2-208">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="346a2-208">RELATED LINKS</span></span>

[<span data-ttu-id="346a2-209">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="346a2-209">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="346a2-210">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="346a2-210">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)

[<span data-ttu-id="346a2-211">Set-Azağinterface</span><span class="sxs-lookup"><span data-stu-id="346a2-211">Set-AzNetworkInterface</span></span>](./Set-AzNetworkInterface.md)
