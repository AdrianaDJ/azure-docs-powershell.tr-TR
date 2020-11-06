---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2F2082F-4BAA-4FBE-8846-2D436A433570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterface.md
ms.openlocfilehash: 111723b2f0271583d43bd1c845eebe9800190a59
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93595214"
---
# <span data-ttu-id="2a93e-101">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2a93e-101">New-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="2a93e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a93e-102">SYNOPSIS</span></span>
<span data-ttu-id="2a93e-103">Ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a93e-103">Creates a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a93e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a93e-104">SYNTAX</span></span>

### <span data-ttu-id="2a93e-105">SetByIpConfigurationResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2a93e-105">SetByIpConfigurationResource (Default)</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a93e-106">Setbyipconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="2a93e-106">SetByIpConfigurationResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String>
 -IpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration]>
 [-NetworkSecurityGroupId <String>] [-NetworkSecurityGroup <PSNetworkSecurityGroup>]
 [-DnsServer <System.Collections.Generic.List`1[System.String]>] [-InternalDnsNameLabel <String>]
 [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a93e-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="2a93e-107">SetByResourceId</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -SubnetId <String>
 [-PublicIpAddressId <String>] [-NetworkSecurityGroupId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>] [-PrivateIpAddress <String>]
 [-IpConfigurationName <String>] [-DnsServer <System.Collections.Generic.List`1[System.String]>]
 [-InternalDnsNameLabel <String>] [-EnableIPForwarding] [-EnableAcceleratedNetworking] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a93e-108">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2a93e-108">SetByResource</span></span>
