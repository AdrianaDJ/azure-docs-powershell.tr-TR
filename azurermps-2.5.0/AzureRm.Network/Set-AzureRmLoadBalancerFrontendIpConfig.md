---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C23BEF37-D472-43EC-90AA-F8742247ABA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 8de9d162ceba8dc436d5244f75011b79a949ddeb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939888"
---
# <span data-ttu-id="b592c-101">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="b592c-101">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="b592c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b592c-102">SYNOPSIS</span></span>
<span data-ttu-id="b592c-103">Bir yük dengeleyicide ön uç IP yapılandırması için hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b592c-103">Sets the goal state for a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b592c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b592c-104">SYNTAX</span></span>

### <span data-ttu-id="b592c-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="b592c-105">SetByResourceSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -Subnet <PSSubnet> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b592c-106">Setbyresourceıdsubnet</span><span class="sxs-lookup"><span data-stu-id="b592c-106">SetByResourceIdSubnet</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-PrivateIpAddress <String>] -SubnetId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b592c-107">Setbyresourceidpublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b592c-107">SetByResourceIdPublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddressId <String> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b592c-108">Setbyresourcepublicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b592c-108">SetByResourcePublicIpAddress</span></span>
```
Set-AzureRmLoadBalancerFrontendIpConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 -PublicIpAddress <PSPublicIpAddress> [-Zone <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b592c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b592c-109">DESCRIPTION</span></span>
<span data-ttu-id="b592c-110">**Set-Azurermloadbalancerfrontendıl** cmdlet 'i, bir Azure Yük dengeleyicideki ön uç IP yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b592c-110">The **Set-AzureRmLoadBalancerFrontendIpConfig** cmdlet sets the goal state for a front-end IP configuration in an Azure load balancer.</span></span>

## <span data-ttu-id="b592c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b592c-111">EXAMPLES</span></span>

### <span data-ttu-id="b592c-112">Örnek 1: yük dengeleyicinin ön uç IP yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="b592c-112">Example 1: Modify the front-end IP configuration of a load balancer</span></span>
```
PS C:\>$Subnet = Get-AzureRmVirtualNetwork -Name "MyVnet" -ResourceGroupName "MyResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet"
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
PS C:\> $slb | Set-AzureRmLoadBalancerFrontendIpConfig -Name "NewFrontend" -Subnet $Subnet
```

<span data-ttu-id="b592c-113">İlk komut, alt ağ adlı sanal alt ağı alır ve $Subnet değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b592c-113">The first command gets the virtual subnet named Subnet, and then stores it in the $Subnet variable.</span></span>

<span data-ttu-id="b592c-114">İkinci komut MyLoadBalancer adındaki ilişkili yük dengeleyiciyi alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b592c-114">The second command gets the associated load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="b592c-115">Üçüncü komut, $slb için Newön uç adlı ön uç IP yapılandırması oluşturan-Azurermloadbalancerfrontendıconfıg öğesini $slb yük dengeleyiciden geçirmek için ardışık düzen işlecini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b592c-115">The third command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerFrontendIpConfig, which creates a front-end IP configuration named NewFrontend for $slb.</span></span>

<span data-ttu-id="b592c-116">Dördüncü komut $slb, ön uç IP yapılandırmasını kaydeden ve güncelleştiren **-Azurermloadbalancerfrontendıconfig öğesini ayarlamak** için.</span><span class="sxs-lookup"><span data-stu-id="b592c-116">The fourth command passes the load balancer in $slb to **Set-AzureRmLoadBalancerFrontendIpConfig** , which saves and updates the front-end IP configuration.</span></span>

## <span data-ttu-id="b592c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b592c-117">PARAMETERS</span></span>

### <span data-ttu-id="b592c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b592c-118">-DefaultProfile</span></span>
<span data-ttu-id="b592c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b592c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b592c-120">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b592c-120">-LoadBalancer</span></span>
<span data-ttu-id="b592c-121">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="b592c-121">Specifies a load balancer.</span></span>
<span data-ttu-id="b592c-122">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin ön uç yapılandırması için hedef durumu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b592c-122">This cmdlet sets the goal state for a front-end configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b592c-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="b592c-123">-Name</span></span>
<span data-ttu-id="b592c-124">Ayarlanacak ön uç IP yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b592c-124">Specifies the name of the front-end IP configuration to set.</span></span>

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

### <span data-ttu-id="b592c-125">-Privateıpaddress</span><span class="sxs-lookup"><span data-stu-id="b592c-125">-PrivateIpAddress</span></span>
<span data-ttu-id="b592c-126">Ayarlanacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicinin özel IP adresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b592c-126">Specifies the private IP address of the load balancer that is associated with the front-end IP configuration to set.</span></span>
<span data-ttu-id="b592c-127">Bu parametreyi yalnızca, *alt ağ* parametresini de belirtmeniz durumunda belirtin.</span><span class="sxs-lookup"><span data-stu-id="b592c-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b592c-128">-Publicıpaddress</span><span class="sxs-lookup"><span data-stu-id="b592c-128">-PublicIpAddress</span></span>
<span data-ttu-id="b592c-129">Ayarlanacak ön uç IP yapılandırmasıyla ilişkili **Publicıpaddress** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b592c-129">Specifies the **PublicIpAddress** object that is associated with the front-end IP configuration to set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b592c-130">-Publicıpadresisıd</span><span class="sxs-lookup"><span data-stu-id="b592c-130">-PublicIpAddressId</span></span>
<span data-ttu-id="b592c-131">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasıyla ilişkili **Publicıpaddress** nesnesinin kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b592c-131">Specifies the ID of the **PublicIpAddress** object that is associated with the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b592c-132">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="b592c-132">-Subnet</span></span>
<span data-ttu-id="b592c-133">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasını içeren **alt ağ** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b592c-133">Specifies the **Subnet** object that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b592c-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b592c-134">-SubnetId</span></span>
<span data-ttu-id="b592c-135">Bu cmdlet 'in ayarladığı ön uç IP yapılandırmasını içeren alt ağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b592c-135">Specifies the ID of the subnet that contains the front-end IP configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b592c-136">-Bölge</span><span class="sxs-lookup"><span data-stu-id="b592c-136">-Zone</span></span>
<span data-ttu-id="b592c-137">Kaynağın gelmesi gerektiğini belirten kullanılabilirlik bölgelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="b592c-137">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b592c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b592c-138">CommonParameters</span></span>
<span data-ttu-id="b592c-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b592c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b592c-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b592c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b592c-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b592c-141">INPUTS</span></span>

### <span data-ttu-id="b592c-142">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b592c-142">PSLoadBalancer</span></span>
<span data-ttu-id="b592c-143">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b592c-143">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b592c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b592c-144">OUTPUTS</span></span>

### <span data-ttu-id="b592c-145">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b592c-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b592c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b592c-146">NOTES</span></span>

## <span data-ttu-id="b592c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b592c-147">RELATED LINKS</span></span>

[<span data-ttu-id="b592c-148">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="b592c-148">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b592c-149">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b592c-149">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="b592c-150">Get-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="b592c-150">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b592c-151">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b592c-151">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="b592c-152">Yeni-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="b592c-152">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="b592c-153">Remove-Azurermloadbalancerfrontendıconfig</span><span class="sxs-lookup"><span data-stu-id="b592c-153">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

