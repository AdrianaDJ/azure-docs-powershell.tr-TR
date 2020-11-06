---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7610228A-61F9-41B8-A42A-CD7C793BB33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 57c92345537e72a38c5228c0a10d38f6ad61d13a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594635"
---
# <span data-ttu-id="8fb60-101">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8fb60-101">Add-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="8fb60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fb60-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb60-103">Ağ arabirimine ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="8fb60-103">Adds a network interface IP configuration to a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fb60-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fb60-104">SYNTAX</span></span>

### <span data-ttu-id="8fb60-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8fb60-105">SetByResource (Default)</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fb60-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="8fb60-106">SetByResourceId</span></span>
```
Add-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb60-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fb60-107">DESCRIPTION</span></span>
<span data-ttu-id="8fb60-108">**Add-Azurermnetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabirimine ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="8fb60-108">The **Add-AzureRmNetworkInterfaceIpConfig** cmdlet adds a network interface IP configuration to an Azure network interface.</span></span>

## <span data-ttu-id="8fb60-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fb60-109">EXAMPLES</span></span>

### <span data-ttu-id="8fb60-110">Örnek 1: uygulama güvenlik grubuyla yeni bir IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="8fb60-110">Example 1: Add a new IP configuration with an application security group</span></span>
```
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name MySubnet -AddressPrefix 10.0.1.0/24
$vnet = New-AzureRmvirtualNetwork -Name MyVNET -ResourceGroupName MyResourceGroup -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$nic = New-AzureRmNetworkInterface -Name MyNetworkInterface -ResourceGroupName MyResourceGroup -Location "West US"  -Subnet $vnet.Subnets[0]

$asg = New-AzureRmApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyASG -Location "West US"

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name $nic.IpConfigurations[0].Name -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg | Set-AzureRmNetworkInterface

$nic | Add-AzureRmNetworkInterfaceIpConfig -Name MyNewIpConfig -Subnet $vnet.Subnets[0] -ApplicationSecurityGroup $asg  | Set-AzureRmNetworkInterface
```

<span data-ttu-id="8fb60-111">Bu örnekte, MyVNET adlı yeni sanal ağdaki bir alt ağa ait yeni bir ağ arabirimi oluşturduk.</span><span class="sxs-lookup"><span data-stu-id="8fb60-111">In this example, we create a new network interface MyNetworkInterface that belongs to a subnet in the new virtual network MyVNET.</span></span> <span data-ttu-id="8fb60-112">Ayrıca, ağ arabirimindeki IP yapılandırmalarıyla ilişkilendirilecek bir boş uygulama güvenlik grubu da oluşturduk.</span><span class="sxs-lookup"><span data-stu-id="8fb60-112">We also create an empty application security group MyASG to associate with the IP configurations in the network interface.</span></span> <span data-ttu-id="8fb60-113">Her iki nesne de oluşturulduğunda, varsayılan IP yapılandırmasını MyASG nesnesiyle bağlantılıyoruz.</span><span class="sxs-lookup"><span data-stu-id="8fb60-113">Once both objects are created, we link the default IP configuration to the MyASG object.</span></span> <span data-ttu-id="8fb60-114">Son olarak, ağ arabiriminde, uygulama güvenlik grubu nesnesine bağlanan yeni bir IP yapılandırması oluşturmamız.</span><span class="sxs-lookup"><span data-stu-id="8fb60-114">At last, we create a new IP configuration in the network interface also linked to the application security group object.</span></span>

## <span data-ttu-id="8fb60-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fb60-115">PARAMETERS</span></span>

### <span data-ttu-id="8fb60-116">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8fb60-116">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="8fb60-117">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-117">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8fb60-118">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="8fb60-118">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="8fb60-119">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-119">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8fb60-120">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8fb60-120">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="8fb60-121">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-121">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8fb60-122">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="8fb60-122">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="8fb60-123">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-123">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8fb60-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb60-124">-DefaultProfile</span></span>
<span data-ttu-id="8fb60-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8fb60-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fb60-126">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8fb60-126">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="8fb60-127">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-127">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8fb60-128">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="8fb60-128">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="8fb60-129">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-129">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8fb60-130">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="8fb60-130">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="8fb60-131">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-131">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8fb60-132">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="8fb60-132">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="8fb60-133">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-133">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="8fb60-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="8fb60-134">-Name</span></span>
<span data-ttu-id="8fb60-135">Ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-135">Specifies the name of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="8fb60-136">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8fb60-136">-NetworkInterface</span></span>
<span data-ttu-id="8fb60-137">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-137">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="8fb60-138">Bu cmdlet, bu parametrenin belirttiği nesneye ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="8fb60-138">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="8fb60-139">-Birincil</span><span class="sxs-lookup"><span data-stu-id="8fb60-139">-Primary</span></span>
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

### <span data-ttu-id="8fb60-140">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="8fb60-140">-PrivateIpAddress</span></span>
<span data-ttu-id="8fb60-141">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-141">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="8fb60-142">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8fb60-142">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="8fb60-143">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-143">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="8fb60-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8fb60-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8fb60-145">'Ü</span><span class="sxs-lookup"><span data-stu-id="8fb60-145">IPv4</span></span>
- <span data-ttu-id="8fb60-146">'Yı</span><span class="sxs-lookup"><span data-stu-id="8fb60-146">IPv6</span></span>

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

### <span data-ttu-id="8fb60-147">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="8fb60-147">-PublicIpAddress</span></span>
<span data-ttu-id="8fb60-148">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-148">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="8fb60-149">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb60-149">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="8fb60-150">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="8fb60-150">-PublicIpAddressId</span></span>
<span data-ttu-id="8fb60-151">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb60-151">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="8fb60-152">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="8fb60-152">-Subnet</span></span>
<span data-ttu-id="8fb60-153">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fb60-153">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="8fb60-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb60-154">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="8fb60-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8fb60-155">-SubnetId</span></span>
<span data-ttu-id="8fb60-156">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8fb60-156">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="8fb60-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb60-157">CommonParameters</span></span>
<span data-ttu-id="8fb60-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fb60-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb60-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb60-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb60-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fb60-160">INPUTS</span></span>

### <span data-ttu-id="8fb60-161">Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="8fb60-161">PSNetworkInterface</span></span>
<span data-ttu-id="8fb60-162">Parametre ' NetworkInterface ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="8fb60-162">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="8fb60-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fb60-163">OUTPUTS</span></span>

### <span data-ttu-id="8fb60-164">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="8fb60-164">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8fb60-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fb60-165">NOTES</span></span>
* <span data-ttu-id="8fb60-166">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="8fb60-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8fb60-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fb60-167">RELATED LINKS</span></span>

[<span data-ttu-id="8fb60-168">Get-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="8fb60-168">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8fb60-169">Yeni-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="8fb60-169">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8fb60-170">Remove-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="8fb60-170">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="8fb60-171">Set-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="8fb60-171">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


