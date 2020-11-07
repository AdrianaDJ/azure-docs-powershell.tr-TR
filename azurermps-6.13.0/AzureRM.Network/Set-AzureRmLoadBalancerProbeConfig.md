---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 3fe5345e6d3cbad90d99f5a94e72873beaca7c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762794"
---
# <span data-ttu-id="79acb-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79acb-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="79acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79acb-102">SYNOPSIS</span></span>
<span data-ttu-id="79acb-103">Bir yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="79acb-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79acb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79acb-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79acb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="79acb-105">DESCRIPTION</span></span>
<span data-ttu-id="79acb-106">**Set-AzureRmLoadBalancerProbeConfig** cmdlet 'i, bir yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="79acb-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="79acb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79acb-107">EXAMPLES</span></span>

### <span data-ttu-id="79acb-108">Örnek 1: yük dengeleyicide yoklama yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="79acb-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="79acb-109">İlk komut MyLoadBalancer adındaki loadbalancer 'ı alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="79acb-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>
<span data-ttu-id="79acb-110">İkinci komut, yük dengeleyiciyi bir şekilde geçirmek için $slb ' a yeni bir yoklama yapılandırması ekleyen-AzureRmLoadBalancerProbeConfig öğesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="79acb-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>
<span data-ttu-id="79acb-111">Üçüncü komut, yükleme dengeleyicisine, yeni yapılandırmayı ayarlayan **-AzureRmLoadBalancerProbeConfig** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="79acb-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="79acb-112">Geçerli cmdlet 'in gerektirmeleri nedeniyle, önceki komutta belirtilen parametrelerin aynısını belirtmeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="79acb-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="79acb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79acb-113">PARAMETERS</span></span>

### <span data-ttu-id="79acb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79acb-114">-DefaultProfile</span></span>
<span data-ttu-id="79acb-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79acb-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79acb-116">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="79acb-116">-IntervalInSeconds</span></span>
<span data-ttu-id="79acb-117">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="79acb-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="79acb-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79acb-118">-LoadBalancer</span></span>
<span data-ttu-id="79acb-119">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="79acb-119">Specifies a load balancer.</span></span>
<span data-ttu-id="79acb-120">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="79acb-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="79acb-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="79acb-121">-Name</span></span>
<span data-ttu-id="79acb-122">Bu cmdlet 'in ayarladığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79acb-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="79acb-123">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="79acb-123">-Port</span></span>
<span data-ttu-id="79acb-124">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79acb-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="79acb-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="79acb-125">-ProbeCount</span></span>
<span data-ttu-id="79acb-126">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="79acb-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="79acb-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="79acb-127">-Protocol</span></span>
<span data-ttu-id="79acb-128">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="79acb-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="79acb-129">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="79acb-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="79acb-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="79acb-130">-RequestPath</span></span>
<span data-ttu-id="79acb-131">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="79acb-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="79acb-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="79acb-132">-Confirm</span></span>
<span data-ttu-id="79acb-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79acb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79acb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79acb-134">-WhatIf</span></span>
<span data-ttu-id="79acb-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79acb-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79acb-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79acb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79acb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79acb-137">CommonParameters</span></span>
<span data-ttu-id="79acb-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79acb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79acb-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79acb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79acb-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79acb-140">INPUTS</span></span>

### <span data-ttu-id="79acb-141">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79acb-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="79acb-142">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79acb-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="79acb-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79acb-143">OUTPUTS</span></span>

### <span data-ttu-id="79acb-144">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79acb-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="79acb-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79acb-145">NOTES</span></span>

## <span data-ttu-id="79acb-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79acb-146">RELATED LINKS</span></span>

[<span data-ttu-id="79acb-147">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79acb-147">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="79acb-148">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79acb-148">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="79acb-149">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79acb-149">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="79acb-150">Yeni-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79acb-150">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="79acb-151">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="79acb-151">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


