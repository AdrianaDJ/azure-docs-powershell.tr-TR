---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 5c9a70399cc50b773e492410b951b7959e8ade60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096511"
---
# <span data-ttu-id="0fb2b-101">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0fb2b-101">Add-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="0fb2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fb2b-103">Bir yük dengeleyicisine gelen NAT havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-103">Adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="0fb2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0fb2b-104">SYNTAX</span></span>

### <span data-ttu-id="0fb2b-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0fb2b-105">SetByResource (Default)</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fb2b-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="0fb2b-106">SetByResourceId</span></span>
```
Add-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fb2b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0fb2b-107">DESCRIPTION</span></span>
<span data-ttu-id="0fb2b-108">**Add-AzLoadBalancerInboundNatPoolConfig** cmdlet 'i, bir yük dengeleyicisine gelen NAT havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-108">The **Add-AzLoadBalancerInboundNatPoolConfig** cmdlet adds an inbound NAT pool to a load balancer.</span></span>

## <span data-ttu-id="0fb2b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0fb2b-109">EXAMPLES</span></span>

### <span data-ttu-id="0fb2b-110">1: ekleme</span><span class="sxs-lookup"><span data-stu-id="0fb2b-110">1: Add</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="0fb2b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0fb2b-111">PARAMETERS</span></span>

### <span data-ttu-id="0fb2b-112">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="0fb2b-112">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb2b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fb2b-113">-DefaultProfile</span></span>
<span data-ttu-id="0fb2b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fb2b-115">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="0fb2b-115">-EnableFloatingIP</span></span>
<span data-ttu-id="0fb2b-116">SQL AlwaysOn kullanılabilirlik grubunu yapılandırmak için gereken kayan IP yeteneği için sanal makinenin uç noktasını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="0fb2b-117">SQL Server 'da SQL AlwaysOn kullanılabilirlik grupları kullanılırken bu ayar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="0fb2b-118">Uç noktayı oluşturduktan sonra bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="0fb2b-119">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="0fb2b-119">-EnableTcpReset</span></span>
<span data-ttu-id="0fb2b-120">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="0fb2b-121">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0fb2b-122">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="0fb2b-122">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb2b-123">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="0fb2b-123">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb2b-124">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="0fb2b-124">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb2b-125">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="0fb2b-125">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fb2b-126">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="0fb2b-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0fb2b-127">TCP boştaki bağlantı için zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="0fb2b-128">Değer 4 ile 30 dakika arasında ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="0fb2b-129">Varsayılan değer 4 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-129">The default value is 4 minutes.</span></span> <span data-ttu-id="0fb2b-130">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0fb2b-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0fb2b-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="0fb2b-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="0fb2b-132">-Name</span></span>
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

### <span data-ttu-id="0fb2b-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="0fb2b-133">-Protocol</span></span>
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

### <span data-ttu-id="0fb2b-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="0fb2b-134">-Confirm</span></span>
<span data-ttu-id="0fb2b-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fb2b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fb2b-136">-WhatIf</span></span>
<span data-ttu-id="0fb2b-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fb2b-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fb2b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fb2b-139">CommonParameters</span></span>
<span data-ttu-id="0fb2b-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0fb2b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fb2b-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fb2b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fb2b-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0fb2b-142">INPUTS</span></span>

### <span data-ttu-id="0fb2b-143">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0fb2b-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="0fb2b-144">System. String</span><span class="sxs-lookup"><span data-stu-id="0fb2b-144">System.String</span></span>

### <span data-ttu-id="0fb2b-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0fb2b-145">System.Int32</span></span>

### <span data-ttu-id="0fb2b-146">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="0fb2b-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="0fb2b-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0fb2b-147">OUTPUTS</span></span>

### <span data-ttu-id="0fb2b-148">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0fb2b-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0fb2b-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0fb2b-149">NOTES</span></span>

## <span data-ttu-id="0fb2b-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0fb2b-150">RELATED LINKS</span></span>

[<span data-ttu-id="0fb2b-151">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0fb2b-151">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="0fb2b-152">Yeni-Azloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="0fb2b-152">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="0fb2b-153">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0fb2b-153">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="0fb2b-154">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0fb2b-154">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
