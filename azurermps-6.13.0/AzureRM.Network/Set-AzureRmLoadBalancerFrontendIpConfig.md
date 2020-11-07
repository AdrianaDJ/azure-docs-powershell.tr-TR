---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 93313b6a2d9623ed518d6e79fabcda8fea5cc7b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762594"
---
# <span data-ttu-id="4b4dd-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4b4dd-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4b4dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b4dd-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4dd-103">Bir yük dengeleyicide ön uç IP yapılandırması için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b4dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b4dd-104">SYNTAX</span></span>

### <span data-ttu-id="4b4dd-105">SetByResourceSubnet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b4dd-105">SetByResourceSubnet (Default)</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b4dd-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="4b4dd-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-PrivateIpAddress <String>] [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b4dd-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="4b4dd-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b4dd-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="4b4dd-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b4dd-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b4dd-109">DESCRIPTION</span></span>
<span data-ttu-id="4b4dd-110">**Set-Azurermloadbalancerfrontendıl** cmdlet 'i, bir Azure Yük dengeleyicideki ön uç IP yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="4b4dd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b4dd-111">EXAMPLES</span></span>

### <span data-ttu-id="4b4dd-112">Örnek 1: yük dengeleyicinin ön uç IP yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4b4dd-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="4b4dd-113">İlk komut, alt ağ adlı sanal alt ağı alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>
<span data-ttu-id="4b4dd-114">İkinci komut MyLoadBalancer adındaki ilişkili yük dengeleyiciyi alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="4b4dd-115">Üçüncü komut, $slb için Newön uç adlı ön uç IP yapılandırması oluşturan-Azurermloadbalancerfrontendıconfıg öğesini $slb yük dengeleyiciden geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>
<span data-ttu-id="4b4dd-116">Dördüncü komut $slb, ön uç IP yapılandırmasını kaydeden ve güncelleştiren **-Azurermloadbalancerfrontendıconfig öğesini ayarlamak** için.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="4b4dd-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b4dd-117">PARAMETERS</span></span>

### <span data-ttu-id="4b4dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4dd-118">-DefaultProfile</span></span>
<span data-ttu-id="4b4dd-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b4dd-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b4dd-120">-LoadBalancer</span></span>
<span data-ttu-id="4b4dd-121">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-121">Specifies a load balancer.</span></span>
<span data-ttu-id="4b4dd-122">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin ön uç yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4b4dd-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b4dd-123">-Name</span></span>
<span data-ttu-id="4b4dd-124">Ayarlanacak ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="4b4dd-125">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="4b4dd-125">-PrivateIpAddress</span></span>
<span data-ttu-id="4b4dd-126">Ayarlanacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="4b4dd-127">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="4b4dd-128">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="4b4dd-128">-PublicIpAddress</span></span>
<span data-ttu-id="4b4dd-129">Ayarlanacak ön uç IP yapılandırmasıyla ilişkili **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="4b4dd-130">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="4b4dd-130">-PublicIpAddressId</span></span>
<span data-ttu-id="4b4dd-131">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasıyla ilişkili **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4b4dd-132">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="4b4dd-132">-Subnet</span></span>
<span data-ttu-id="4b4dd-133">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasını içeren **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4b4dd-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4b4dd-134">-SubnetId</span></span>
<span data-ttu-id="4b4dd-135">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasını içeren alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="4b4dd-136">-Bölge</span><span class="sxs-lookup"><span data-stu-id="4b4dd-136">-Zone</span></span>
<span data-ttu-id="4b4dd-137">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="4b4dd-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b4dd-138">-Confirm</span></span>
<span data-ttu-id="4b4dd-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b4dd-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b4dd-140">-WhatIf</span></span>
<span data-ttu-id="4b4dd-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b4dd-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b4dd-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4dd-143">CommonParameters</span></span>
<span data-ttu-id="4b4dd-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b4dd-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4dd-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4dd-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4dd-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b4dd-146">INPUTS</span></span>

### <span data-ttu-id="4b4dd-147">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b4dd-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="4b4dd-148">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4b4dd-148">Parameters: LoadBalancer (ByValue)</span></span>

### <span data-ttu-id="4b4dd-149">System. Koleksiyonlar. Generic. LIST \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="4b4dd-149">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="4b4dd-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b4dd-150">OUTPUTS</span></span>

### <span data-ttu-id="4b4dd-151">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b4dd-151">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4b4dd-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b4dd-152">NOTES</span></span>

## <span data-ttu-id="4b4dd-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b4dd-153">RELATED LINKS</span></span>

[<span data-ttu-id="4b4dd-154">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="4b4dd-154">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4b4dd-155">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b4dd-155">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4b4dd-156">Get-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="4b4dd-156">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4b4dd-157">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4b4dd-157">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="4b4dd-158">Yeni-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="4b4dd-158">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4b4dd-159">Remove-Azurermloadbalancerfrontendıconfig</span><span class="sxs-lookup"><span data-stu-id="4b4dd-159">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)


