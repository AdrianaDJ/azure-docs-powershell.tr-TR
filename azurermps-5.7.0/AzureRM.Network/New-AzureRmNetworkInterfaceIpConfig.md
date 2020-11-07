---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D29C82CC-2080-48DA-880A-1AA83007E552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 4499daa24230b9ec0b4731aa7be17c6f040db7d6
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93765204"
---
# <span data-ttu-id="59219-101">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="59219-101">New-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="59219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59219-102">SYNOPSIS</span></span>
<span data-ttu-id="59219-103">Ağ arabirimi IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-103">Creates a network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59219-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59219-104">SYNTAX</span></span>

### <span data-ttu-id="59219-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59219-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>] [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59219-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="59219-106">SetByResourceId</span></span>
```
New-AzureRmNetworkInterfaceIpConfig -Name <String> [-PrivateIpAddressVersion <String>]
 [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>] [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59219-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="59219-107">DESCRIPTION</span></span>
<span data-ttu-id="59219-108">**Yeni-Azurermnetworkınterfaceipconfig** cmdlet 'i, bir ağ arabirimi Için bir Azure ağ arabirimi IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-108">The **New-AzureRmNetworkInterfaceIpConfig** cmdlet creates an Azure network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="59219-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59219-109">EXAMPLES</span></span>

### <span data-ttu-id="59219-110">1: ağ arabirimi için genel IP adresiyle bir IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="59219-110">1: Create an IP configuration with a public IP address for a network interface</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$PIP1 = Get-AzureRmPublicIPAddress -Name "PIP1" -ResourceGroupName "RG1"

$IPConfig1 = New-AzureRmNetworkInterfaceIpConfig -Name "IPConfig-1" -Subnet $Subnet -PublicIpAddress $PIP1
    -Primary

 $nic = New-AzureRmNetworkInterface -Name $NicName -ResourceGroupName myrg -Location westus
    -IpConfiguration $IpConfig1
```

<span data-ttu-id="59219-111">İlk iki komut myvnet adlı bir sanal ağ ve önceden oluşturulmuş olan mysubnet adlı bir alt ağ alır.</span><span class="sxs-lookup"><span data-stu-id="59219-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="59219-112">Bunlar sırasıyla $vnet ve $Subnet depolanır.</span><span class="sxs-lookup"><span data-stu-id="59219-112">These are stored in $vnet and $Subnet respectively.</span></span> <span data-ttu-id="59219-113">Üçüncü komut PIP1 adındaki önceden oluşturulmuş bir genel IP adresini alır.</span><span class="sxs-lookup"><span data-stu-id="59219-113">The third command gets a previously created public IP address called PIP1.</span></span> <span data-ttu-id="59219-114">İleri komutu, birincil IP yapılandırması olarak "IPConfig-1" adlı yeni bir IP yapılandırması oluşturur ve onunla ilişkilendirilmiş ortak bir IP adresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-114">The forth command creates a new IP configuration called "IPConfig-1" as the primary IP configuration with a public IP address associated with it.</span></span>
<span data-ttu-id="59219-115">Son komut, bu IP yapılandırmasını kullanarak mynic1 adındaki bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-115">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

### <span data-ttu-id="59219-116">2: özel bir IP adresiyle bir IP yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="59219-116">2: Create an IP configuration with a private IP address</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$IPConfig2 = New-AzureRmNetworkInterfaceIpConfig -Name "IP-Config2" -Subnet $Subnet -PrivateIpAddress
    10.0.0.5

$nic = New-AzureRmNetworkInterface -Name mynic1 -ResourceGroupName myrg -Location westus -IpConfiguration
    $IpConfig2
