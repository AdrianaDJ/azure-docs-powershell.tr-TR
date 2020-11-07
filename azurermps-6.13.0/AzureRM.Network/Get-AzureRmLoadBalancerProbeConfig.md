---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 87722e7f639e3a9e2ca135196bceff75c61abddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765099"
---
# <span data-ttu-id="c3e71-101">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c3e71-101">Get-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="c3e71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e71-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e71-103">Bir yük dengeleyicinin yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="c3e71-103">Gets a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3e71-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerProbeConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3e71-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e71-106">**Get-AzureRmLoadBalancerProbeConfig** cmdlet 'i, bir yük dengeleyicinin bir veya daha fazla yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="c3e71-106">The **Get-AzureRmLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="c3e71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3e71-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e71-108">Örnek 1: yük dengeleyicinin yoklama yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="c3e71-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="c3e71-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="c3e71-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="c3e71-110">İkinci komut, $slb 'daki yük dengeleyiciden Myyoklama adlı ilişkili yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="c3e71-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="c3e71-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3e71-111">PARAMETERS</span></span>

### <span data-ttu-id="c3e71-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e71-112">-DefaultProfile</span></span>
<span data-ttu-id="c3e71-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c3e71-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3e71-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3e71-114">-LoadBalancer</span></span>
<span data-ttu-id="c3e71-115">Alınacak yoklama yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3e71-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="c3e71-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3e71-116">-Name</span></span>
<span data-ttu-id="c3e71-117">Alınacak yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3e71-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="c3e71-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e71-118">CommonParameters</span></span>
<span data-ttu-id="c3e71-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3e71-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e71-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e71-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e71-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3e71-121">INPUTS</span></span>

### <span data-ttu-id="c3e71-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3e71-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="c3e71-123">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3e71-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="c3e71-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3e71-124">OUTPUTS</span></span>

### <span data-ttu-id="c3e71-125">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="c3e71-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="c3e71-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3e71-126">NOTES</span></span>

## <span data-ttu-id="c3e71-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3e71-127">RELATED LINKS</span></span>

[<span data-ttu-id="c3e71-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c3e71-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c3e71-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3e71-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c3e71-130">Yeni-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c3e71-130">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c3e71-131">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c3e71-131">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="c3e71-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="c3e71-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


