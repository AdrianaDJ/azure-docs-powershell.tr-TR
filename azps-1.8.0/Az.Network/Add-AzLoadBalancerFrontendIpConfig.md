---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 07FF274A-F365-44E5-A66B-6740CD165664
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 2dba7d00ea308225736de6714c90c74b0ce30837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760711"
---
# <span data-ttu-id="b1eb5-101">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b1eb5-101">Add-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b1eb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="b1eb5-103">Bir yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-103">Adds a front-end IP configuration to a load balancer.</span></span>

## <span data-ttu-id="b1eb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1eb5-104">SYNTAX</span></span>

### <span data-ttu-id="b1eb5-105">SetByResourceSubnet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1eb5-105">SetByResourceSubnet (Default)</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1eb5-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="b1eb5-106">SetByResourceIdSubnet</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1eb5-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b1eb5-107">SetByResourceIdPublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1eb5-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b1eb5-108">SetByResourcePublicIpAddress</span></span>
```
Add-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1eb5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1eb5-109">DESCRIPTION</span></span>
<span data-ttu-id="b1eb5-110">**Add-AzLoadBalancerFrontendIpConifg** cmdlet 'ı bir Azure yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-110">The **Add-AzLoadBalancerFrontendIpConifg** cmdlet adds a front-end IP configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="b1eb5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1eb5-111">EXAMPLES</span></span>

### <span data-ttu-id="b1eb5-112">Örnek 1 dinamik IP adresi olan ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="b1eb5-112">Example 1 Add a front-end IP configuration with a dynamic IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyRg" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet | Set-AzLoadBalancer
```

<span data-ttu-id="b1eb5-113">İlk komut MyVnet adlı Azure sanal ağını alır ve MySubnet adlı alt ağı almak için ardışık düzeni **Get-AzVirtualNetworkSubnetConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-113">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="b1eb5-114">Bu komut, sonucu $Subnet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-114">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="b1eb5-115">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu, $MySubnet adlı değişkende depolanan alt ağdan dinamik bir IP adresi içeren bir ön uç IP yapılandırması olan **Add-Azloadbalancerfrontendıconfıg** cmdlet 'ine iletir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-115">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a dynamic private IP address from the subnet stored in the variable named $MySubnet.</span></span>

