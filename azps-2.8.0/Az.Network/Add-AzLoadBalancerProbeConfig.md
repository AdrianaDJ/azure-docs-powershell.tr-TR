---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 071a6db22f6788f76a6c4323c26247c070f164b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932090"
---
# <span data-ttu-id="2bd8c-101">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bd8c-101">Add-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="2bd8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bd8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd8c-103">Bir yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-103">Adds a probe configuration to a load balancer.</span></span>

## <span data-ttu-id="2bd8c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2bd8c-104">SYNTAX</span></span>

```
Add-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd8c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2bd8c-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd8c-106">**Add-AzLoadBalancerProbeConfig** cmdlet 'ı bir Azure yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-106">The **Add-AzLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="2bd8c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2bd8c-107">EXAMPLES</span></span>

### <span data-ttu-id="2bd8c-108">Örnek 1 yük dengeleyicisine bir yoklama yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="2bd8c-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzLoadBalancer
```

<span data-ttu-id="2bd8c-109">Bu komut myLb adındaki yük dengeleyiciden alır, belirtilen yoklama yapılandırmasını ekler ve ardından yük dengeleyiciyi güncelleştirmek için **set-AzLoadBalancer** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="2bd8c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2bd8c-110">PARAMETERS</span></span>

### <span data-ttu-id="2bd8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd8c-111">-DefaultProfile</span></span>
<span data-ttu-id="2bd8c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bd8c-113">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="2bd8c-113">-IntervalInSeconds</span></span>
<span data-ttu-id="2bd8c-114">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="2bd8c-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2bd8c-115">-LoadBalancer</span></span>
<span data-ttu-id="2bd8c-116">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="2bd8c-117">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="2bd8c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2bd8c-118">-Name</span></span>
<span data-ttu-id="2bd8c-119">Eklenecek yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="2bd8c-120">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="2bd8c-120">-Port</span></span>
<span data-ttu-id="2bd8c-121">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="2bd8c-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="2bd8c-122">-ProbeCount</span></span>
<span data-ttu-id="2bd8c-123">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="2bd8c-124">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="2bd8c-124">-Protocol</span></span>
<span data-ttu-id="2bd8c-125">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="2bd8c-126">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="2bd8c-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="2bd8c-127">-RequestPath</span></span>
<span data-ttu-id="2bd8c-128">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="2bd8c-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2bd8c-129">-Confirm</span></span>
<span data-ttu-id="2bd8c-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd8c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd8c-131">-WhatIf</span></span>
<span data-ttu-id="2bd8c-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bd8c-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd8c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd8c-134">CommonParameters</span></span>
<span data-ttu-id="2bd8c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2bd8c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd8c-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bd8c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd8c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2bd8c-137">INPUTS</span></span>

### <span data-ttu-id="2bd8c-138">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2bd8c-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="2bd8c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2bd8c-139">System.String</span></span>

### <span data-ttu-id="2bd8c-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2bd8c-140">System.Int32</span></span>

## <span data-ttu-id="2bd8c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2bd8c-141">OUTPUTS</span></span>

### <span data-ttu-id="2bd8c-142">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2bd8c-142">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="2bd8c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2bd8c-143">NOTES</span></span>

## <span data-ttu-id="2bd8c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2bd8c-144">RELATED LINKS</span></span>

[<span data-ttu-id="2bd8c-145">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bd8c-145">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2bd8c-146">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bd8c-146">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2bd8c-147">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bd8c-147">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="2bd8c-148">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2bd8c-148">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)

[<span data-ttu-id="2bd8c-149">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="2bd8c-149">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


