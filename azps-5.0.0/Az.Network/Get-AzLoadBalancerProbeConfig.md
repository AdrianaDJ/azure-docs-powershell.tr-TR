---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 5b6031657438bfc28ce76519c8489e041a060965
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276223"
---
# <span data-ttu-id="8322b-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8322b-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="8322b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8322b-102">SYNOPSIS</span></span>
<span data-ttu-id="8322b-103">Bir yük dengeleyicinin yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="8322b-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="8322b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8322b-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8322b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8322b-105">DESCRIPTION</span></span>
<span data-ttu-id="8322b-106">**Get-AzLoadBalancerProbeConfig** cmdlet 'i bir yük dengeleyicinin bir veya daha fazla yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="8322b-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="8322b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8322b-107">EXAMPLES</span></span>

### <span data-ttu-id="8322b-108">Örnek 1: yük dengeleyicinin yoklama yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="8322b-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="8322b-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="8322b-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="8322b-110">İkinci komut, $slb 'daki yük dengeleyiciden Myyoklama adlı ilişkili yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="8322b-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="8322b-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8322b-111">PARAMETERS</span></span>

### <span data-ttu-id="8322b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8322b-112">-DefaultProfile</span></span>
<span data-ttu-id="8322b-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8322b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8322b-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8322b-114">-LoadBalancer</span></span>
<span data-ttu-id="8322b-115">Alınacak yoklama yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="8322b-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="8322b-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="8322b-116">-Name</span></span>
<span data-ttu-id="8322b-117">Alınacak yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8322b-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="8322b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8322b-118">CommonParameters</span></span>
<span data-ttu-id="8322b-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8322b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8322b-120">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8322b-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8322b-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8322b-121">INPUTS</span></span>

### <span data-ttu-id="8322b-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8322b-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8322b-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8322b-123">OUTPUTS</span></span>

### <span data-ttu-id="8322b-124">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="8322b-124">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="8322b-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8322b-125">NOTES</span></span>

## <span data-ttu-id="8322b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8322b-126">RELATED LINKS</span></span>

[<span data-ttu-id="8322b-127">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8322b-127">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8322b-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8322b-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="8322b-129">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8322b-129">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8322b-130">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8322b-130">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="8322b-131">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="8322b-131">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


