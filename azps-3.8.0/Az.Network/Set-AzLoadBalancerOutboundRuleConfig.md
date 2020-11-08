---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 82e61d3c4a387630dec2c829d651f8d9746a3419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097983"
---
# <span data-ttu-id="4b842-101">Set-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b842-101">Set-AzLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="4b842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b842-102">SYNOPSIS</span></span>
<span data-ttu-id="4b842-103">Bir yük dengeleyici için giden kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b842-103">Sets an outbound rule configuration for a load balancer.</span></span>

## <span data-ttu-id="4b842-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b842-104">SYNTAX</span></span>

### <span data-ttu-id="4b842-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b842-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPool <PSBackendAddressPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b842-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4b842-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <PSResourceId[]> -BackendAddressPoolId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b842-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b842-107">DESCRIPTION</span></span>
<span data-ttu-id="4b842-108">**Set-Azloadbalanceroutboundbir** Azure Yük dengeleyicinin giden kural yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4b842-108">The **Set-AzLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4b842-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b842-109">EXAMPLES</span></span>

### <span data-ttu-id="4b842-110">Örnek 1: yük dengeleyicide giden kural yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="4b842-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="4b842-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4b842-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="4b842-112">İkinci komut, yük dengeleyiciyi bir giden kural yapılandırması ekleyen-AzLoadBalancerOutboundRuleConfig öğesini $slb</span><span class="sxs-lookup"><span data-stu-id="4b842-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="4b842-113">Üçüncü komut yük dengeleyiciden, giden kuralı yapılandırmasını kaydeden ve güncelleştiren **-AzLoadBalancerOutboundRuleConfig** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="4b842-113">The third command passes the load balancer to **Set-AzLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="4b842-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b842-114">PARAMETERS</span></span>

### <span data-ttu-id="4b842-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="4b842-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="4b842-116">NAT için kullanılacak giden bağlantı noktalarının sayısı.</span><span class="sxs-lookup"><span data-stu-id="4b842-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="4b842-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b842-117">-BackendAddressPool</span></span>
<span data-ttu-id="4b842-118">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="4b842-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="4b842-119">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="4b842-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="4b842-120">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="4b842-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="4b842-121">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="4b842-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="4b842-122">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="4b842-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="4b842-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b842-123">-DefaultProfile</span></span>
<span data-ttu-id="4b842-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b842-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b842-125">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="4b842-125">-EnableTcpReset</span></span>
<span data-ttu-id="4b842-126">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="4b842-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="4b842-127">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4b842-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="4b842-128">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="4b842-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="4b842-129">Yük dengeleyicinin ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="4b842-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="4b842-130">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="4b842-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4b842-131">TCP boştaki bağlantının zaman aşımı</span><span class="sxs-lookup"><span data-stu-id="4b842-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="4b842-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b842-132">-LoadBalancer</span></span>
<span data-ttu-id="4b842-133">Yük dengeleyici kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="4b842-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="4b842-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b842-134">-Name</span></span>
<span data-ttu-id="4b842-135">Giden kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="4b842-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="4b842-136">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="4b842-136">-Protocol</span></span>
<span data-ttu-id="4b842-137">Protokol-TCP, UDP veya tümü</span><span class="sxs-lookup"><span data-stu-id="4b842-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="4b842-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b842-138">-Confirm</span></span>
<span data-ttu-id="4b842-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b842-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b842-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b842-140">-WhatIf</span></span>
<span data-ttu-id="4b842-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b842-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b842-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b842-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b842-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b842-143">CommonParameters</span></span>
<span data-ttu-id="4b842-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b842-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b842-145">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b842-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b842-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b842-146">INPUTS</span></span>

### <span data-ttu-id="4b842-147">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b842-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="4b842-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4b842-148">System.Int32</span></span>

### <span data-ttu-id="4b842-149">System. String</span><span class="sxs-lookup"><span data-stu-id="4b842-149">System.String</span></span>

### <span data-ttu-id="4b842-150">Microsoft. Azure. Commands. Network. model. Psresourceıd []</span><span class="sxs-lookup"><span data-stu-id="4b842-150">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

### <span data-ttu-id="4b842-151">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4b842-151">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="4b842-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b842-152">OUTPUTS</span></span>

### <span data-ttu-id="4b842-153">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b842-153">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4b842-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b842-154">NOTES</span></span>

## <span data-ttu-id="4b842-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b842-155">RELATED LINKS</span></span>

[<span data-ttu-id="4b842-156">Add-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b842-156">Add-AzLoadBalancerOutboundRuleConfig</span></span>](./Add-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="4b842-157">Get-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b842-157">Get-AzLoadBalancerOutboundRuleConfig</span></span>](./Get-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="4b842-158">Yeni-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b842-158">New-AzLoadBalancerOutboundRuleConfig</span></span>](./New-AzLoadBalancerOutboundRuleConfig.md)

[<span data-ttu-id="4b842-159">Remove-AzLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b842-159">Remove-AzLoadBalancerOutboundRuleConfig</span></span>](./Remove-AzLoadBalancerOutboundRuleConfig.md)