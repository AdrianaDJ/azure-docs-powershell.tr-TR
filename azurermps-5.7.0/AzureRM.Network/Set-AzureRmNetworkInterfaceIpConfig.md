---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: f12605c8c93611783f53bbf8dc6851af277a42b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764164"
---
# <span data-ttu-id="5cdb6-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5cdb6-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="5cdb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cdb6-102">SYNOPSIS</span></span>
<span data-ttu-id="5cdb6-103">Bir Azure ağ arabirimi IP yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cdb6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cdb6-104">SYNTAX</span></span>

### <span data-ttu-id="5cdb6-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cdb6-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-Subnet <PSSubnet>]
 [-PublicIpAddress <PSPublicIpAddress>]
 [-LoadBalancerBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool]>]
 [-LoadBalancerInboundNatRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSInboundNatRule]>]
 [-ApplicationGatewayBackendAddressPool <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool]>]
 [-ApplicationSecurityGroup <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cdb6-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="5cdb6-106">SetByResourceId</span></span>
```
Set-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-PrivateIpAddressVersion <String>] [-PrivateIpAddress <String>] [-Primary] [-SubnetId <String>]
 [-PublicIpAddressId <String>]
 [-LoadBalancerBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-LoadBalancerInboundNatRuleId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationGatewayBackendAddressPoolId <System.Collections.Generic.List`1[System.String]>]
 [-ApplicationSecurityGroupId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cdb6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cdb6-107">DESCRIPTION</span></span>
<span data-ttu-id="5cdb6-108">**Set-Azurermnetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabirimi IP yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="5cdb6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cdb6-109">EXAMPLES</span></span>

### <span data-ttu-id="5cdb6-110">1: IP yapılandırmasının IP adresini değiştirme</span><span class="sxs-lookup"><span data-stu-id="5cdb6-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="5cdb6-111">İlk iki komut myvnet adlı bir sanal ağ ve mysubnet adlı bir alt ağ alır ve bunu değişkenler $vnet ve $subnet sırayla depolar.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="5cdb6-112">Üçüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="5cdb6-113">Üçüncü komut, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="5cdb6-114">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="5cdb6-115">2: bir uygulama güvenlik grubuyla bir IP yapılandırmasını ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="5cdb6-115">2: Associating an IP configuration with an application security group</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="5cdb6-116">Bu örnekte, $asg değişkeni uygulama güvenlik grubuna başvuru içerir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="5cdb6-117">Dördüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="5cdb6-118">Set-AzureRmNetworkInterfaceIpConfig, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar ve alınan uygulama güvenlik grubuyla bir ilişki oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="5cdb6-119">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="5cdb6-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cdb6-120">PARAMETERS</span></span>

### <span data-ttu-id="5cdb6-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5cdb6-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="5cdb6-122">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="5cdb6-123">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="5cdb6-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="5cdb6-124">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="5cdb6-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5cdb6-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="5cdb6-126">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="5cdb6-127">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="5cdb6-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="5cdb6-128">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="5cdb6-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cdb6-129">-DefaultProfile</span></span>
<span data-ttu-id="5cdb6-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cdb6-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5cdb6-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="5cdb6-132">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="5cdb6-133">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="5cdb6-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="5cdb6-134">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="5cdb6-135">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="5cdb6-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="5cdb6-136">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="5cdb6-137">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="5cdb6-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="5cdb6-138">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="5cdb6-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="5cdb6-139">-Name</span></span>
<span data-ttu-id="5cdb6-140">Bu cmdlet 'in ayarladığı ağ IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="5cdb6-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5cdb6-141">-NetworkInterface</span></span>
<span data-ttu-id="5cdb6-142">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="5cdb6-143">Bu cmdlet, bu parametrenin belirttiği nesneye ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="5cdb6-144">-Birincil</span><span class="sxs-lookup"><span data-stu-id="5cdb6-144">-Primary</span></span>
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

### <span data-ttu-id="5cdb6-145">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="5cdb6-145">-PrivateIpAddress</span></span>
<span data-ttu-id="5cdb6-146">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="5cdb6-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="5cdb6-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="5cdb6-148">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="5cdb6-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5cdb6-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cdb6-150">'Ü</span><span class="sxs-lookup"><span data-stu-id="5cdb6-150">IPv4</span></span>
- <span data-ttu-id="5cdb6-151">'Yı</span><span class="sxs-lookup"><span data-stu-id="5cdb6-151">IPv6</span></span>

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

### <span data-ttu-id="5cdb6-152">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="5cdb6-152">-PublicIpAddress</span></span>
<span data-ttu-id="5cdb6-153">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="5cdb6-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="5cdb6-155">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="5cdb6-155">-PublicIpAddressId</span></span>
<span data-ttu-id="5cdb6-156">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="5cdb6-157">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="5cdb6-157">-Subnet</span></span>
<span data-ttu-id="5cdb6-158">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="5cdb6-159">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="5cdb6-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5cdb6-160">-SubnetId</span></span>
<span data-ttu-id="5cdb6-161">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="5cdb6-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cdb6-162">CommonParameters</span></span>
<span data-ttu-id="5cdb6-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cdb6-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cdb6-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cdb6-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cdb6-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cdb6-165">INPUTS</span></span>

### <span data-ttu-id="5cdb6-166">Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="5cdb6-166">PSNetworkInterface</span></span>
<span data-ttu-id="5cdb6-167">Parametre ' NetworkInterface ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="5cdb6-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="5cdb6-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cdb6-168">OUTPUTS</span></span>

### <span data-ttu-id="5cdb6-169">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="5cdb6-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="5cdb6-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cdb6-170">NOTES</span></span>
* <span data-ttu-id="5cdb6-171">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="5cdb6-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="5cdb6-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cdb6-172">RELATED LINKS</span></span>

[<span data-ttu-id="5cdb6-173">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="5cdb6-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5cdb6-174">Get-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="5cdb6-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5cdb6-175">Yeni-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="5cdb6-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5cdb6-176">Remove-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="5cdb6-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


