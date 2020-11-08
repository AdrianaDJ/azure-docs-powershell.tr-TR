---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: f1f95866721eb5b96e4673ad24a5452b0acdaeb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097976"
---
# <span data-ttu-id="ea0af-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea0af-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ea0af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea0af-102">SYNOPSIS</span></span>
<span data-ttu-id="ea0af-103">Bir yük dengeleyicinin yoklama yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="ea0af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea0af-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea0af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea0af-105">DESCRIPTION</span></span>
<span data-ttu-id="ea0af-106">**Set-AzLoadBalancerProbeConfig** cmdlet 'i bir yük dengeleyicinin yoklama yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="ea0af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea0af-107">EXAMPLES</span></span>

### <span data-ttu-id="ea0af-108">Örnek 1: yük dengeleyicide yoklama yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="ea0af-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="ea0af-109">İlk komut MyLoadBalancer adındaki loadbalancer 'ı alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ea0af-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="ea0af-110">İkinci komut, yük dengeleyiciyi bir şekilde geçirmek için $slb ' a yeni bir yoklama yapılandırması ekleyen-Azloadbalancerloadbalancerconfig öğesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ea0af-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="ea0af-111">Üçüncü komut, yük dengeleyici **Ayarla-AzLoadBalancerProbeConfig** 'e geçirir ve yeni yapılandırmayı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ea0af-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="ea0af-112">Geçerli cmdlet 'in gerektirmeleri nedeniyle, önceki komutta belirtilen parametrelerin aynısını belirtmeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ea0af-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="ea0af-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea0af-113">PARAMETERS</span></span>

### <span data-ttu-id="ea0af-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea0af-114">-DefaultProfile</span></span>
<span data-ttu-id="ea0af-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea0af-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea0af-116">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="ea0af-116">-IntervalInSeconds</span></span>
<span data-ttu-id="ea0af-117">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="ea0af-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea0af-118">-LoadBalancer</span></span>
<span data-ttu-id="ea0af-119">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-119">Specifies a load balancer.</span></span>
<span data-ttu-id="ea0af-120">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin yoklama yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea0af-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea0af-121">-Name</span></span>
<span data-ttu-id="ea0af-122">Bu cmdlet 'in ayarladığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="ea0af-123">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="ea0af-123">-Port</span></span>
<span data-ttu-id="ea0af-124">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="ea0af-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="ea0af-125">-ProbeCount</span></span>
<span data-ttu-id="ea0af-126">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="ea0af-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ea0af-127">-Protocol</span></span>
<span data-ttu-id="ea0af-128">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="ea0af-129">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="ea0af-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0af-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="ea0af-130">-RequestPath</span></span>
<span data-ttu-id="ea0af-131">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea0af-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea0af-132">-Confirm</span></span>
<span data-ttu-id="ea0af-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea0af-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea0af-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea0af-134">-WhatIf</span></span>
<span data-ttu-id="ea0af-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea0af-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea0af-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea0af-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea0af-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea0af-137">CommonParameters</span></span>
<span data-ttu-id="ea0af-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea0af-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea0af-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea0af-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea0af-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea0af-140">INPUTS</span></span>

### <span data-ttu-id="ea0af-141">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea0af-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="ea0af-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ea0af-142">System.String</span></span>

### <span data-ttu-id="ea0af-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ea0af-143">System.Int32</span></span>

## <span data-ttu-id="ea0af-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea0af-144">OUTPUTS</span></span>

### <span data-ttu-id="ea0af-145">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea0af-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ea0af-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea0af-146">NOTES</span></span>

## <span data-ttu-id="ea0af-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea0af-147">RELATED LINKS</span></span>

[<span data-ttu-id="ea0af-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea0af-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ea0af-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ea0af-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ea0af-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea0af-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ea0af-151">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea0af-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ea0af-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ea0af-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

