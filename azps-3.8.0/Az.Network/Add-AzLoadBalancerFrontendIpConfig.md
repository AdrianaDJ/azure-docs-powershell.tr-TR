---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 7596dff276a4913dd1c322ad023ebfb32b8e1aac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096519"
---
# <span data-ttu-id="dee8f-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="dee8f-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="dee8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dee8f-102">SYNOPSIS</span></span>
<span data-ttu-id="dee8f-103">Bir yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="dee8f-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="dee8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dee8f-104">SYNTAX</span></span>

### <span data-ttu-id="dee8f-105">SetByResourceSubnet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dee8f-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dee8f-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="dee8f-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dee8f-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="dee8f-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dee8f-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="dee8f-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dee8f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="dee8f-109">DESCRIPTION</span></span>
<span data-ttu-id="dee8f-110">**Add-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir Azure yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="dee8f-110">The **Add-AzLoadBalancerFrontendIpConfig** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="dee8f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dee8f-111">EXAMPLES</span></span>

### <span data-ttu-id="dee8f-112">Örnek 1 dinamik IP adresi olan ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="dee8f-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="dee8f-113">İlk komut MyVnet adlı Azure sanal ağını alır ve MySubnet adlı alt ağı almak için ardışık düzeni **Get-AzVirtualNetworkSubnetConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="dee8f-114">Bu komut, sonucu $Subnet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="dee8f-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="dee8f-115">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu, $MySubnet adlı değişkende depolanan alt ağdan dinamik bir IP adresi içeren bir ön uç IP yapılandırması olan **Add-Azloadbalancerfrontendıconfıg** cmdlet 'ine iletir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="dee8f-116">Örnek 2 statik IP adresi olan ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="dee8f-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="dee8f-117">İlk komut MyVnet adlı Azure sanal ağını alır ve MySubnet adlı alt ağı almak için ardışık düzeni **Get-AzVirtualNetworkSubnetConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="dee8f-118">Bu komut, sonucu $Subnet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="dee8f-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="dee8f-119">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu, $Subnet adlı değişkende depolanan alt ağdan statik özel IP adresi olan bir ön uç IP **yapılandırması ekleyerek yük** dengeleyicisine geçirir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="dee8f-120">Örnek 3 genel IP adresiyle ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="dee8f-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="dee8f-121">İlk komut, MyPub adlı Azure genel IP adresini alır ve sonucu $PublicIp adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="dee8f-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="dee8f-122">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu $PublicIp adlı değişkende depolanan genel IP adresiyle yük dengeleyicisine ön uç IP yapılandırması ekleyen **Add-Azloadbalancerfrontendıconfıg** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="dee8f-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dee8f-123">PARAMETERS</span></span>

### <span data-ttu-id="dee8f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee8f-124">-DefaultProfile</span></span>
<span data-ttu-id="dee8f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dee8f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dee8f-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dee8f-126">-LoadBalancer</span></span>
<span data-ttu-id="dee8f-127">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="dee8f-128">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="dee8f-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="dee8f-129">-Name</span></span>
<span data-ttu-id="dee8f-130">Eklenecek ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="dee8f-131">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="dee8f-131">-PrivateIpAddress</span></span>
<span data-ttu-id="dee8f-132">Ön uç IP yapılandırmasıyla ilişkilendirilecek özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-133">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="dee8f-133">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="dee8f-134">IP yapılandırmasının özel IP adresi sürümü.</span><span class="sxs-lookup"><span data-stu-id="dee8f-134">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-135">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="dee8f-135">-PublicIpAddress</span></span>
<span data-ttu-id="dee8f-136">Ön uç IP yapılandırmasıyla ilişkilendirilecek ortak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-136">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-137">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="dee8f-137">-PublicIpAddressId</span></span>
<span data-ttu-id="dee8f-138">Ön uç IP yapılandırmasının ekleneceği ortak IP adresinin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-138">Specifies the ID of the public IP address in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-139">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="dee8f-139">-Subnet</span></span>
<span data-ttu-id="dee8f-140">Ön uç IP yapılandırmasının ekleneceği alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-140">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-141">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="dee8f-141">-SubnetId</span></span>
<span data-ttu-id="dee8f-142">Ön uç IP yapılandırmasının ekleneceği alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-142">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-143">-Bölge</span><span class="sxs-lookup"><span data-stu-id="dee8f-143">-Zone</span></span>
<span data-ttu-id="dee8f-144">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="dee8f-144">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="dee8f-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="dee8f-145">-Confirm</span></span>
<span data-ttu-id="dee8f-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dee8f-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dee8f-147">-WhatIf</span></span>
<span data-ttu-id="dee8f-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dee8f-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dee8f-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dee8f-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dee8f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee8f-150">CommonParameters</span></span>
<span data-ttu-id="dee8f-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dee8f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee8f-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dee8f-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee8f-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dee8f-153">INPUTS</span></span>

### <span data-ttu-id="dee8f-154">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dee8f-154">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="dee8f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="dee8f-155">System.String</span></span>

### <span data-ttu-id="dee8f-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="dee8f-156">System.String[]</span></span>

### <span data-ttu-id="dee8f-157">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="dee8f-157">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="dee8f-158">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="dee8f-158">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="dee8f-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dee8f-159">OUTPUTS</span></span>

### <span data-ttu-id="dee8f-160">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="dee8f-160">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="dee8f-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dee8f-161">NOTES</span></span>

## <span data-ttu-id="dee8f-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dee8f-162">RELATED LINKS</span></span>

[<span data-ttu-id="dee8f-163">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="dee8f-163">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dee8f-164">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="dee8f-164">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="dee8f-165">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="dee8f-165">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="dee8f-166">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="dee8f-166">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dee8f-167">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="dee8f-167">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="dee8f-168">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="dee8f-168">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


