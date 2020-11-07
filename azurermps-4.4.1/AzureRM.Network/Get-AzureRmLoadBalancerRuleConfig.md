---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B2CF11FC-520C-4C14-9A1B-13F06B250B5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: b5d8bbba6416e20ffd29180f8d0a2f211dc88270
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763102"
---
# <span data-ttu-id="103c8-101">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="103c8-101">Get-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="103c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="103c8-102">SYNOPSIS</span></span>
<span data-ttu-id="103c8-103">Bir yük dengeleyicinin kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="103c8-103">Gets the rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="103c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="103c8-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="103c8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="103c8-105">DESCRIPTION</span></span>
<span data-ttu-id="103c8-106">**Get-AzureRmLoadBalancerRuleConfig** cmdlet 'i, bir yük dengeleyicinin bir veya daha fazla kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="103c8-106">The **Get-AzureRmLoadBalancerRuleConfig** cmdlet gets one or more rule configurations for a load balancer.</span></span>

## <span data-ttu-id="103c8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="103c8-107">EXAMPLES</span></span>

### <span data-ttu-id="103c8-108">Örnek 1: yük dengeleyicinin kural yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="103c8-108">Example 1: Get the rule configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerRuleConfig -Name "MyLBrulename" -LoadBalancer $slb
```

<span data-ttu-id="103c8-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="103c8-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="103c8-110">İkinci komut, $slb 'teki yük dengeleyiciden MyLBrulename adlı ilişkili kural yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="103c8-110">The second command gets the associated rule configuration named MyLBrulename from the load balancer in $slb.</span></span>

## <span data-ttu-id="103c8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="103c8-111">PARAMETERS</span></span>

### <span data-ttu-id="103c8-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="103c8-112">-LoadBalancer</span></span>
<span data-ttu-id="103c8-113">Alınacak kural yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="103c8-113">Specifies the load balancer that is associated with the rule configuration to get.</span></span>

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

### <span data-ttu-id="103c8-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="103c8-114">-Name</span></span>
<span data-ttu-id="103c8-115">Alınacak kural yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="103c8-115">Specifies the name of the rule configuration to get.</span></span>

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

### <span data-ttu-id="103c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103c8-116">-DefaultProfile</span></span>
<span data-ttu-id="103c8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="103c8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="103c8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103c8-118">CommonParameters</span></span>
<span data-ttu-id="103c8-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="103c8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103c8-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="103c8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103c8-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="103c8-121">INPUTS</span></span>

### <span data-ttu-id="103c8-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="103c8-122">PSLoadBalancer</span></span>
<span data-ttu-id="103c8-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="103c8-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="103c8-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="103c8-124">OUTPUTS</span></span>

### <span data-ttu-id="103c8-125">Microsoft. Azure. Commands. Network. modeller. PSLoadBalancingRule</span><span class="sxs-lookup"><span data-stu-id="103c8-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancingRule</span></span>

## <span data-ttu-id="103c8-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="103c8-126">NOTES</span></span>

## <span data-ttu-id="103c8-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="103c8-127">RELATED LINKS</span></span>

[<span data-ttu-id="103c8-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="103c8-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="103c8-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="103c8-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="103c8-130">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="103c8-130">Remove-AzureRmLoadBalancerRuleConfig</span></span>](./Remove-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="103c8-131">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="103c8-131">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)

