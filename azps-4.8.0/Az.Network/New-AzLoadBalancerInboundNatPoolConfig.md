---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: dfc0e6616113a163771d214a7ebe7f8df593173c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265999"
---
# <span data-ttu-id="ff0c8-101">New-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ff0c8-101">New-AzLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="ff0c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ff0c8-103">Bir yük dengeleyici için gelen NAT havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-103">Creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="ff0c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff0c8-104">SYNTAX</span></span>

### <span data-ttu-id="ff0c8-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ff0c8-105">SetByResource (Default)</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff0c8-106">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="ff0c8-106">SetByResourceId</span></span>
```
New-AzLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff0c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff0c8-107">DESCRIPTION</span></span>
<span data-ttu-id="ff0c8-108">**Yeni-Azloadbalancerınboundnatpoolconfig** cmdlet 'i, bir yük dengeleyici IÇIN gelen NAT havuzu yapılandırmasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-108">The **New-AzLoadBalancerInboundNatPoolConfig** cmdlet creates an inbound NAT pool configuration for a load balancer.</span></span>

## <span data-ttu-id="ff0c8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff0c8-109">EXAMPLES</span></span>

### <span data-ttu-id="ff0c8-110">Örnek 1: yeni</span><span class="sxs-lookup"><span data-stu-id="ff0c8-110">Example 1: New</span></span>
```powershell
PS C:\> $slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="ff0c8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff0c8-111">PARAMETERS</span></span>

### <span data-ttu-id="ff0c8-112">-Backendbağlantınoktası</span><span class="sxs-lookup"><span data-stu-id="ff0c8-112">-BackendPort</span></span>
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

### <span data-ttu-id="ff0c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff0c8-113">-DefaultProfile</span></span>
<span data-ttu-id="ff0c8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff0c8-115">-Enabsolloatingip</span><span class="sxs-lookup"><span data-stu-id="ff0c8-115">-EnableFloatingIP</span></span>
<span data-ttu-id="ff0c8-116">SQL AlwaysOn kullanılabilirlik grubunu yapılandırmak için gereken kayan IP yeteneği için sanal makinenin uç noktasını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-116">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="ff0c8-117">SQL Server 'da SQL AlwaysOn kullanılabilirlik grupları kullanılırken bu ayar gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-117">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="ff0c8-118">Uç noktayı oluşturduktan sonra bu ayar değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-118">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="ff0c8-119">-Enabletcönayar</span><span class="sxs-lookup"><span data-stu-id="ff0c8-119">-EnableTcpReset</span></span>
<span data-ttu-id="ff0c8-120">TCP akışı boşta durma zaman aşımından veya beklenmeyen bağlantı sonlandırmasına iki yönlü TCP sıfırlama alma.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-120">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="ff0c8-121">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-121">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ff0c8-122">-Frontendıyapılandırma</span><span class="sxs-lookup"><span data-stu-id="ff0c8-122">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="ff0c8-123">-Frontendıconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="ff0c8-123">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="ff0c8-124">-Frontenvseçportrangeend</span><span class="sxs-lookup"><span data-stu-id="ff0c8-124">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="ff0c8-125">-Frontenvseçportrangestart</span><span class="sxs-lookup"><span data-stu-id="ff0c8-125">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="ff0c8-126">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="ff0c8-126">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ff0c8-127">TCP boştaki bağlantı için zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-127">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="ff0c8-128">Değer 4 ile 30 dakika arasında ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-128">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="ff0c8-129">Varsayılan değer 4 dakikadır.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-129">The default value is 4 minutes.</span></span> <span data-ttu-id="ff0c8-130">Bu öğe yalnızca protokol TCP olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-130">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="ff0c8-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff0c8-131">-Name</span></span>
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

### <span data-ttu-id="ff0c8-132">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ff0c8-132">-Protocol</span></span>
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

### <span data-ttu-id="ff0c8-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff0c8-133">-Confirm</span></span>
<span data-ttu-id="ff0c8-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff0c8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff0c8-135">-WhatIf</span></span>
<span data-ttu-id="ff0c8-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ff0c8-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff0c8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff0c8-138">CommonParameters</span></span>
<span data-ttu-id="ff0c8-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff0c8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff0c8-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff0c8-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff0c8-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff0c8-141">INPUTS</span></span>

### <span data-ttu-id="ff0c8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ff0c8-142">System.String</span></span>

### <span data-ttu-id="ff0c8-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ff0c8-143">System.Int32</span></span>

### <span data-ttu-id="ff0c8-144">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="ff0c8-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="ff0c8-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff0c8-145">OUTPUTS</span></span>

### <span data-ttu-id="ff0c8-146">Microsoft. Azure. Commands. Network. model. Psınboundnatpool</span><span class="sxs-lookup"><span data-stu-id="ff0c8-146">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="ff0c8-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff0c8-147">NOTES</span></span>

## <span data-ttu-id="ff0c8-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff0c8-148">RELATED LINKS</span></span>

[<span data-ttu-id="ff0c8-149">Add-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ff0c8-149">Add-AzLoadBalancerInboundNatPoolConfig</span></span>](./Add-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ff0c8-150">Get-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ff0c8-150">Get-AzLoadBalancerInboundNatPoolConfig</span></span>](./Get-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ff0c8-151">Remove-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ff0c8-151">Remove-AzLoadBalancerInboundNatPoolConfig</span></span>](./Remove-AzLoadBalancerInboundNatPoolConfig.md)

[<span data-ttu-id="ff0c8-152">Set-AzLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ff0c8-152">Set-AzLoadBalancerInboundNatPoolConfig</span></span>](./Set-AzLoadBalancerInboundNatPoolConfig.md)
