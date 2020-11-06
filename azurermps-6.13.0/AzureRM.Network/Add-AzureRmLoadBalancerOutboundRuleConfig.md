---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: ac96a07fb7ec32589ac351fc592c4c2848e75978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588080"
---
# <span data-ttu-id="c544a-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c544a-101">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="c544a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c544a-102">SYNOPSIS</span></span>
<span data-ttu-id="c544a-103">Bir yük dengeleyicisine giden kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="c544a-103">Adds an outbound rule configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c544a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c544a-104">SYNTAX</span></span>

### <span data-ttu-id="c544a-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c544a-105">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c544a-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="c544a-106">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c544a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c544a-107">DESCRIPTION</span></span>
<span data-ttu-id="c544a-108">**Add-AzureRmLoadBalancerOutboundRuleConfig** cmdlet 'i, bir Azure yük dengeleyicisine giden bir kural yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="c544a-108">The **Add-AzureRmLoadBalancerOutboundRuleConfig** cmdlet adds an outbound rule configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="c544a-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c544a-109">EXAMPLES</span></span>

### <span data-ttu-id="c544a-110">Örnek 1: yük dengeleyicisine giden kural yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="c544a-110">Example 1: Add an outbound rule configuration to a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0]
```

<span data-ttu-id="c544a-111">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c544a-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c544a-112">İkinci komut, yük dengeleyiciyi bir giden kural yapılandırması ekleyen **-AzureRmLoadBalancerOutboundRuleConfig** öğesini $SLB</span><span class="sxs-lookup"><span data-stu-id="c544a-112">The second command uses the pipeline operator to pass the load balancer in $slb to **Add-AzureRmLoadBalancerOutboundRuleConfig** , which adds an outbound rule configuration to the load balancer.</span></span>

## <span data-ttu-id="c544a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c544a-113">PARAMETERS</span></span>

### <span data-ttu-id="c544a-114">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="c544a-114">-AllocatedOutboundPort</span></span>
<span data-ttu-id="c544a-115">NAT için kullanılacak giden bağlantı noktalarının sayısı.</span><span class="sxs-lookup"><span data-stu-id="c544a-115">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="c544a-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c544a-116">-BackendAddressPool</span></span>
<span data-ttu-id="c544a-117">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="c544a-117">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c544a-118">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="c544a-118">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c544a-119">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="c544a-119">-BackendAddressPoolId</span></span>
<span data-ttu-id="c544a-120">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="c544a-120">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="c544a-121">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="c544a-121">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="c544a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c544a-122">-DefaultProfile</span></span>
<span data-ttu-id="c544a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c544a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c544a-124">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="c544a-124">-EnableTcpReset</span></span>
<span data-ttu-id="c544a-125">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="c544a-125">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="c544a-126">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c544a-126">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="c544a-127">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="c544a-127">-FrontendIpConfiguration</span></span>
<span data-ttu-id="c544a-128">Yük dengeleyicinin ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="c544a-128">The Frontend IP addresses of the load balancer.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c544a-129">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="c544a-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="c544a-130">TCP boştaki bağlantının zaman aşımı</span><span class="sxs-lookup"><span data-stu-id="c544a-130">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="c544a-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c544a-131">-LoadBalancer</span></span>
<span data-ttu-id="c544a-132">Yük dengeleyici kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="c544a-132">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="c544a-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="c544a-133">-Name</span></span>
<span data-ttu-id="c544a-134">Giden kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="c544a-134">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="c544a-135">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="c544a-135">-Protocol</span></span>
<span data-ttu-id="c544a-136">Protokol-TCP, UDP veya tümü</span><span class="sxs-lookup"><span data-stu-id="c544a-136">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="c544a-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="c544a-137">-Confirm</span></span>
<span data-ttu-id="c544a-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c544a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c544a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c544a-139">-WhatIf</span></span>
<span data-ttu-id="c544a-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c544a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c544a-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c544a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c544a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c544a-142">CommonParameters</span></span>
<span data-ttu-id="c544a-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c544a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c544a-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c544a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c544a-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c544a-145">INPUTS</span></span>

### <span data-ttu-id="c544a-146">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c544a-146">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="c544a-147">System. Int32 System. String System. Koleksiyonlar. Generic. List \` 1 [[Microsoft. Azure. Commands. Network. modeller. Psresourceıd, Microsoft. Azure. Commands. Network, Version = 6.5.0.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Network. modeller. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c544a-147">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c544a-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c544a-148">OUTPUTS</span></span>

### <span data-ttu-id="c544a-149">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c544a-149">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c544a-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c544a-150">NOTES</span></span>

## <span data-ttu-id="c544a-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c544a-151">RELATED LINKS</span></span>