```

<span data-ttu-id="59219-117">İlk iki komut myvnet adlı bir sanal ağ ve önceden oluşturulmuş olan mysubnet adlı bir alt ağ alır.</span><span class="sxs-lookup"><span data-stu-id="59219-117">The first two commands get a virtual network called myvnet and a subnet called mysubnet respectively that were previously created.</span></span> <span data-ttu-id="59219-118">Bunlar sırasıyla $vnet ve $Subnet depolanır.</span><span class="sxs-lookup"><span data-stu-id="59219-118">These are stored in $vnet and $Subnet respectively.</span></span>  <span data-ttu-id="59219-119">Üçüncü komut kendisiyle ilişkilendirilmiş özel bir IP adresi 10.0.0.5 ile "IPConfig-2" adlı yeni bir IP yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-119">The third command creates a new IP configuration called "IPConfig-2" with a private IP address 10.0.0.5 associated with it.</span></span>
<span data-ttu-id="59219-120">Son komut, bu IP yapılandırmasını kullanarak mynic1 adındaki bir ağ arabirimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-120">The last command then creates a network interface called mynic1 using this IP configuration.</span></span>

## <span data-ttu-id="59219-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59219-121">PARAMETERS</span></span>

### <span data-ttu-id="59219-122">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="59219-122">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="59219-123">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-123">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="59219-124">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="59219-124">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="59219-125">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-125">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="59219-126">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="59219-126">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="59219-127">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-127">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="59219-128">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="59219-128">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="59219-129">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-129">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="59219-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59219-130">-DefaultProfile</span></span>
<span data-ttu-id="59219-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59219-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59219-132">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="59219-132">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="59219-133">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-133">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="59219-134">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="59219-134">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="59219-135">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-135">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="59219-136">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="59219-136">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="59219-137">Bu ağ arabirimi IP yapılandırması 'nın ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-137">Specifies a collection of load balancer inbound Nat Rule references to which this network interface IPConfiguration belongs.</span></span>

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

### <span data-ttu-id="59219-138">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="59219-138">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="59219-139">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-139">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="59219-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="59219-140">-Name</span></span>
<span data-ttu-id="59219-141">Ağ arabirimi IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-141">Specifies the name of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59219-142">-Birincil</span><span class="sxs-lookup"><span data-stu-id="59219-142">-Primary</span></span>
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

### <span data-ttu-id="59219-143">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="59219-143">-PrivateIpAddress</span></span>
<span data-ttu-id="59219-144">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-144">Specifies the static IP address of the network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59219-145">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="59219-145">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="59219-146">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-146">Specifies the IP address version of a network interface IP configuration.</span></span>

<span data-ttu-id="59219-147">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="59219-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59219-148">'Ü</span><span class="sxs-lookup"><span data-stu-id="59219-148">IPv4</span></span>
- <span data-ttu-id="59219-149">'Yı</span><span class="sxs-lookup"><span data-stu-id="59219-149">IPv6</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59219-150">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="59219-150">-PublicIpAddress</span></span>
<span data-ttu-id="59219-151">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-151">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="59219-152">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-152">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59219-153">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="59219-153">-PublicIpAddressId</span></span>
<span data-ttu-id="59219-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59219-155">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="59219-155">-Subnet</span></span>
<span data-ttu-id="59219-156">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-156">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="59219-157">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="59219-157">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59219-158">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="59219-158">-SubnetId</span></span>
<span data-ttu-id="59219-159">Bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa bir başvuru belirtir.</span><span class="sxs-lookup"><span data-stu-id="59219-159">Specifies a reference to a subnet in which this network interface IP configuration is created.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59219-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59219-160">CommonParameters</span></span>
<span data-ttu-id="59219-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59219-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59219-162">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59219-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59219-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59219-163">INPUTS</span></span>

### <span data-ttu-id="59219-164">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59219-164">None</span></span>
<span data-ttu-id="59219-165">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="59219-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59219-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59219-166">OUTPUTS</span></span>

### <span data-ttu-id="59219-167">Microsoft. Azure. Commands. Network. model. Psnetworkınterfaceıp yapılandırması</span><span class="sxs-lookup"><span data-stu-id="59219-167">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="59219-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59219-168">NOTES</span></span>
* <span data-ttu-id="59219-169">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="59219-169">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="59219-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59219-170">RELATED LINKS</span></span>

[<span data-ttu-id="59219-171">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="59219-171">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="59219-172">Get-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="59219-172">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="59219-173">Remove-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="59219-173">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="59219-174">Set-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="59219-174">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


