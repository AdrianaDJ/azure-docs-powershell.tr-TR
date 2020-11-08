---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dbc91068bc208d6ee5a73963ecde00a3d2d9fbb0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097985"
---
# <span data-ttu-id="70bbd-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70bbd-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="70bbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="70bbd-103">Bir yük dengeleyici için gelen NAT havuzu yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="70bbd-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="70bbd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70bbd-104">SYNTAX</span></span>

### <span data-ttu-id="70bbd-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="70bbd-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70bbd-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="70bbd-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70bbd-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="70bbd-107">DESCRIPTION</span></span>
<span data-ttu-id="70bbd-108">**Set-AzLoadBalancerInboundNatPoolConfig** cmdlet 'i, bir yük DENGELEYICININ gelen NAT havuzu yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="70bbd-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="70bbd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70bbd-109">EXAMPLES</span></span>

### <span data-ttu-id="70bbd-110">1: küme</span><span class="sxs-lookup"><span data-stu-id="70bbd-110">1: Set</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
```

## <span data-ttu-id="70bbd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70bbd-111">PARAMETERS</span></span>

### <span data-ttu-id="70bbd-112">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="70bbd-112">-BackendPort</span></span>
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

### <span data-ttu-id="70bbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70bbd-113">-DefaultProfile</span></span>
<span data-ttu-id="70bbd-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="70bbd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70bbd-115">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="70bbd-115">-EnableFloatingIP</span></span>
<span data-ttu-id="70bbd-116">SQL AlwaysOn kullanılabilirlik grubunu yapılandırmak için gereken kayan IP yeteneği için sanal makinenin uç noktasını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="70bbd-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="70bbd-117">SQL Server 'da SQL AlwaysOn kullanılabilirlik grupları kullanılırken bu ayar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="70bbd-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="70bbd-118">Uç noktayı oluşturduktan sonra bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="70bbd-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="70bbd-119">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="70bbd-119">-EnableTcpReset</span></span>
<span data-ttu-id="70bbd-120">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="70bbd-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="70bbd-121">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70bbd-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="70bbd-122">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="70bbd-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="70bbd-123">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="70bbd-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="70bbd-124">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="70bbd-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="70bbd-125">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="70bbd-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="70bbd-126">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="70bbd-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="70bbd-127">TCP boştaki bağlantı için zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="70bbd-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="70bbd-128">Değer 4 ile 30 dakika arasında ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="70bbd-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="70bbd-129">Varsayılan değer 4 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="70bbd-129">The default value is 4 minutes.</span></span> <span data-ttu-id="70bbd-130">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70bbd-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="70bbd-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70bbd-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="70bbd-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="70bbd-132">-Name</span></span>
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

### <span data-ttu-id="70bbd-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="70bbd-133">-Protocol</span></span>
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

### <span data-ttu-id="70bbd-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="70bbd-134">-Confirm</span></span>
<span data-ttu-id="70bbd-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="70bbd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70bbd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70bbd-136">-WhatIf</span></span>
<span data-ttu-id="70bbd-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="70bbd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70bbd-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="70bbd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70bbd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70bbd-139">CommonParameters</span></span>
<span data-ttu-id="70bbd-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70bbd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70bbd-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70bbd-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70bbd-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70bbd-142">INPUTS</span></span>

### <span data-ttu-id="70bbd-143">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70bbd-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="70bbd-144">System. String</span><span class="sxs-lookup"><span data-stu-id="70bbd-144">System.String</span></span>

### <span data-ttu-id="70bbd-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="70bbd-145">System.Int32</span></span>

### <span data-ttu-id="70bbd-146">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="70bbd-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="70bbd-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70bbd-147">OUTPUTS</span></span>

### <span data-ttu-id="70bbd-148">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="70bbd-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="70bbd-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70bbd-149">NOTES</span></span>

## <span data-ttu-id="70bbd-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70bbd-150">RELATED LINKS</span></span>

[<span data-ttu-id="70bbd-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70bbd-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="70bbd-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70bbd-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="70bbd-153">Yeni-Azloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="70bbd-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="70bbd-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="70bbd-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)