```
New-AzureRmNetworkInterface -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
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

## <span data-ttu-id="2a93e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a93e-109">DESCRIPTION</span></span>
<span data-ttu-id="2a93e-110">**New-Azurermnetworkınterface** cmdlet 'ı bir Azure ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a93e-110">The **New-AzureRmNetworkInterface** cmdlet creates an Azure network interface.</span></span>

## <span data-ttu-id="2a93e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a93e-111">EXAMPLES</span></span>

### <span data-ttu-id="2a93e-112">Örnek 1: Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2a93e-112">Example 1: Create an Azure network interface</span></span>
```
PS C:\>New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1" -IpConfigurationName "IPConfiguration1" -DnsServer "8.8.8.8", "8.8.4.4"
```

<span data-ttu-id="2a93e-113">Bu komut, VirtualNetwork1 adındaki sanal ağda dinamik olarak atanmış özel bir IP adresine sahip NetworkInterface001 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a93e-113">This command creates a network interface named NetworkInterface001 with a dynamically assigned private IP address from Subnet1 in the virtual network named VirtualNetwork1.</span></span> <span data-ttu-id="2a93e-114">Komut ayrıca ağ arabirimine iki DNS sunucusu atar.</span><span class="sxs-lookup"><span data-stu-id="2a93e-114">The command also assigns two DNS servers to the network interface.</span></span> <span data-ttu-id="2a93e-115">IPConfiguration1 adı kullanılarak IP yapılandırması alt kaynağı otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2a93e-115">The IPConfiguration child resource will be created automatically using the name IPConfiguration1.</span></span>

### <span data-ttu-id="2a93e-116">Örnek 2: IP yapılandırma nesnesini kullanarak Azure ağ arabirimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="2a93e-116">Example 2: Create an Azure network interface using an IP configuration object</span></span>
```
PS C:\>$IPconfig = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig1" -PrivateIpAddressVersion IPv4 -PrivateIpAddress "10.0.1.10" -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup1/providers/Microsoft.Network/virtualNetworks/VirtualNetwork1/subnets/Subnet1"
PS C:\> New-AzureRmNetworkInterface -Name "NetworkInterface1" -ResourceGroupName "ResourceGroup1" -Location "centralus" -IpConfiguration $IPconfig
```

<span data-ttu-id="2a93e-117">Bu örnek, IP yapılandırma nesnesi kullanan yeni bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a93e-117">This example creates a new network interface using an IP configuration object.</span></span> <span data-ttu-id="2a93e-118">IP yapılandırma nesnesi statik özel bir IPv4 adresi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-118">The IP configuration object specifies a static private IPv4 address.</span></span>

<span data-ttu-id="2a93e-119">İlk komut, IPConfig1 adlı bir ağ arabirimi IP yapılandırması oluşturur ve yapılandırmayı $IPconfig adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="2a93e-119">The first command creates a network interface IP configuration named IPConfig1 and stores the configuration in the variable named $IPconfig.</span></span>

<span data-ttu-id="2a93e-120">İkinci komut, $IPconfig adlı değişkende depolanan ağ arabirimi IP yapılandırmasını kullanan NetworkInterface1 adlı bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a93e-120">The second command creates a network interface named NetworkInterface1 that uses the network interface IP configuration stored in the variable named $IPconfig.</span></span>

## <span data-ttu-id="2a93e-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a93e-121">PARAMETERS</span></span>

### <span data-ttu-id="2a93e-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a93e-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="2a93e-123">**Applicationgatewaybackendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-123">Specifies an **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2a93e-124">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="2a93e-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="2a93e-125">**Applicationgatewaybackendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-125">Specifies the ID of a **ApplicationGatewayBackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2a93e-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a93e-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="2a93e-127">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-127">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="2a93e-128">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="2a93e-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="2a93e-129">Ağ arabirimi IP yapılandırmasının ait olacağı uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-129">Specifies a collection of application security group references to which the network interface IP configuration should belong to.</span></span>

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

### <span data-ttu-id="2a93e-130">-Iş</span><span class="sxs-lookup"><span data-stu-id="2a93e-130">-AsJob</span></span>
<span data-ttu-id="2a93e-131">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2a93e-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a93e-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a93e-132">-DefaultProfile</span></span>
<span data-ttu-id="2a93e-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a93e-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a93e-134">-DnsServer</span><span class="sxs-lookup"><span data-stu-id="2a93e-134">-DnsServer</span></span>
<span data-ttu-id="2a93e-135">Ağ arabiriminin DNS sunucusunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-135">Specifies the DNS server for the network interface.</span></span>

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

### <span data-ttu-id="2a93e-136">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="2a93e-136">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="2a93e-137">Hızlandırılmış ağı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-137">Enables accelerated networking.</span></span>

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

### <span data-ttu-id="2a93e-138">-Enableipiletme</span><span class="sxs-lookup"><span data-stu-id="2a93e-138">-EnableIPForwarding</span></span>
<span data-ttu-id="2a93e-139">Bu cmdlet 'in ağ arabiriminin IP iletimini etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-139">Indicates that this cmdlet enables IP forwarding for the network interface.</span></span>
<span data-ttu-id="2a93e-140">IP yönlendirme, sanal makinenin diğer hedeflere yönlendirilen trafiği almasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2a93e-140">IP forwarding allows a virtual machine to receive traffic addressed to other destinations.</span></span>

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

### <span data-ttu-id="2a93e-141">-Force</span><span class="sxs-lookup"><span data-stu-id="2a93e-141">-Force</span></span>
<span data-ttu-id="2a93e-142">Aynı ada sahip bir ağ arabirimi olsa bile ağ arabirimini oluşturmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="2a93e-142">Forces the creation of the network interface even if a network interface with the same name already exists.</span></span>

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

### <span data-ttu-id="2a93e-143">-Internaldnsnamelabel</span><span class="sxs-lookup"><span data-stu-id="2a93e-143">-InternalDnsNameLabel</span></span>
<span data-ttu-id="2a93e-144">Yeni ağ arabiriminin iç DNS adı etiketini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-144">Specifies the internal DNS name label for the new network interface.</span></span>

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

### <span data-ttu-id="2a93e-145">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="2a93e-145">-IpConfiguration</span></span>
<span data-ttu-id="2a93e-146">Bu cmdlet 'in ağ arabirimi için kullandığı IP yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-146">Specifies the IP configuration that this cmdlet uses for the network interface.</span></span>

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

### <span data-ttu-id="2a93e-147">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="2a93e-147">-IpConfigurationName</span></span>
<span data-ttu-id="2a93e-148">IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-148">Specifies the name of an IP configuration.</span></span>

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

### <span data-ttu-id="2a93e-149">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="2a93e-149">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="2a93e-150">**Backendaddresspool** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-150">Specifies a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2a93e-151">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="2a93e-151">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="2a93e-152">**Backendaddresspool** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-152">Specifies the ID of a **BackendAddressPool** object.</span></span>

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

### <span data-ttu-id="2a93e-153">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="2a93e-153">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="2a93e-154">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-154">Specifies an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="2a93e-155">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="2a93e-155">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="2a93e-156">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-156">Specifies the ID of an inbound NAT rule configuration for a load balancer.</span></span>

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

### <span data-ttu-id="2a93e-157">-Konum</span><span class="sxs-lookup"><span data-stu-id="2a93e-157">-Location</span></span>
<span data-ttu-id="2a93e-158">Ağ arabiriminin bölgesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-158">Specifies the region for a network interface.</span></span>

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

### <span data-ttu-id="2a93e-159">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a93e-159">-Name</span></span>
<span data-ttu-id="2a93e-160">Oluşturulacak ağ arabiriminin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-160">Specifies the name of the network interface to create.</span></span>

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

### <span data-ttu-id="2a93e-161">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2a93e-161">-NetworkSecurityGroup</span></span>
<span data-ttu-id="2a93e-162">Bir **Networksecuritygroup** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-162">Specifies a **NetworkSecurityGroup** object.</span></span>

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

### <span data-ttu-id="2a93e-163">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="2a93e-163">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="2a93e-164">Ağ güvenlik grubunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-164">Specifies the ID of a network security group.</span></span>

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

### <span data-ttu-id="2a93e-165">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="2a93e-165">-PrivateIpAddress</span></span>
<span data-ttu-id="2a93e-166">Bu ağ arabirimine atanacak statik bir IPv4 IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-166">Specifies a static IPv4 IP address to assign to this network interface.</span></span>

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

### <span data-ttu-id="2a93e-167">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="2a93e-167">-PublicIpAddress</span></span>
<span data-ttu-id="2a93e-168">Ağ arabirimine atanacak **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-168">Specifies a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="2a93e-169">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="2a93e-169">-PublicIpAddressId</span></span>
<span data-ttu-id="2a93e-170">Ağ arabirimine atanacak **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-170">Specifies the ID of a **PublicIPAddress** object to assign to a network interface.</span></span>

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

### <span data-ttu-id="2a93e-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a93e-171">-ResourceGroupName</span></span>
<span data-ttu-id="2a93e-172">Ağ arabiriminin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-172">Specifies the name of a resource group that the network interface belongs to.</span></span>

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

### <span data-ttu-id="2a93e-173">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="2a93e-173">-Subnet</span></span>
<span data-ttu-id="2a93e-174">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-174">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="2a93e-175">Bu cmdlet, bu parametrenin belirttiği alt ağ için bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2a93e-175">This cmdlet creates a network interface for the subnet that this parameter specifies.</span></span>

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

### <span data-ttu-id="2a93e-176">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2a93e-176">-SubnetId</span></span>
<span data-ttu-id="2a93e-177">Ağ arabirimi oluşturulacak alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-177">Specifies the ID of the subnet for which to create a network interface.</span></span>

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

### <span data-ttu-id="2a93e-178">Etiketli</span><span class="sxs-lookup"><span data-stu-id="2a93e-178">-Tag</span></span>
<span data-ttu-id="2a93e-179">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="2a93e-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2a93e-180">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="2a93e-180">For example:</span></span>

<span data-ttu-id="2a93e-181">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="2a93e-181">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2a93e-182">-Onay</span><span class="sxs-lookup"><span data-stu-id="2a93e-182">-Confirm</span></span>
<span data-ttu-id="2a93e-183">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2a93e-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a93e-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a93e-184">-WhatIf</span></span>
<span data-ttu-id="2a93e-185">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a93e-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a93e-186">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2a93e-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a93e-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a93e-187">CommonParameters</span></span>
<span data-ttu-id="2a93e-188">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a93e-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a93e-189">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a93e-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a93e-190">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a93e-190">INPUTS</span></span>

### <span data-ttu-id="2a93e-191">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2a93e-191">None</span></span>
<span data-ttu-id="2a93e-192">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="2a93e-192">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a93e-193">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a93e-193">OUTPUTS</span></span>

### <span data-ttu-id="2a93e-194">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="2a93e-194">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="2a93e-195">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a93e-195">NOTES</span></span>

## <span data-ttu-id="2a93e-196">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a93e-196">RELATED LINKS</span></span>

[<span data-ttu-id="2a93e-197">Get-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="2a93e-197">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="2a93e-198">Remove-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="2a93e-198">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)

[<span data-ttu-id="2a93e-199">Set-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="2a93e-199">Set-AzureRmNetworkInterface</span></span>](./Set-AzureRmNetworkInterface.md)
