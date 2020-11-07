---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 0e74aa06d2966ed4e907de7428ddc1f4d3a6f2cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936527"
---
# <span data-ttu-id="f5c8c-101">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f5c8c-101">Set-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="f5c8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c8c-103">Bir Azure ağ arabirimi IP yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="f5c8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5c8c-104">SYNTAX</span></span>

### <span data-ttu-id="f5c8c-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5c8c-105">SetByResource (Default)</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5c8c-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="f5c8c-106">SetByResourceId</span></span>
```
Set-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5c8c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5c8c-107">DESCRIPTION</span></span>
<span data-ttu-id="f5c8c-108">**Set-Aznetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabirimi IP yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-108">The **Set-AzNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="f5c8c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5c8c-109">EXAMPLES</span></span>

### <span data-ttu-id="f5c8c-110">1: IP yapılandırmasının IP adresini değiştirme</span><span class="sxs-lookup"><span data-stu-id="f5c8c-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="f5c8c-111">İlk iki komut myvnet adlı bir sanal ağ ve mysubnet adlı bir alt ağ alır ve bunu değişkenler $vnet ve $subnet sırayla depolar.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="f5c8c-112">Üçüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="f5c8c-113">Üçüncü komut, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="f5c8c-114">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="f5c8c-115">2: bir uygulama güvenliği grubu ile bir IP yapılandırmasını ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="f5c8c-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzNetworkInterface
```

<span data-ttu-id="f5c8c-116">Bu örnekte, $asg değişkeni uygulama güvenlik grubuna başvuru içerir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="f5c8c-117">Dördüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="f5c8c-118">Set-AzNetworkInterfaceIpConfig, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar ve alınan uygulama güvenlik grubuyla bir ilişki oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-118">The Set-AzNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="f5c8c-119">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="f5c8c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5c8c-120">PARAMETERS</span></span>

### <span data-ttu-id="f5c8c-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f5c8c-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="f5c8c-122">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f5c8c-123">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="f5c8c-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="f5c8c-124">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f5c8c-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f5c8c-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="f5c8c-126">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f5c8c-127">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="f5c8c-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="f5c8c-128">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f5c8c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c8c-129">-DefaultProfile</span></span>
<span data-ttu-id="f5c8c-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5c8c-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f5c8c-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="f5c8c-132">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f5c8c-133">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="f5c8c-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="f5c8c-134">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f5c8c-135">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="f5c8c-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="f5c8c-136">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f5c8c-137">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="f5c8c-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="f5c8c-138">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="f5c8c-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="f5c8c-139">-Name</span></span>
<span data-ttu-id="f5c8c-140">Bu cmdlet 'in ayarladığı ağ IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="f5c8c-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f5c8c-141">-NetworkInterface</span></span>
<span data-ttu-id="f5c8c-142">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="f5c8c-143">Bu cmdlet, bu parametrenin belirttiği nesneye ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5c8c-144">-Birincil</span><span class="sxs-lookup"><span data-stu-id="f5c8c-144">-Primary</span></span>
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

### <span data-ttu-id="f5c8c-145">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="f5c8c-145">-PrivateIpAddress</span></span>
<span data-ttu-id="f5c8c-146">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="f5c8c-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="f5c8c-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="f5c8c-148">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="f5c8c-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f5c8c-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f5c8c-150">'Ü</span><span class="sxs-lookup"><span data-stu-id="f5c8c-150">IPv4</span></span>
- <span data-ttu-id="f5c8c-151">'Yı</span><span class="sxs-lookup"><span data-stu-id="f5c8c-151">IPv6</span></span>

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

### <span data-ttu-id="f5c8c-152">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="f5c8c-152">-PublicIpAddress</span></span>
<span data-ttu-id="f5c8c-153">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="f5c8c-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="f5c8c-155">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="f5c8c-155">-PublicIpAddressId</span></span>
<span data-ttu-id="f5c8c-156">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="f5c8c-157">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="f5c8c-157">-Subnet</span></span>
<span data-ttu-id="f5c8c-158">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="f5c8c-159">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="f5c8c-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f5c8c-160">-SubnetId</span></span>
<span data-ttu-id="f5c8c-161">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="f5c8c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c8c-162">CommonParameters</span></span>
<span data-ttu-id="f5c8c-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5c8c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c8c-164">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5c8c-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c8c-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5c8c-165">INPUTS</span></span>

### <span data-ttu-id="f5c8c-166">Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="f5c8c-166">PSNetworkInterface</span></span>
<span data-ttu-id="f5c8c-167">Parametre ' NetworkInterface ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="f5c8c-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="f5c8c-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5c8c-168">OUTPUTS</span></span>

### <span data-ttu-id="f5c8c-169">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="f5c8c-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f5c8c-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5c8c-170">NOTES</span></span>
* <span data-ttu-id="f5c8c-171">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="f5c8c-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f5c8c-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5c8c-172">RELATED LINKS</span></span>

[<span data-ttu-id="f5c8c-173">Add-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="f5c8c-173">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f5c8c-174">Get-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="f5c8c-174">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f5c8c-175">New-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="f5c8c-175">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f5c8c-176">Remove-Aznetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="f5c8c-176">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)