### <span data-ttu-id="b1eb5-116">Örnek 2 statik IP adresi olan ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="b1eb5-116">Example 2 Add a front-end IP configuration with a static IP address</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "RG001" | Get-AzVirtualNetworkSubnetConfig -Name "MySubnet"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Subnet $Subnet -PrivateIpAddress "10.0.1.6" | Set-AzLoadBalancer
```

<span data-ttu-id="b1eb5-117">İlk komut MyVnet adlı Azure sanal ağını alır ve MySubnet adlı alt ağı almak için ardışık düzeni **Get-AzVirtualNetworkSubnetConfig** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-117">The first command gets the Azure virtual network named MyVnet and passes the result using the pipeline to the **Get-AzVirtualNetworkSubnetConfig** cmdlet to get the subnet named MySubnet.</span></span>
<span data-ttu-id="b1eb5-118">Bu komut, sonucu $Subnet adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-118">The command then stores the result in the variable named $Subnet.</span></span>
<span data-ttu-id="b1eb5-119">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu, $Subnet adlı değişkende depolanan alt ağdan statik özel IP adresi olan bir ön uç IP **yapılandırması ekleyerek yük** dengeleyicisine geçirir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-119">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with a static private IP address from the subnet stored in the variable named $Subnet.</span></span>

### <span data-ttu-id="b1eb5-120">Örnek 3 genel IP adresiyle ön uç IP yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="b1eb5-120">Example 3 Add a front-end IP configuration with a public IP address</span></span>
```
PS C:\>$PublicIp = Get-AzPublicIpAddress -ResourceGroupName "myRG" -Name "MyPub"
PS C:\> Get-AzLoadBalancer -Name "MyLB" -ResourceGroupName "NrpTest" | Add-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -PublicIpAddress $PublicIp | Set-AzLoadBalancer
```

<span data-ttu-id="b1eb5-121">İlk komut, MyPub adlı Azure genel IP adresini alır ve sonucu $PublicIp adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-121">The first command gets the Azure public IP address named MyPub and stores the result in the variable named $PublicIp.</span></span>
<span data-ttu-id="b1eb5-122">İkinci komut MyLB adındaki yük dengeleyiciyi alır ve sonucu $PublicIp adlı değişkende depolanan genel IP adresiyle yük dengeleyicisine ön uç IP yapılandırması ekleyen **Add-Azloadbalancerfrontendıconfıg** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-122">The second command gets the load balancer named MyLB and passes the result to the **Add-AzLoadBalancerFrontendIpConfig** cmdlet that adds a front-end IP configuration to the load balancer with public IP address stored in the variable named $PublicIp.</span></span>

## <span data-ttu-id="b1eb5-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1eb5-123">PARAMETERS</span></span>

### <span data-ttu-id="b1eb5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1eb5-124">-DefaultProfile</span></span>
<span data-ttu-id="b1eb5-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1eb5-126">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b1eb5-126">-LoadBalancer</span></span>
<span data-ttu-id="b1eb5-127">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-127">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="b1eb5-128">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine ön uç IP yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-128">This cmdlet adds a front-end IP configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1eb5-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1eb5-129">-Name</span></span>
<span data-ttu-id="b1eb5-130">Eklenecek ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-130">Specifies the name of the front-end IP configuration to add.</span></span>

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

### <span data-ttu-id="b1eb5-131">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="b1eb5-131">-PrivateIpAddress</span></span>
<span data-ttu-id="b1eb5-132">Ön uç IP yapılandırmasıyla ilişkilendirilecek özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-132">Specifies the private IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b1eb5-133">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b1eb5-133">-PublicIpAddress</span></span>
<span data-ttu-id="b1eb5-134">Ön uç IP yapılandırmasıyla ilişkilendirilecek ortak IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-134">Specifies the public IP address to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b1eb5-135">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="b1eb5-135">-PublicIpAddressId</span></span>
<span data-ttu-id="b1eb5-136">Ön uç IP yapılandırmasının ekleneceği genel IP adresinin KIMLIĞINI verir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-136">Specifes the ID of the public IP address in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b1eb5-137">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="b1eb5-137">-Subnet</span></span>
<span data-ttu-id="b1eb5-138">Ön uç IP yapılandırmasının ekleneceği alt ağ nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-138">Specifies the subnet object in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b1eb5-139">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b1eb5-139">-SubnetId</span></span>
<span data-ttu-id="b1eb5-140">Ön uç IP yapılandırmasının ekleneceği alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-140">Specifies the ID of the subnet in which to add a front-end IP configuration.</span></span>

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

### <span data-ttu-id="b1eb5-141">-Bölge</span><span class="sxs-lookup"><span data-stu-id="b1eb5-141">-Zone</span></span>
<span data-ttu-id="b1eb5-142">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-142">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b1eb5-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="b1eb5-143">-Confirm</span></span>
<span data-ttu-id="b1eb5-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1eb5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1eb5-145">-WhatIf</span></span>
<span data-ttu-id="b1eb5-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1eb5-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1eb5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1eb5-148">CommonParameters</span></span>
<span data-ttu-id="b1eb5-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1eb5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1eb5-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1eb5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1eb5-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1eb5-151">INPUTS</span></span>

### <span data-ttu-id="b1eb5-152">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b1eb5-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b1eb5-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b1eb5-153">System.String</span></span>

### <span data-ttu-id="b1eb5-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="b1eb5-154">System.String[]</span></span>

### <span data-ttu-id="b1eb5-155">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b1eb5-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b1eb5-156">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b1eb5-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="b1eb5-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1eb5-157">OUTPUTS</span></span>

### <span data-ttu-id="b1eb5-158">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b1eb5-158">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b1eb5-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1eb5-159">NOTES</span></span>

## <span data-ttu-id="b1eb5-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1eb5-160">RELATED LINKS</span></span>

[<span data-ttu-id="b1eb5-161">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="b1eb5-161">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b1eb5-162">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b1eb5-162">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="b1eb5-163">Get-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="b1eb5-163">Get-AzVirtualNetworkSubnetConfig</span></span>](./Get-AzVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="b1eb5-164">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="b1eb5-164">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b1eb5-165">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="b1eb5-165">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b1eb5-166">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="b1eb5-166">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


