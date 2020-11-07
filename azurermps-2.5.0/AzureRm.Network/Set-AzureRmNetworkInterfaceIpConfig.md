---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 13EF1028-43DE-424D-8185-EC45B5CEF2C1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterfaceipconfig
schema: 2.0.0
ms.openlocfilehash: f37f6fe6211ab05b94249b924eb76c4b98d05082
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939873"
---
# <span data-ttu-id="4d506-101">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4d506-101">Set-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="4d506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d506-102">SYNOPSIS</span></span>
<span data-ttu-id="4d506-103">Bir Azure ağ arabirimi IP yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4d506-103">Sets the goal state for an Azure network interface IP configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d506-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d506-104">SYNTAX</span></span>

### <span data-ttu-id="4d506-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d506-105">SetByResource (Default)</span></span>
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

### <span data-ttu-id="4d506-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4d506-106">SetByResourceId</span></span>
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

## <span data-ttu-id="4d506-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d506-107">DESCRIPTION</span></span>
<span data-ttu-id="4d506-108">**Set-Azurermnetworkınterfaceipconfig** cmdlet 'i, bir Azure ağ arabirimi IP yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4d506-108">The **Set-AzureRmNetworkInterfaceIpConfig** cmdlet sets the goal state for an Azure network interface IP configuration.</span></span>

## <span data-ttu-id="4d506-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d506-109">EXAMPLES</span></span>

### <span data-ttu-id="4d506-110">1: IP yapılandırmasının IP adresini değiştirme</span><span class="sxs-lookup"><span data-stu-id="4d506-110">1: Changing the IP address of an IP configuration</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="4d506-111">İlk iki komut myvnet adlı bir sanal ağ ve mysubnet adlı bir alt ağ alır ve bunu değişkenler $vnet ve $subnet sırayla depolar.</span><span class="sxs-lookup"><span data-stu-id="4d506-111">The first two commands get a virtual network called myvnet and a subnet called mysubnet and store it in the variables $vnet and $subnet respectively.</span></span> <span data-ttu-id="4d506-112">Üçüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="4d506-112">The third command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="4d506-113">Üçüncü komut, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4d506-113">The third command sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11.</span></span> <span data-ttu-id="4d506-114">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4d506-114">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>
    

