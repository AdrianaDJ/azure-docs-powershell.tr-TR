---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C8B91455-C1A7-43BD-9E63-A20E2694371F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 9a6999dc379a5a39acea9b17107cabf2cae5ee25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589240"
---
# <span data-ttu-id="a33cb-101">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a33cb-101">Set-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a33cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a33cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a33cb-103">Bir yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a33cb-103">Sets the goal state for a probe configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a33cb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a33cb-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a33cb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a33cb-105">DESCRIPTION</span></span>
<span data-ttu-id="a33cb-106">**Set-AzureRmLoadBalancerProbeConfig** cmdlet 'i, bir yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a33cb-106">The **Set-AzureRmLoadBalancerProbeConfig** cmdlet sets the goal state for a probe configuration.</span></span>

## <span data-ttu-id="a33cb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a33cb-107">EXAMPLES</span></span>

### <span data-ttu-id="a33cb-108">Örnek 1: yük dengeleyicide yoklama yapılandırmasını değiştirme</span><span class="sxs-lookup"><span data-stu-id="a33cb-108">Example 1: Modify the probe configuration on a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $slb | Add-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 2 -RequestPath "healthcheck.aspx" 
PS C:\> $slb | Set-AzureRmLoadBalancerProbeConfig -Name "NewProbe" -Port 80 -IntervalInSeconds 15 -ProbeCount 2
```

<span data-ttu-id="a33cb-109">İlk komut MyLoadBalancer adındaki loadbalancer 'ı alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="a33cb-109">The first command gets the loadbalancer named MyLoadBalancer, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="a33cb-110">İkinci komut, yük dengeleyiciyi bir şekilde geçirmek için $slb ' a yeni bir yoklama yapılandırması ekleyen-AzureRmLoadBalancerProbeConfig öğesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a33cb-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerProbeConfig, which adds a new probe configuration to it.</span></span>

<span data-ttu-id="a33cb-111">Üçüncü komut, yükleme dengeleyicisine, yeni yapılandırmayı ayarlayan **-AzureRmLoadBalancerProbeConfig** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="a33cb-111">The third command passes the load balancer to **Set-AzureRmLoadBalancerProbeConfig** , which sets the new configuration.</span></span>
<span data-ttu-id="a33cb-112">Geçerli cmdlet 'in gerektirmeleri nedeniyle, önceki komutta belirtilen parametrelerin aynısını belirtmeniz gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a33cb-112">Note that it is necessary to specify several of the same parameters that were specified in the previous command because they are required by the current cmdlet.</span></span>

## <span data-ttu-id="a33cb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a33cb-113">PARAMETERS</span></span>

### <span data-ttu-id="a33cb-114">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="a33cb-114">-IntervalInSeconds</span></span>
<span data-ttu-id="a33cb-115">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a33cb-115">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33cb-116">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a33cb-116">-LoadBalancer</span></span>
<span data-ttu-id="a33cb-117">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="a33cb-117">Specifies a load balancer.</span></span>
<span data-ttu-id="a33cb-118">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin yoklama yapılandırmasının hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a33cb-118">This cmdlet sets the goal state for a probe configuration for the load balancer that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a33cb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a33cb-119">-Name</span></span>
<span data-ttu-id="a33cb-120">Bu cmdlet 'in ayarladığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a33cb-120">Specifies the name of the probe configuration that this cmdlet sets.</span></span>

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

### <span data-ttu-id="a33cb-121">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="a33cb-121">-Port</span></span>
<span data-ttu-id="a33cb-122">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a33cb-122">Specifies the port on which probes should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33cb-123">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="a33cb-123">-ProbeCount</span></span>
<span data-ttu-id="a33cb-124">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a33cb-124">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33cb-125">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="a33cb-125">-Protocol</span></span>
<span data-ttu-id="a33cb-126">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a33cb-126">Specifies the protocol to use for the probing.</span></span>
<span data-ttu-id="a33cb-127">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="a33cb-127">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33cb-128">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="a33cb-128">-RequestPath</span></span>
<span data-ttu-id="a33cb-129">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a33cb-129">Specifies the path in the load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33cb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33cb-130">-DefaultProfile</span></span>
<span data-ttu-id="a33cb-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a33cb-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a33cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33cb-132">CommonParameters</span></span>
<span data-ttu-id="a33cb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a33cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33cb-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a33cb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33cb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a33cb-135">INPUTS</span></span>

### <span data-ttu-id="a33cb-136">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a33cb-136">PSLoadBalancer</span></span>
<span data-ttu-id="a33cb-137">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="a33cb-137">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="a33cb-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a33cb-138">OUTPUTS</span></span>

### <span data-ttu-id="a33cb-139">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a33cb-139">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a33cb-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a33cb-140">NOTES</span></span>

## <span data-ttu-id="a33cb-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a33cb-141">RELATED LINKS</span></span>

[<span data-ttu-id="a33cb-142">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a33cb-142">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a33cb-143">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a33cb-143">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="a33cb-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a33cb-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a33cb-145">Yeni-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a33cb-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a33cb-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a33cb-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)


