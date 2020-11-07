---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancerprobeconfig
schema: 2.0.0
ms.openlocfilehash: 902fa7e266583fe52c516ac3704bdc394215e2c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939886"
---
# <span data-ttu-id="380a7-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="380a7-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="380a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="380a7-102">SYNOPSIS</span></span>
<span data-ttu-id="380a7-103">Bir yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="380a7-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="380a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="380a7-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="380a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="380a7-105">DESCRIPTION</span></span>
<span data-ttu-id="380a7-106">**Set-AzureRmLoadBalancerProbeConfig** cmdlet 'i, bir yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="380a7-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="380a7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="380a7-107">EXAMPLES</span></span>

### <span data-ttu-id="380a7-108">Örnek 1: yük dengeleyicide yoklama yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="380a7-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="380a7-109">İlk komut MyLoadBalancer adındaki loadbalancer 'ı alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="380a7-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="380a7-110">İkinci komut, yük dengeleyiciyi bir şekilde geçirmek için $slb ' a yeni bir yoklama yapılandırması ekleyen-AzureRmLoadBalancerProbeConfig öğesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="380a7-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="380a7-111">Üçüncü komut, yükleme dengeleyicisine, yeni yapılandırmayı ayarlayan **-AzureRmLoadBalancerProbeConfig** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="380a7-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="380a7-112">Geçerli cmdlet 'in gerektirmeleri nedeniyle, önceki komutta belirtilen parametrelerin aynısını belirtmeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="380a7-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="380a7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="380a7-113">PARAMETERS</span></span>

### <span data-ttu-id="380a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380a7-114">-DefaultProfile</span></span>
<span data-ttu-id="380a7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="380a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="380a7-116">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="380a7-116">-IntervalInSeconds</span></span>
<span data-ttu-id="380a7-117">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="380a7-117">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="380a7-118">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="380a7-118">-LoadBalancer</span></span>
<span data-ttu-id="380a7-119">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="380a7-119">Specifies a load balancer.</span></span>
<span data-ttu-id="380a7-120">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="380a7-120">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="380a7-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="380a7-121">-Name</span></span>
<span data-ttu-id="380a7-122">Bu cmdlet 'in ayarladığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="380a7-122">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="380a7-123">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="380a7-123">-Port</span></span>
<span data-ttu-id="380a7-124">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="380a7-124">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="380a7-125">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="380a7-125">-ProbeCount</span></span>
<span data-ttu-id="380a7-126">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="380a7-126">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="380a7-127">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="380a7-127">-Protocol</span></span>
<span data-ttu-id="380a7-128">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="380a7-128">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="380a7-129">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="380a7-129">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="380a7-130">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="380a7-130">-RequestPath</span></span>
<span data-ttu-id="380a7-131">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="380a7-131">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="380a7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380a7-132">CommonParameters</span></span>
<span data-ttu-id="380a7-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="380a7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380a7-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="380a7-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380a7-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="380a7-135">INPUTS</span></span>

### <span data-ttu-id="380a7-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="380a7-136">PSLoadBalancer</span></span>
<span data-ttu-id="380a7-137">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="380a7-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="380a7-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="380a7-138">OUTPUTS</span></span>

### <span data-ttu-id="380a7-139">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="380a7-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="380a7-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="380a7-140">NOTES</span></span>

## <span data-ttu-id="380a7-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="380a7-141">RELATED LINKS</span></span>

[<span data-ttu-id="380a7-142">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="380a7-142">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="380a7-143">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="380a7-143">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="380a7-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="380a7-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="380a7-145">Yeni-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="380a7-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="380a7-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="380a7-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


