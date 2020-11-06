---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6F9BAB0B-7DC7-4672-B2B5-8B139D652DDD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 62ed11a2819a2b0c31756c90ce4ab623a1feae91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593217"
---
# <span data-ttu-id="512a2-101">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="512a2-101">Add-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="512a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="512a2-102">SYNOPSIS</span></span>
<span data-ttu-id="512a2-103">Bir yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="512a2-103">Adds a probe configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="512a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="512a2-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> -Name <String> [-Protocol <String>]
 -Port <Int32> -IntervalInSeconds <Int32> -ProbeCount <Int32> [-RequestPath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="512a2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="512a2-105">DESCRIPTION</span></span>
<span data-ttu-id="512a2-106">**Add-AzureRmLoadBalancerProbeConfig** cmdlet 'ı bir Azure yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="512a2-106">The **Add-AzureRmLoadBalancerProbeConfig** cmdlet adds a probe configuration to an Azure load balancer.</span></span>

## <span data-ttu-id="512a2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="512a2-107">EXAMPLES</span></span>

### <span data-ttu-id="512a2-108">Örnek 1 yük dengeleyicisine bir yoklama yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="512a2-108">Example 1 Add a probe configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "myLb" -ResourceGroupName "myRg" | Add-AzureRmLoadBalancerProbeConfig -Name "probeName" -RequestPath healthcheck2.aspx -Protocol http -Port 81 -IntervalInSeconds 16 -ProbeCount 3 | Set-AzureRmLoadBalancer
```

<span data-ttu-id="512a2-109">Bu komut myLb adındaki yük dengeleyiciden alır, belirtilen yoklama yapılandırmasını ekler ve ardından yük dengeleyicmayı güncelleştirmek için **set-AzureRmLoadBalancer** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="512a2-109">This command gets the load balancer named myLb, adds the specified probe configuration to it, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update the load balancer.</span></span>

## <span data-ttu-id="512a2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="512a2-110">PARAMETERS</span></span>

### <span data-ttu-id="512a2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512a2-111">-DefaultProfile</span></span>
<span data-ttu-id="512a2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="512a2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="512a2-113">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="512a2-113">-IntervalInSeconds</span></span>
<span data-ttu-id="512a2-114">Yük dengeli hizmetin her örneğine yönelik yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="512a2-114">Specifies the interval, in seconds, between probes to each instance of the load-balanced service.</span></span>

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

### <span data-ttu-id="512a2-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="512a2-115">-LoadBalancer</span></span>
<span data-ttu-id="512a2-116">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="512a2-116">Specifies a **LoadBalancer** object.</span></span>
<span data-ttu-id="512a2-117">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicisine bir yoklama yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="512a2-117">This cmdlet adds a probe configuration to the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="512a2-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="512a2-118">-Name</span></span>
<span data-ttu-id="512a2-119">Eklenecek yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="512a2-119">Specifies the name of the probe configuration to add.</span></span>

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

### <span data-ttu-id="512a2-120">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="512a2-120">-Port</span></span>
<span data-ttu-id="512a2-121">Sondada yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="512a2-121">Specifies the port on which probes should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="512a2-122">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="512a2-122">-ProbeCount</span></span>
<span data-ttu-id="512a2-123">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="512a2-123">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="512a2-124">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="512a2-124">-Protocol</span></span>
<span data-ttu-id="512a2-125">Yoklama için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="512a2-125">Specifies the protocol to use for the probe.</span></span>
<span data-ttu-id="512a2-126">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="512a2-126">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="512a2-127">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="512a2-127">-RequestPath</span></span>
<span data-ttu-id="512a2-128">Sistem durumunu belirlemek için yük dengeli hizmet hizmeti 'nin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="512a2-128">Specifies the path in the load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="512a2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="512a2-129">-Confirm</span></span>
<span data-ttu-id="512a2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="512a2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="512a2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512a2-131">-WhatIf</span></span>
<span data-ttu-id="512a2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="512a2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="512a2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="512a2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="512a2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512a2-134">CommonParameters</span></span>
<span data-ttu-id="512a2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="512a2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512a2-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512a2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512a2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="512a2-137">INPUTS</span></span>

### <span data-ttu-id="512a2-138">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="512a2-138">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="512a2-139">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="512a2-139">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="512a2-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="512a2-140">OUTPUTS</span></span>

### <span data-ttu-id="512a2-141">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="512a2-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="512a2-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="512a2-142">NOTES</span></span>

## <span data-ttu-id="512a2-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="512a2-143">RELATED LINKS</span></span>

[<span data-ttu-id="512a2-144">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="512a2-144">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="512a2-145">Yeni-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="512a2-145">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="512a2-146">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="512a2-146">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="512a2-147">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="512a2-147">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)

[<span data-ttu-id="512a2-148">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="512a2-148">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


