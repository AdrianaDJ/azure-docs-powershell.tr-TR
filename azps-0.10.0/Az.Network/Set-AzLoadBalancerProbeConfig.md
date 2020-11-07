---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a14196a98be2f901cc120926e716efe884a747a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936534"
---
# <span data-ttu-id="d79a8-101">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d79a8-101">Set-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="d79a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d79a8-103">Bir yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d79a8-103">Sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="d79a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d79a8-104">SYNTAX</span></span>

```
Set-AzLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d79a8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d79a8-105">DESCRIPTION</span></span>
<span data-ttu-id="d79a8-106">**Set-AzLoadBalancerProbeConfig** cmdlet 'i, bir yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d79a8-106">The **Set-AzLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="d79a8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d79a8-107">EXAMPLES</span></span>

### <span data-ttu-id="d79a8-108">Örnek 1: yük dengeleyicide yoklama yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="d79a8-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="d79a8-109">İlk komut MyLoadBalancer adındaki loadbalancer 'ı alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d79a8-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="d79a8-110">İkinci komut, yük dengeleyiciyi bir şekilde geçirmek için $slb ' a yeni bir yoklama yapılandırması ekleyen-Azloadbalancerloadbalancerconfig öğesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d79a8-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="d79a8-111">Üçüncü komut, yük dengeleyici **Ayarla-AzLoadBalancerProbeConfig** 'e geçirir ve yeni yapılandırmayı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d79a8-111">The third command passes the load balancer to **Set-AzLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="d79a8-112">Geçerli cmdlet 'in gerektirmeleri nedeniyle, önceki komutta belirtilen parametrelerin aynısını belirtmeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d79a8-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="d79a8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d79a8-113">PARAMETERS</span></span>

### <span data-ttu-id="d79a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79a8-114">-DefaultProfile</span></span>
<span data-ttu-id="d79a8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d79a8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a8-116">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="d79a8-116">-IntervalInSeconds</span></span>
<span data-ttu-id="d79a8-117">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79a8-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a8-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d79a8-118">-LoadBalancer</span></span>
<span data-ttu-id="d79a8-119">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79a8-119">Specifies a load balancer.</span></span>
<span data-ttu-id="d79a8-120">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d79a8-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d79a8-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="d79a8-121">-Name</span></span>
<span data-ttu-id="d79a8-122">Bu cmdlet 'in ayarladığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79a8-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a8-123">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="d79a8-123">-Port</span></span>
<span data-ttu-id="d79a8-124">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79a8-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a8-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="d79a8-125">-ProbeCount</span></span>
<span data-ttu-id="d79a8-126">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79a8-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a8-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="d79a8-127">-Protocol</span></span>
<span data-ttu-id="d79a8-128">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79a8-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="d79a8-129">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="d79a8-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a8-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="d79a8-130">-RequestPath</span></span>
<span data-ttu-id="d79a8-131">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79a8-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79a8-132">CommonParameters</span></span>
<span data-ttu-id="d79a8-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d79a8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79a8-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79a8-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79a8-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d79a8-135">INPUTS</span></span>

### <span data-ttu-id="d79a8-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d79a8-136">PSLoadBalancer</span></span>
<span data-ttu-id="d79a8-137">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d79a8-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d79a8-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d79a8-138">OUTPUTS</span></span>

### <span data-ttu-id="d79a8-139">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d79a8-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d79a8-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d79a8-140">NOTES</span></span>

## <span data-ttu-id="d79a8-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d79a8-141">RELATED LINKS</span></span>

[<span data-ttu-id="d79a8-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d79a8-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="d79a8-143">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d79a8-143">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d79a8-144">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d79a8-144">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="d79a8-145">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d79a8-145">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="d79a8-146">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="d79a8-146">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)


