---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b09aeb7288f69d0edc678578bbcc91306f5b0c2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595084"
---
# <span data-ttu-id="d2531-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2531-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="d2531-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2531-102">SYNOPSIS</span></span>
<span data-ttu-id="d2531-103">Bir yük dengeleyicinin kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="d2531-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2531-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2531-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2531-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2531-105">DESCRIPTION</span></span>
<span data-ttu-id="d2531-106">**Get-AzureRmLoadBalancerRuleConfig** cmdlet 'i, bir yük dengeleyicinin bir veya daha fazla kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="d2531-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="d2531-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2531-107">EXAMPLES</span></span>

### <span data-ttu-id="d2531-108">Örnek 1: yük dengeleyicinin kural yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="d2531-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="d2531-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="d2531-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="d2531-110">İkinci komut, $slb 'teki yük dengeleyiciden MyLBrulename adlı ilişkili kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="d2531-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="d2531-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2531-111">PARAMETERS</span></span>

### <span data-ttu-id="d2531-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2531-112">-DefaultProfile</span></span>
<span data-ttu-id="d2531-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2531-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2531-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2531-114">-LoadBalancer</span></span>
<span data-ttu-id="d2531-115">Alınacak kural yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2531-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="d2531-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2531-116">-Name</span></span>
<span data-ttu-id="d2531-117">Alınacak kural yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2531-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="d2531-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2531-118">CommonParameters</span></span>
<span data-ttu-id="d2531-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2531-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2531-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2531-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2531-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2531-121">INPUTS</span></span>

### <span data-ttu-id="d2531-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2531-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="d2531-123">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d2531-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="d2531-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2531-124">OUTPUTS</span></span>

### <span data-ttu-id="d2531-125">Microsoft. Azure. Commands. Network. modeller. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="d2531-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="d2531-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2531-126">NOTES</span></span>

## <span data-ttu-id="d2531-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2531-127">RELATED LINKS</span></span>

[<span data-ttu-id="d2531-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2531-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="d2531-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2531-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d2531-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2531-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="d2531-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d2531-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


