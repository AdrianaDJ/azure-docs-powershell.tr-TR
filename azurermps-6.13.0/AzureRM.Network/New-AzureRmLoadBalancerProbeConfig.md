---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a4889190e58edd896d1a93222a35688dd5884c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590151"
---
# <span data-ttu-id="a9853-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a9853-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="a9853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9853-102">SYNOPSIS</span></span>
<span data-ttu-id="a9853-103">Bir yük dengeleyici için yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9853-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9853-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9853-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9853-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9853-105">DESCRIPTION</span></span>
<span data-ttu-id="a9853-106">**Yeni-AzureRmLoadBalancerProbeConfig** cmdlet 'i, bir Azure yük dengeleyicisi için bir yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9853-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="a9853-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9853-107">EXAMPLES</span></span>

### <span data-ttu-id="a9853-108">Örnek 1: yoklama yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="a9853-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="a9853-109">Bu komut, HTTP protokolünü kullanarak Myaraştırması adlı bir yoklama yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a9853-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="a9853-110">Yeni yoklama, bağlantı noktası 80 ' da yük dengeli bir hizmete bağlanır.</span><span class="sxs-lookup"><span data-stu-id="a9853-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="a9853-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9853-111">PARAMETERS</span></span>

### <span data-ttu-id="a9853-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9853-112">-DefaultProfile</span></span>
<span data-ttu-id="a9853-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a9853-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9853-114">-Intervalınseconds</span><span class="sxs-lookup"><span data-stu-id="a9853-114">-IntervalInSeconds</span></span>
<span data-ttu-id="a9853-115">Yük dengeli bir hizmetin her örneğindeki yoklamalarını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9853-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="a9853-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a9853-116">-Name</span></span>
<span data-ttu-id="a9853-117">Oluşturulacak yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9853-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="a9853-118">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="a9853-118">-Port</span></span>
<span data-ttu-id="a9853-119">Yeni araştırın yük dengeli bir hizmete bağlanması gereken bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9853-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="a9853-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="a9853-120">-ProbeCount</span></span>
<span data-ttu-id="a9853-121">Bir örnek sağlıksız kabul edilecek örnek başına hata sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9853-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="a9853-122">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="a9853-122">-Protocol</span></span>
<span data-ttu-id="a9853-123">Araştırma yapılandırması için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9853-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="a9853-124">Bu parametre için kabul edilebilir değerler: TCP veya http.</span><span class="sxs-lookup"><span data-stu-id="a9853-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

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

### <span data-ttu-id="a9853-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="a9853-125">-RequestPath</span></span>
<span data-ttu-id="a9853-126">Sistem durumunu belirlemek için yük dengeli bir hizmetin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a9853-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="a9853-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="a9853-127">-Confirm</span></span>
<span data-ttu-id="a9853-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a9853-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9853-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9853-129">-WhatIf</span></span>
<span data-ttu-id="a9853-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a9853-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9853-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a9853-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9853-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9853-132">CommonParameters</span></span>
<span data-ttu-id="a9853-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9853-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9853-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9853-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9853-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9853-135">INPUTS</span></span>

### <span data-ttu-id="a9853-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a9853-136">None</span></span>

## <span data-ttu-id="a9853-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9853-137">OUTPUTS</span></span>

### <span data-ttu-id="a9853-138">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="a9853-138">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="a9853-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9853-139">NOTES</span></span>

## <span data-ttu-id="a9853-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9853-140">RELATED LINKS</span></span>

[<span data-ttu-id="a9853-141">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a9853-141">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a9853-142">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a9853-142">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a9853-143">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a9853-143">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="a9853-144">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="a9853-144">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


