---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 355DF798-6233-45C6-9416-8AB0E0D7DC02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 3ea89cf0450a5cf24c4299f7eb9c5183195a9663
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932200"
---
# <span data-ttu-id="90b37-101">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90b37-101">Set-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="90b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90b37-102">SYNOPSIS</span></span>
<span data-ttu-id="90b37-103">Bir yük dengeleyici için gelen NAT havuzu yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="90b37-103">Sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="90b37-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90b37-104">SYNTAX</span></span>

### <span data-ttu-id="90b37-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="90b37-105">SetByResource (Default)</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90b37-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="90b37-106">SetByResourceId</span></span>
```
Set-AzLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b37-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="90b37-107">DESCRIPTION</span></span>
<span data-ttu-id="90b37-108">**Set-AzLoadBalancerInboundNatPoolConfig** cmdlet 'i, bir yük DENGELEYICININ gelen NAT havuzu yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="90b37-108">The **Set-AzLoadBalancerInboundNatPoolConfig** cmdlet sets an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="90b37-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90b37-109">EXAMPLES</span></span>

### <span data-ttu-id="90b37-110">1: küme</span><span class="sxs-lookup"><span data-stu-id="90b37-110">1: Set</span></span>
```
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -LoadBalancer $slb
PS C:\> Set-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -LoadBalancer $slb -FrontendIpConfigurationId $inboundNatPoolConfig.FrontendIPConfiguration -Protocol TCP -FrontendPortRangeStart 2001 -FrontendPortRangeEnd 3000 -BackendPort 2001
```

## <span data-ttu-id="90b37-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90b37-111">PARAMETERS</span></span>

### <span data-ttu-id="90b37-112">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="90b37-112">-BackendPort</span></span>
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

### <span data-ttu-id="90b37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b37-113">-DefaultProfile</span></span>
<span data-ttu-id="90b37-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90b37-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90b37-115">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="90b37-115">-EnableFloatingIP</span></span>
<span data-ttu-id="90b37-116">SQL AlwaysOn kullanılabilirlik grubunu yapılandırmak için gereken kayan IP yeteneği için sanal makinenin uç noktasını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="90b37-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="90b37-117">SQL Server 'da SQL AlwaysOn kullanılabilirlik grupları kullanılırken bu ayar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="90b37-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="90b37-118">Uç noktayı oluşturduktan sonra bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="90b37-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="90b37-119">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="90b37-119">-EnableTcpReset</span></span>
<span data-ttu-id="90b37-120">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="90b37-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="90b37-121">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="90b37-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="90b37-122">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="90b37-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="90b37-123">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="90b37-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="90b37-124">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="90b37-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="90b37-125">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="90b37-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="90b37-126">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="90b37-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="90b37-127">TCP boştaki bağlantı için zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="90b37-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="90b37-128">Değer 4 ile 30 dakika arasında ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="90b37-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="90b37-129">Varsayılan değer 4 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="90b37-129">The default value is 4 minutes.</span></span> <span data-ttu-id="90b37-130">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="90b37-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="90b37-131">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90b37-131">-LoadBalancer</span></span>
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

### <span data-ttu-id="90b37-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="90b37-132">-Name</span></span>
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

### <span data-ttu-id="90b37-133">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="90b37-133">-Protocol</span></span>
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

### <span data-ttu-id="90b37-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="90b37-134">-Confirm</span></span>
<span data-ttu-id="90b37-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90b37-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b37-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b37-136">-WhatIf</span></span>
<span data-ttu-id="90b37-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90b37-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90b37-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90b37-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b37-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b37-139">CommonParameters</span></span>
<span data-ttu-id="90b37-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90b37-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b37-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90b37-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b37-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90b37-142">INPUTS</span></span>

### <span data-ttu-id="90b37-143">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90b37-143">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="90b37-144">System. String</span><span class="sxs-lookup"><span data-stu-id="90b37-144">System.String</span></span>

### <span data-ttu-id="90b37-145">System. Int32</span><span class="sxs-lookup"><span data-stu-id="90b37-145">System.Int32</span></span>

### <span data-ttu-id="90b37-146">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="90b37-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="90b37-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90b37-147">OUTPUTS</span></span>

### <span data-ttu-id="90b37-148">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="90b37-148">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="90b37-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90b37-149">NOTES</span></span>

## <span data-ttu-id="90b37-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90b37-150">RELATED LINKS</span></span>

[<span data-ttu-id="90b37-151">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90b37-151">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90b37-152">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90b37-152">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90b37-153">Yeni-Azloadbalancerınboundnatpoolconfig</span><span class="sxs-lookup"><span data-stu-id="90b37-153">New-AzLoadBalancerInboundNatPoolConfig</span></span>](./New-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="90b37-154">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="90b37-154">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)