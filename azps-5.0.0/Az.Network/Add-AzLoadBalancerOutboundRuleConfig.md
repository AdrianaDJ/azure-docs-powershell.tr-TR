---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ca7c581a2cc3710403dae9aff0c0afda450dbbae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325930"
---
# <span data-ttu-id="bbc3f-101">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc3f-101">Add-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="bbc3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbc3f-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc3f-103">Bir yük dengeleyicisine giden kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-103">Adds an outbound rule configuration to a load balancer.</span></span>

## <span data-ttu-id="bbc3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbc3f-104">SYNTAX</span></span>

### <span data-ttu-id="bbc3f-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbc3f-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc3f-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="bbc3f-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbc3f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbc3f-107">DESCRIPTION</span></span>
<span data-ttu-id="bbc3f-108">**Add-Azloadbalanceroutboundbir** , Azure yük dengeleyicisine giden bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-108">The **Add-AzLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="bbc3f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbc3f-109">EXAMPLES</span></span>

### <span data-ttu-id="bbc3f-110">Örnek 1: yük dengeleyicisine giden kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="bbc3f-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="bbc3f-111">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="bbc3f-112">İkinci komut, yük dengeleyiciyi bir giden kural yapılandırması ekleyen **-AzLoadBalancerOutboundRuleConfig** öğesini $SLB</span><span class="sxs-lookup"><span data-stu-id="bbc3f-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="bbc3f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbc3f-113">PARAMETERS</span></span>

### <span data-ttu-id="bbc3f-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="bbc3f-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="bbc3f-115">NAT için kullanılacak giden bağlantı noktalarının sayısı.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-115">The number of outbound ports to be used for NAT.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc3f-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbc3f-116">-BackendAddressPool</span></span>
<span data-ttu-id="bbc3f-117">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="bbc3f-118">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc3f-119">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="bbc3f-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="bbc3f-120">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="bbc3f-121">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc3f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc3f-122">-DefaultProfile</span></span>
<span data-ttu-id="bbc3f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbc3f-124">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="bbc3f-124">-EnableTcpReset</span></span>
<span data-ttu-id="bbc3f-125">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="bbc3f-126">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-126">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc3f-127">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="bbc3f-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="bbc3f-128">Yük dengeleyicinin ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc3f-129">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="bbc3f-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="bbc3f-130">TCP boştaki bağlantının zaman aşımı</span><span class="sxs-lookup"><span data-stu-id="bbc3f-130">The timeout for the TCP idle connection</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc3f-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbc3f-131">-LoadBalancer</span></span>
<span data-ttu-id="bbc3f-132">Yük dengeleyici kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="bbc3f-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="bbc3f-133">-Name</span></span>
<span data-ttu-id="bbc3f-134">Giden kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="bbc3f-135">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="bbc3f-135">-Protocol</span></span>
<span data-ttu-id="bbc3f-136">Protokol-TCP, UDP veya tümü</span><span class="sxs-lookup"><span data-stu-id="bbc3f-136">Protocol - TCP, UDP or All</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbc3f-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="bbc3f-137">-Confirm</span></span>
<span data-ttu-id="bbc3f-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbc3f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc3f-139">-WhatIf</span></span>
<span data-ttu-id="bbc3f-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbc3f-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbc3f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc3f-142">CommonParameters</span></span>
<span data-ttu-id="bbc3f-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbc3f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc3f-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbc3f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc3f-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbc3f-145">INPUTS</span></span>

### <span data-ttu-id="bbc3f-146">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbc3f-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="bbc3f-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bbc3f-147">System.Int32</span></span>

### <span data-ttu-id="bbc3f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="bbc3f-148">System.String</span></span>

### <span data-ttu-id="bbc3f-149">Microsoft. Azure. Commands. Network. model. Psresourceıd []</span><span class="sxs-lookup"><span data-stu-id="bbc3f-149">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="bbc3f-150">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="bbc3f-150">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="bbc3f-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbc3f-151">OUTPUTS</span></span>

### <span data-ttu-id="bbc3f-152">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bbc3f-152">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="bbc3f-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbc3f-153">NOTES</span></span>

## <span data-ttu-id="bbc3f-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbc3f-154">RELATED LINKS</span></span>

[<span data-ttu-id="bbc3f-155">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc3f-155">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="bbc3f-156">Yeni-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc3f-156">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="bbc3f-157">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc3f-157">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="bbc3f-158">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbc3f-158">Set-AzLoadBalancerOutboundRuleConfig</span></span>](./Set-AzLoadBalancerOutboundRuleConfig.md)
