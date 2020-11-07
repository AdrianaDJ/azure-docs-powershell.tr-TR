---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 81ff9c40045f78f961a90737d2142f5cd5189583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763034"
---
# <span data-ttu-id="4d0f3-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4d0f3-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="4d0f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d0f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4d0f3-103">Bir yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d0f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d0f3-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -Name <String> -LoadBalancer <PSLoadBalancer> [-RequestPath <String>]
 [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d0f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d0f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4d0f3-106">**Add-AzureRmLoadBalancerProbeConfig** cmdlet 'ı bir Azure yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="4d0f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d0f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4d0f3-108">Örnek 1 yük dengeleyicisine bir yoklama yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="4d0f3-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="4d0f3-109">Bu komut myLb adındaki yük dengeleyiciden alır, belirtilen yoklama yapılandırmasını ekler ve ardından yük dengeleyicmayı güncelleştirmek için **set-AzureRmLoadBalancer** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="4d0f3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d0f3-110">PARAMETERS</span></span>

### <span data-ttu-id="4d0f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d0f3-111">-DefaultProfile</span></span>
<span data-ttu-id="4d0f3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d0f3-113">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="4d0f3-113">-IntervalInSeconds</span></span>
<span data-ttu-id="4d0f3-114">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="4d0f3-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d0f3-115">-LoadBalancer</span></span>
<span data-ttu-id="4d0f3-116">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="4d0f3-117">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="4d0f3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d0f3-118">-Name</span></span>
<span data-ttu-id="4d0f3-119">Eklenecek yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="4d0f3-120">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="4d0f3-120">-Port</span></span>
<span data-ttu-id="4d0f3-121">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="4d0f3-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="4d0f3-122">-ProbeCount</span></span>
<span data-ttu-id="4d0f3-123">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="4d0f3-124">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="4d0f3-124">-Protocol</span></span>
<span data-ttu-id="4d0f3-125">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="4d0f3-126">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="4d0f3-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="4d0f3-127">-RequestPath</span></span>
<span data-ttu-id="4d0f3-128">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="4d0f3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d0f3-129">CommonParameters</span></span>
<span data-ttu-id="4d0f3-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d0f3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d0f3-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d0f3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d0f3-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d0f3-132">INPUTS</span></span>

### <span data-ttu-id="4d0f3-133">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d0f3-133">PSLoadBalancer</span></span>
<span data-ttu-id="4d0f3-134">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4d0f3-134">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4d0f3-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d0f3-135">OUTPUTS</span></span>

### <span data-ttu-id="4d0f3-136">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d0f3-136">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4d0f3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d0f3-137">NOTES</span></span>

## <span data-ttu-id="4d0f3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d0f3-138">RELATED LINKS</span></span>

[<span data-ttu-id="4d0f3-139">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4d0f3-139">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="4d0f3-140">Yeni-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4d0f3-140">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="4d0f3-141">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4d0f3-141">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="4d0f3-142">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4d0f3-142">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="4d0f3-143">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4d0f3-143">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


