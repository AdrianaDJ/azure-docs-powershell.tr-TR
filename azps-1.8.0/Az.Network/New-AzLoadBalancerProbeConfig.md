---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6bcf0957d389f45bb0e010446381303c6124146b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760319"
---
# <span data-ttu-id="de4fa-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4fa-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="de4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="de4fa-103">Bir yük dengeleyici için yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de4fa-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="de4fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de4fa-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de4fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="de4fa-105">DESCRIPTION</span></span>
<span data-ttu-id="de4fa-106">**New-AzLoadBalancerProbeConfig** cmdlet 'i, bir Azure yük dengeleyicisi için bir yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de4fa-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="de4fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de4fa-107">EXAMPLES</span></span>

### <span data-ttu-id="de4fa-108">Örnek 1: yoklama yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="de4fa-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="de4fa-109">Bu komut, HTTP protokolünü kullanarak Myaraştırması adlı bir yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="de4fa-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="de4fa-110">Yeni yoklama, bağlantı noktası 80 ' da yük dengeli bir hizmete bağlanır.</span><span class="sxs-lookup"><span data-stu-id="de4fa-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="de4fa-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de4fa-111">PARAMETERS</span></span>

### <span data-ttu-id="de4fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de4fa-112">-DefaultProfile</span></span>
<span data-ttu-id="de4fa-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de4fa-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de4fa-114">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="de4fa-114">-IntervalInSeconds</span></span>
<span data-ttu-id="de4fa-115">Yük dengeli bir hizmetin her örneğindeki yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4fa-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="de4fa-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="de4fa-116">-Name</span></span>
<span data-ttu-id="de4fa-117">Oluşturulacak yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4fa-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="de4fa-118">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="de4fa-118">-Port</span></span>
<span data-ttu-id="de4fa-119">Yeni araştırın yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4fa-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="de4fa-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="de4fa-120">-ProbeCount</span></span>
<span data-ttu-id="de4fa-121">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4fa-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="de4fa-122">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="de4fa-122">-Protocol</span></span>
<span data-ttu-id="de4fa-123">Araştırma yapılandırması için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4fa-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="de4fa-124">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="de4fa-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="de4fa-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="de4fa-125">-RequestPath</span></span>
<span data-ttu-id="de4fa-126">Sistem durumunu belirlemek için yük dengeli bir hizmetin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="de4fa-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="de4fa-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="de4fa-127">-Confirm</span></span>
<span data-ttu-id="de4fa-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de4fa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de4fa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de4fa-129">-WhatIf</span></span>
<span data-ttu-id="de4fa-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de4fa-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de4fa-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de4fa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de4fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de4fa-132">CommonParameters</span></span>
<span data-ttu-id="de4fa-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de4fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de4fa-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de4fa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de4fa-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de4fa-135">INPUTS</span></span>

### <span data-ttu-id="de4fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="de4fa-136">System.String</span></span>

### <span data-ttu-id="de4fa-137">System. Int32</span><span class="sxs-lookup"><span data-stu-id="de4fa-137">System.Int32</span></span>

## <span data-ttu-id="de4fa-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de4fa-138">OUTPUTS</span></span>

### <span data-ttu-id="de4fa-139">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="de4fa-139">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="de4fa-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de4fa-140">NOTES</span></span>

## <span data-ttu-id="de4fa-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de4fa-141">RELATED LINKS</span></span>

[<span data-ttu-id="de4fa-142">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4fa-142">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="de4fa-143">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4fa-143">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="de4fa-144">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4fa-144">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="de4fa-145">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="de4fa-145">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


