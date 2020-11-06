---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1c813a7ac23ae8bc161f10df02ac618d5f6a7a81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591347"
---
# <span data-ttu-id="83804-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="83804-101">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="83804-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83804-102">SYNOPSIS</span></span>
<span data-ttu-id="83804-103">Bir yük dengeleyici için giden kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83804-103">Sets an outbound rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83804-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83804-104">SYNTAX</span></span>

### <span data-ttu-id="83804-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="83804-105">SetByResource (Default)</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPool <PSBackendAddressPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="83804-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="83804-106">SetByResourceId</span></span>
```
Set-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-AllocatedOutboundPort <Int32>] -Protocol <String> [-EnableTcpReset] [-IdleTimeoutInMinutes <Int32>]
 -FrontendIpConfiguration <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSResourceId]>
 -BackendAddressPoolId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83804-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="83804-107">DESCRIPTION</span></span>
<span data-ttu-id="83804-108">**Set-AzureRmLoadBalancerOutboundRuleConfig** cmdlet 'i, bir Azure yük dengeleyicisi için giden kuralı yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="83804-108">The **Set-AzureRmLoadBalancerOutboundRuleConfig** cmdlet sets an outbound rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="83804-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83804-109">EXAMPLES</span></span>

### <span data-ttu-id="83804-110">Örnek 1: yük dengeleyicide giden kural yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="83804-110">Example 1: Modify the outbound rule configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>$slb | Add-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 5
PS C:\>$slb | Set-AzureRmLoadBalancerOutboundRuleConfig -Name "NewRule" -Protocol "Tcp" -FrontendIPConfiguration $slb.FrontendIpConfigurations[0] -BackendAddressPool $slb.BackendAddressPools[0] -IdleTimeoutInMinutes 10
```

<span data-ttu-id="83804-111">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="83804-111">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="83804-112">İkinci $slb komut, bir giden kuralı yapılandırmasını ekleyen-AzureRmLoadBalancerOutboundRuleConfig öğesini ekleme</span><span class="sxs-lookup"><span data-stu-id="83804-112">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerOutboundRuleConfig, which adds an outbound rule configuration to it.</span></span>
<span data-ttu-id="83804-113">Üçüncü komut yük dengeleyiciden, giden kuralı yapılandırmasını kaydeden ve güncelleştiren **-AzureRmLoadBalancerOutboundRuleConfig** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="83804-113">The third command passes the load balancer to **Set-AzureRmLoadBalancerOutboundRuleConfig** , which saves and updates the outbound rule configuration.</span></span>

## <span data-ttu-id="83804-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83804-114">PARAMETERS</span></span>

### <span data-ttu-id="83804-115">-AllocatedOutboundPort</span><span class="sxs-lookup"><span data-stu-id="83804-115">-AllocatedOutboundPort</span></span>
<span data-ttu-id="83804-116">NAT için kullanılacak giden bağlantı noktalarının sayısı.</span><span class="sxs-lookup"><span data-stu-id="83804-116">The number of outbound ports to be used for NAT.</span></span>

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

### <span data-ttu-id="83804-117">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="83804-117">-BackendAddressPool</span></span>
<span data-ttu-id="83804-118">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="83804-118">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="83804-119">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="83804-119">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="83804-120">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="83804-120">-BackendAddressPoolId</span></span>
<span data-ttu-id="83804-121">Bir DIP havuzuna başvuru.</span><span class="sxs-lookup"><span data-stu-id="83804-121">A reference to a pool of DIPs.</span></span>
<span data-ttu-id="83804-122">Giden trafik, arka uç IP 'lerde, IP 'Ler genelinde rasgele yük dengelemesi yapılır.</span><span class="sxs-lookup"><span data-stu-id="83804-122">Outbound traffic is randomly load balanced across IPs in the backend IPs.</span></span>

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

### <span data-ttu-id="83804-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83804-123">-DefaultProfile</span></span>
<span data-ttu-id="83804-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="83804-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83804-125">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="83804-125">-EnableTcpReset</span></span>
<span data-ttu-id="83804-126">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="83804-126">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span>
<span data-ttu-id="83804-127">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="83804-127">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="83804-128">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="83804-128">-FrontendIpConfiguration</span></span>
<span data-ttu-id="83804-129">Yük dengeleyicinin ön uç IP adresleri.</span><span class="sxs-lookup"><span data-stu-id="83804-129">The Frontend IP addresses of the load balancer.</span></span>

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

### <span data-ttu-id="83804-130">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="83804-130">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="83804-131">TCP boştaki bağlantının zaman aşımı</span><span class="sxs-lookup"><span data-stu-id="83804-131">The timeout for the TCP idle connection</span></span>

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

### <span data-ttu-id="83804-132">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83804-132">-LoadBalancer</span></span>
<span data-ttu-id="83804-133">Yük dengeleyici kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="83804-133">The reference of the load balancer resource.</span></span>

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

### <span data-ttu-id="83804-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="83804-134">-Name</span></span>
<span data-ttu-id="83804-135">Giden kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="83804-135">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="83804-136">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="83804-136">-Protocol</span></span>
<span data-ttu-id="83804-137">Protokol-TCP, UDP veya tümü</span><span class="sxs-lookup"><span data-stu-id="83804-137">Protocol - TCP, UDP or All</span></span>

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

### <span data-ttu-id="83804-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="83804-138">-Confirm</span></span>
<span data-ttu-id="83804-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="83804-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83804-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83804-140">-WhatIf</span></span>
<span data-ttu-id="83804-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83804-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83804-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="83804-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83804-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83804-143">CommonParameters</span></span>
<span data-ttu-id="83804-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83804-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83804-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83804-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83804-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83804-146">INPUTS</span></span>

### <span data-ttu-id="83804-147">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83804-147">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="83804-148">System. Int32 System. String System. Koleksiyonlar. Generic. List \` 1 [[Microsoft. Azure. Commands. Network. modeller. Psresourceıd, Microsoft. Azure. Commands. Network, Version = 6.5.0.0, Culture = neutral, PublicKeyToken = null]] Microsoft. Azure. Commands. Network. modeller. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="83804-148">System.Int32 System.String System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSResourceId, Microsoft.Azure.Commands.Network, Version=6.5.0.0, Culture=neutral, PublicKeyToken=null]] Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="83804-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83804-149">OUTPUTS</span></span>

### <span data-ttu-id="83804-150">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="83804-150">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="83804-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83804-151">NOTES</span></span>

## <span data-ttu-id="83804-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83804-152">RELATED LINKS</span></span>