### <span data-ttu-id="4d506-115">2: bir uygulama güvenliği grubu ile bir IP yapılandırmasını ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="4d506-115">2: Associating an IP configuration with an applicaiton security groupp</span></span>
```
$vnet = Get-AzureRmVirtualNetwork -Name myvnet -ResourceGroupName myrg
$subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name mysubnet -VirtualNetwork $vnet
$asg = Get-ApplicationSecurityGroup -Name myasg -ResourceGroupName myrg

$nic = Get-AzureRmNetworkInterface -Name nic1 -ResourceGroupName myrg

$nic | Set-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -PrivateIpAddress 10.0.0.11 -Subnet $subnet -ApplicationSecurityGroup $asg
    -Primary

$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="4d506-116">Bu örnekte, $asg değişkeni uygulama güvenlik grubuna başvuru içerir.</span><span class="sxs-lookup"><span data-stu-id="4d506-116">In this example, the variable $asg contains a reference to an application security group.</span></span>
<span data-ttu-id="4d506-117">Dördüncü komut, güncelleştirilmesi gereken IP yapılandırmasıyla ilişkili ağ arabirim nic1.</span><span class="sxs-lookup"><span data-stu-id="4d506-117">The fourth command gets the network interface nic1 associated with the IP configuration that needs to be updated.</span></span> <span data-ttu-id="4d506-118">Set-AzureRmNetworkInterfaceIpConfig, birincil IP yapılandırma ipconfig1 özel IP adresini 10.0.0.11 olarak ayarlar ve alınan uygulama güvenlik grubuyla bir ilişki oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d506-118">The Set-AzureRmNetworkInterfaceIpConfig sets the private IP address of the primary IP configuration ipconfig1 to 10.0.0.11 and creates an association with the retrieved application security group.</span></span>
<span data-ttu-id="4d506-119">Son komut son olarak, değişikliklerin başarıyla yapıldığını sağlayan ağ arabirimini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4d506-119">Finally, the last command updates the network interface ensuring the changes have been made successfully.</span></span>

## <span data-ttu-id="4d506-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d506-120">PARAMETERS</span></span>

### <span data-ttu-id="4d506-121">-ApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d506-121">-ApplicationGatewayBackendAddressPool</span></span>
<span data-ttu-id="4d506-122">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-122">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="4d506-123">-Applicationgatewaybackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="4d506-123">-ApplicationGatewayBackendAddressPoolId</span></span>
<span data-ttu-id="4d506-124">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama ağ geçidi arka uç adres havuzu başvurularını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-124">Specifies a collection of application gateway backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="4d506-125">-ApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4d506-125">-ApplicationSecurityGroup</span></span>
<span data-ttu-id="4d506-126">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-126">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="4d506-127">-Applicationsecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="4d506-127">-ApplicationSecurityGroupId</span></span>
<span data-ttu-id="4d506-128">Bu ağ arabirimi IP yapılandırmasının ait olduğu uygulama güvenlik grubu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-128">Specifies a collection of application security group references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="4d506-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d506-129">-DefaultProfile</span></span>
<span data-ttu-id="4d506-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d506-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d506-131">-LoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d506-131">-LoadBalancerBackendAddressPool</span></span>
<span data-ttu-id="4d506-132">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-132">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="4d506-133">-Loadbalancerbackendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="4d506-133">-LoadBalancerBackendAddressPoolId</span></span>
<span data-ttu-id="4d506-134">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici arka uç adres havuzu başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-134">Specifies a collection of load balancer backend address pool references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="4d506-135">-Loadbalancerınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="4d506-135">-LoadBalancerInboundNatRule</span></span>
<span data-ttu-id="4d506-136">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen ağ adresi çevirisi (NAT) kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-136">Specifies a collection of load balancer inbound network address translation (NAT) rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="4d506-137">-Loadbalancerınboundnatruleıd</span><span class="sxs-lookup"><span data-stu-id="4d506-137">-LoadBalancerInboundNatRuleId</span></span>
<span data-ttu-id="4d506-138">Bu ağ arabirimi IP yapılandırmasının ait olduğu yük dengeleyici gelen NAT kuralı başvurularının koleksiyonunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-138">Specifies a collection of load balancer inbound NAT rule references to which this network interface IP configuration belongs.</span></span>

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

### <span data-ttu-id="4d506-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d506-139">-Name</span></span>
<span data-ttu-id="4d506-140">Bu cmdlet 'in ayarladığı ağ IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-140">Specifies the name of the network IP configuration for which this cmdlet sets.</span></span>

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

### <span data-ttu-id="4d506-141">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="4d506-141">-NetworkInterface</span></span>
<span data-ttu-id="4d506-142">Bir **NetworkInterface** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-142">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="4d506-143">Bu cmdlet, bu parametrenin belirttiği nesneye ağ arabirimi IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="4d506-143">This cmdlet adds a network interface IP configuration to the object that this parameter specifies.</span></span>

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

### <span data-ttu-id="4d506-144">-Birincil</span><span class="sxs-lookup"><span data-stu-id="4d506-144">-Primary</span></span>
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

### <span data-ttu-id="4d506-145">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="4d506-145">-PrivateIpAddress</span></span>
<span data-ttu-id="4d506-146">Ağ arabirimi IP yapılandırmasının statik IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-146">Specifies the static IP address of the network interface IP configuration.</span></span>

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

### <span data-ttu-id="4d506-147">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="4d506-147">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="4d506-148">Bir ağ arabirimi IP yapılandırmasının IP adresi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-148">Specifies the IP address version of a network interface IP configuration.</span></span>
<span data-ttu-id="4d506-149">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4d506-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4d506-150">'Ü</span><span class="sxs-lookup"><span data-stu-id="4d506-150">IPv4</span></span>
- <span data-ttu-id="4d506-151">'Yı</span><span class="sxs-lookup"><span data-stu-id="4d506-151">IPv6</span></span>

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

### <span data-ttu-id="4d506-152">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="4d506-152">-PublicIpAddress</span></span>
<span data-ttu-id="4d506-153">**Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-153">Specifies a **PublicIPAddress** object.</span></span>
<span data-ttu-id="4d506-154">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d506-154">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="4d506-155">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="4d506-155">-PublicIpAddressId</span></span>
<span data-ttu-id="4d506-156">Bu cmdlet, bu ağ arabirimi IP yapılandırmasıyla ilişkilendirilecek genel bir IP adresine başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d506-156">This cmdlet creates a reference to a public IP Address to associate with this network interface IP configuration.</span></span>

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

### <span data-ttu-id="4d506-157">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="4d506-157">-Subnet</span></span>
<span data-ttu-id="4d506-158">**Alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d506-158">Specifies a **Subnet** object.</span></span>
<span data-ttu-id="4d506-159">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d506-159">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="4d506-160">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4d506-160">-SubnetId</span></span>
<span data-ttu-id="4d506-161">Bu cmdlet, bu ağ arabirimi IP yapılandırmasının oluşturulduğu alt ağa başvuru oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4d506-161">This cmdlet creates a reference to a subnet in which this network interface IP configuration is created.</span></span>

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

### <span data-ttu-id="4d506-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d506-162">CommonParameters</span></span>
<span data-ttu-id="4d506-163">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d506-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d506-164">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d506-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d506-165">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d506-165">INPUTS</span></span>

### <span data-ttu-id="4d506-166">Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="4d506-166">PSNetworkInterface</span></span>
<span data-ttu-id="4d506-167">Parametre ' NetworkInterface ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="4d506-167">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="4d506-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d506-168">OUTPUTS</span></span>

### <span data-ttu-id="4d506-169">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="4d506-169">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="4d506-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d506-170">NOTES</span></span>
* <span data-ttu-id="4d506-171">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ</span><span class="sxs-lookup"><span data-stu-id="4d506-171">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4d506-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d506-172">RELATED LINKS</span></span>

[<span data-ttu-id="4d506-173">Add-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4d506-173">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4d506-174">Get-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4d506-174">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4d506-175">Yeni-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4d506-175">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4d506-176">Remove-Azurermnetworkınterfaceipconfig</span><span class="sxs-lookup"><span data-stu-id="4d506-176">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)


