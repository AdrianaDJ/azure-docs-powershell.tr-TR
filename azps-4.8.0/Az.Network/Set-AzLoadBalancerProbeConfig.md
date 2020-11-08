---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: d0e3d2b11f79dee858849935d71872f1f1b2dd7f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108835"
---
# <span data-ttu-id="5e93b-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e93b-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="5e93b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e93b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e93b-103">Bir yük dengeleyicinin yoklama yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-103">Updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="5e93b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e93b-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e93b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e93b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e93b-106">**Set-AzLoadBalancerProbeConfig** cmdlet 'i bir yük dengeleyicinin yoklama yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-106">The **Set-AzLoadBalancerProbeConfig** cmdlet updates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="5e93b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e93b-107">EXAMPLES</span></span>

### <span data-ttu-id="5e93b-108">Örnek 1: yük dengeleyicide yoklama yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="5e93b-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="5e93b-109">İlk komut MyLoadBalancer adındaki loadbalancer 'ı alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5e93b-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="5e93b-110">İkinci komut, yük dengeleyiciyi bir şekilde geçirmek için $slb ' a yeni bir yoklama yapılandırması ekleyen-Azloadbalancerloadbalancerconfig öğesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5e93b-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="5e93b-111">Üçüncü komut, yük dengeleyici **Ayarla-AzLoadBalancerProbeConfig** 'e geçirir ve yeni yapılandırmayı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5e93b-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="5e93b-112">Geçerli cmdlet 'in gerektirmeleri nedeniyle, önceki komutta belirtilen parametrelerin aynısını belirtmeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5e93b-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="5e93b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e93b-113">PARAMETERS</span></span>

### <span data-ttu-id="5e93b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e93b-114">-DefaultProfile</span></span>
<span data-ttu-id="5e93b-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e93b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e93b-116">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="5e93b-116">-IntervalInSeconds</span></span>
<span data-ttu-id="5e93b-117">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="5e93b-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5e93b-118">-LoadBalancer</span></span>
<span data-ttu-id="5e93b-119">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-119">Specifies a load balancer.</span></span>
<span data-ttu-id="5e93b-120">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin yoklama yapılandırmasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-120">This cmdlet updates a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e93b-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e93b-121">-Name</span></span>
<span data-ttu-id="5e93b-122">Bu cmdlet 'in ayarladığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="5e93b-123">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="5e93b-123">-Port</span></span>
<span data-ttu-id="5e93b-124">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="5e93b-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="5e93b-125">-ProbeCount</span></span>
<span data-ttu-id="5e93b-126">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="5e93b-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="5e93b-127">-Protocol</span></span>
<span data-ttu-id="5e93b-128">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="5e93b-129">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="5e93b-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="5e93b-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="5e93b-130">-RequestPath</span></span>
<span data-ttu-id="5e93b-131">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="5e93b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="5e93b-132">-Confirm</span></span>
<span data-ttu-id="5e93b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5e93b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e93b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e93b-134">-WhatIf</span></span>
<span data-ttu-id="5e93b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e93b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e93b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5e93b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e93b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e93b-137">CommonParameters</span></span>
<span data-ttu-id="5e93b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e93b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e93b-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e93b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e93b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e93b-140">INPUTS</span></span>

### <span data-ttu-id="5e93b-141">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5e93b-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="5e93b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5e93b-142">System.String</span></span>

### <span data-ttu-id="5e93b-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5e93b-143">System.Int32</span></span>

## <span data-ttu-id="5e93b-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e93b-144">OUTPUTS</span></span>

### <span data-ttu-id="5e93b-145">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5e93b-145">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="5e93b-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e93b-146">NOTES</span></span>

## <span data-ttu-id="5e93b-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e93b-147">RELATED LINKS</span></span>

[<span data-ttu-id="5e93b-148">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e93b-148">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5e93b-149">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="5e93b-149">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="5e93b-150">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e93b-150">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5e93b-151">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e93b-151">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="5e93b-152">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5e93b-152">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


