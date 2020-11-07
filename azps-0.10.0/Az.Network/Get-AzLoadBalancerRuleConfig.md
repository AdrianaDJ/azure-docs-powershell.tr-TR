---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: a5d21e5a34727d0bc13730503d55be6ef604a245
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935527"
---
# <span data-ttu-id="830b9-101">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="830b9-101">Get-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="830b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="830b9-102">SYNOPSIS</span></span>
<span data-ttu-id="830b9-103">Bir yük dengeleyicinin kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="830b9-103">Gets the rule configuration for a load balancer.</span></span>

## <span data-ttu-id="830b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="830b9-104">SYNTAX</span></span>

```
Get-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="830b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="830b9-105">DESCRIPTION</span></span>
<span data-ttu-id="830b9-106">**Get-AzLoadBalancerRuleConfig** cmdlet 'i, bir yük dengeleyicinin bir veya daha fazla kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="830b9-106">The **Get-AzLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="830b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="830b9-107">EXAMPLES</span></span>

### <span data-ttu-id="830b9-108">Örnek 1: yük dengeleyicinin kural yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="830b9-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="830b9-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="830b9-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="830b9-110">İkinci komut, $slb 'teki yük dengeleyiciden MyLBrulename adlı ilişkili kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="830b9-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="830b9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="830b9-111">PARAMETERS</span></span>

### <span data-ttu-id="830b9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830b9-112">-DefaultProfile</span></span>
<span data-ttu-id="830b9-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="830b9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="830b9-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="830b9-114">-LoadBalancer</span></span>
<span data-ttu-id="830b9-115">Alınacak kural yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="830b9-115">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="830b9-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="830b9-116">-Name</span></span>
<span data-ttu-id="830b9-117">Alınacak kural yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="830b9-117">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="830b9-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830b9-118">CommonParameters</span></span>
<span data-ttu-id="830b9-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="830b9-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830b9-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="830b9-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830b9-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="830b9-121">INPUTS</span></span>

### <span data-ttu-id="830b9-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="830b9-122">PSLoadBalancer</span></span>
<span data-ttu-id="830b9-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="830b9-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="830b9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="830b9-124">OUTPUTS</span></span>

### <span data-ttu-id="830b9-125">Microsoft. Azure. Commands. Network. modeller. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="830b9-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="830b9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="830b9-126">NOTES</span></span>

## <span data-ttu-id="830b9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="830b9-127">RELATED LINKS</span></span>

[<span data-ttu-id="830b9-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="830b9-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="830b9-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="830b9-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="830b9-130">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="830b9-130">Remove-AzLoadBalancerRuleConfig</span></span>](./Remove-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="830b9-131">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="830b9-131">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


