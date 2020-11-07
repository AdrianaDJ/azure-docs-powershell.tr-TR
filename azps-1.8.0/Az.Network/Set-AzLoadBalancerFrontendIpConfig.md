---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: f1c6790ba733004a565087b261e0ca9b42f9688b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760009"
---
# <span data-ttu-id="da0d6-101">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="da0d6-101">Set-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="da0d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="da0d6-103">Bir yük dengeleyicinin ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-103">Updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="da0d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da0d6-104">SYNTAX</span></span>

### <span data-ttu-id="da0d6-105">SetByResourceSubnet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="da0d6-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da0d6-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="da0d6-106">SetByResourceIdSubnet</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-PrivateIpAddress <String>]
 [-Zone <String[]>] -SubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da0d6-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="da0d6-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddressId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da0d6-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="da0d6-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Zone <String[]>]
 -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da0d6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="da0d6-109">DESCRIPTION</span></span>
<span data-ttu-id="da0d6-110">**Set-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir yük dengeleyicinin ön uç IP yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-110">The **Set-AzLoadBalancerFrontendIpConfig** cmdlet updates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="da0d6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da0d6-111">EXAMPLES</span></span>

### <span data-ttu-id="da0d6-112">Örnek 1: yük dengeleyicinin ön uç IP yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="da0d6-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="da0d6-113">İlk komut, alt ağ adlı sanal alt ağı alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="da0d6-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="da0d6-114">İkinci komut MyLoadBalancer adındaki ilişkili yük dengeleyiciyi alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="da0d6-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="da0d6-115">Üçüncü komut, $slb için Newön uç adlı ön uç IP yapılandırması oluşturan-Azloadbalancerfrontendıconfıg öğesini $slb</span><span class="sxs-lookup"><span data-stu-id="da0d6-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="da0d6-116">Dördüncü komut $slb ' de, ön uç IP yapılandırmasını kaydeden ve güncelleştiren **-Azloadbalancerfrontendıconfig** 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-116">The fourth command passes the load balancer in $slb to **Set-AzLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="da0d6-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da0d6-117">PARAMETERS</span></span>

### <span data-ttu-id="da0d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da0d6-118">-DefaultProfile</span></span>
<span data-ttu-id="da0d6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da0d6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da0d6-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da0d6-120">-LoadBalancer</span></span>
<span data-ttu-id="da0d6-121">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-121">Specifies a load balancer.</span></span>
<span data-ttu-id="da0d6-122">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin ön uç yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-122">This cmdlet updates a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="da0d6-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="da0d6-123">-Name</span></span>
<span data-ttu-id="da0d6-124">Ayarlanacak ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="da0d6-125">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="da0d6-125">-PrivateIpAddress</span></span>
<span data-ttu-id="da0d6-126">Ayarlanacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="da0d6-127">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="da0d6-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="da0d6-128">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="da0d6-128">-PublicIpAddress</span></span>
<span data-ttu-id="da0d6-129">Ayarlanacak ön uç IP yapılandırmasıyla ilişkili **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="da0d6-130">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="da0d6-130">-PublicIpAddressId</span></span>
<span data-ttu-id="da0d6-131">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasıyla ilişkili **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="da0d6-132">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="da0d6-132">-Subnet</span></span>
<span data-ttu-id="da0d6-133">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasını içeren **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="da0d6-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="da0d6-134">-SubnetId</span></span>
<span data-ttu-id="da0d6-135">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasını içeren alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="da0d6-136">-Bölge</span><span class="sxs-lookup"><span data-stu-id="da0d6-136">-Zone</span></span>
<span data-ttu-id="da0d6-137">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="da0d6-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="da0d6-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="da0d6-138">-Confirm</span></span>
<span data-ttu-id="da0d6-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="da0d6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da0d6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da0d6-140">-WhatIf</span></span>
<span data-ttu-id="da0d6-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="da0d6-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da0d6-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="da0d6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da0d6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0d6-143">CommonParameters</span></span>
<span data-ttu-id="da0d6-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da0d6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0d6-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da0d6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0d6-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da0d6-146">INPUTS</span></span>

### <span data-ttu-id="da0d6-147">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da0d6-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="da0d6-148">System. String</span><span class="sxs-lookup"><span data-stu-id="da0d6-148">System.String</span></span>

### <span data-ttu-id="da0d6-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="da0d6-149">System.String[]</span></span>

### <span data-ttu-id="da0d6-150">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="da0d6-150">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="da0d6-151">Microsoft. Azure. Commands. Network. model. Pspublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="da0d6-151">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="da0d6-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da0d6-152">OUTPUTS</span></span>

### <span data-ttu-id="da0d6-153">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da0d6-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="da0d6-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da0d6-154">NOTES</span></span>

## <span data-ttu-id="da0d6-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da0d6-155">RELATED LINKS</span></span>

[<span data-ttu-id="da0d6-156">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="da0d6-156">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da0d6-157">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="da0d6-157">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="da0d6-158">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="da0d6-158">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da0d6-159">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="da0d6-159">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="da0d6-160">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="da0d6-160">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="da0d6-161">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="da0d6-161">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)


