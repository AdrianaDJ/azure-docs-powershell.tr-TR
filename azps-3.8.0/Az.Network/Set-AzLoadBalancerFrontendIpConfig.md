---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 62a479dd0c9c622100f5880c1aaf46836e179c53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096149"
---
# <span data-ttu-id="cb6a1-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="cb6a1-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="cb6a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6a1-103">Bir yük dengeleyicinin ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="cb6a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb6a1-104">SYNTAX</span></span>

### <span data-ttu-id="cb6a1-105">SetByResourceSubnet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb6a1-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6a1-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="cb6a1-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6a1-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="cb6a1-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb6a1-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="cb6a1-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb6a1-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb6a1-109">DESCRIPTION</span></span>
<span data-ttu-id="cb6a1-110">**Set-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir yük dengeleyicinin ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="cb6a1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb6a1-111">EXAMPLES</span></span>

### <span data-ttu-id="cb6a1-112">Örnek 1: yük dengeleyicinin ön uç IP yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="cb6a1-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="cb6a1-113">İlk komut, alt ağ adlı sanal alt ağı alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="cb6a1-114">İkinci komut MyLoadBalancer adındaki ilişkili yük dengeleyiciyi alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="cb6a1-115">Üçüncü komut, $slb için Newön uç adlı ön uç IP yapılandırması oluşturan-Azloadbalancerfrontendıconfıg öğesini $slb</span><span class="sxs-lookup"><span data-stu-id="cb6a1-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="cb6a1-116">Dördüncü komut $slb ' de, ön uç IP yapılandırmasını kaydeden ve güncelleştiren **-Azloadbalancerfrontendıconfig** 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="cb6a1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb6a1-117">PARAMETERS</span></span>

### <span data-ttu-id="cb6a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb6a1-118">-DefaultProfile</span></span>
<span data-ttu-id="cb6a1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb6a1-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cb6a1-120">-LoadBalancer</span></span>
<span data-ttu-id="cb6a1-121">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-121">Specifies a load balancer.</span></span>
<span data-ttu-id="cb6a1-122">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin ön uç yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="cb6a1-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb6a1-123">-Name</span></span>
<span data-ttu-id="cb6a1-124">Ayarlanacak ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="cb6a1-125">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="cb6a1-125">-PrivateIpAddress</span></span>
<span data-ttu-id="cb6a1-126">Ayarlanacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="cb6a1-127">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="cb6a1-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="cb6a1-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="cb6a1-129">IP yapılandırmasının özel IP adresi sürümü.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="cb6a1-130">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="cb6a1-130">-PublicIpAddress</span></span>
<span data-ttu-id="cb6a1-131">Ayarlanacak ön uç IP yapılandırmasıyla ilişkili **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-131">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="cb6a1-132">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="cb6a1-132">-PublicIpAddressId</span></span>
<span data-ttu-id="cb6a1-133">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasıyla ilişkili **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-133">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="cb6a1-134">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="cb6a1-134">-Subnet</span></span>
<span data-ttu-id="cb6a1-135">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasını içeren **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-135">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="cb6a1-136">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cb6a1-136">-SubnetId</span></span>
<span data-ttu-id="cb6a1-137">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasını içeren alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-137">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="cb6a1-138">-Bölge</span><span class="sxs-lookup"><span data-stu-id="cb6a1-138">-Zone</span></span>
<span data-ttu-id="cb6a1-139">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-139">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="cb6a1-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb6a1-140">-Confirm</span></span>
<span data-ttu-id="cb6a1-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb6a1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb6a1-142">-WhatIf</span></span>
<span data-ttu-id="cb6a1-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cb6a1-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb6a1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6a1-145">CommonParameters</span></span>
<span data-ttu-id="cb6a1-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6a1-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cb6a1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6a1-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb6a1-148">INPUTS</span></span>

### <span data-ttu-id="cb6a1-149">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cb6a1-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="cb6a1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cb6a1-150">System.String</span></span>

### <span data-ttu-id="cb6a1-151">System. String []</span><span class="sxs-lookup"><span data-stu-id="cb6a1-151">System.String[]</span></span>

### <span data-ttu-id="cb6a1-152">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="cb6a1-152">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="cb6a1-153">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="cb6a1-153">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="cb6a1-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb6a1-154">OUTPUTS</span></span>

### <span data-ttu-id="cb6a1-155">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cb6a1-155">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="cb6a1-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb6a1-156">NOTES</span></span>

## <span data-ttu-id="cb6a1-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb6a1-157">RELATED LINKS</span></span>

[<span data-ttu-id="cb6a1-158">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="cb6a1-158">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cb6a1-159">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="cb6a1-159">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="cb6a1-160">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="cb6a1-160">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cb6a1-161">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cb6a1-161">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="cb6a1-162">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="cb6a1-162">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="cb6a1-163">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="cb6a1-163">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


