---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerruleconfig
schema: 2.0.0
ms.openlocfilehash: bb0821265f87f959523009a9277dc884498e0e0c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939894"
---
# <span data-ttu-id="1cf07-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cf07-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="1cf07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cf07-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf07-103">Bir yük dengeleyicinin kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1cf07-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cf07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1cf07-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cf07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1cf07-105">DESCRIPTION</span></span>
<span data-ttu-id="1cf07-106">**Remove-AzureRmLoadBalancerRuleConfig** cmdlet 'i, bir Azure Yük dengeleyicinin bir kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1cf07-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="1cf07-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1cf07-107">EXAMPLES</span></span>

### <span data-ttu-id="1cf07-108">Örnek 1: yük dengeleyiciden bir kural yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1cf07-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="1cf07-109">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1cf07-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="1cf07-110">İkinci komut, $loadbalancer 'daki yük dengeleyiciden MyLBruleName adlı kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1cf07-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="1cf07-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1cf07-111">PARAMETERS</span></span>

### <span data-ttu-id="1cf07-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf07-112">-DefaultProfile</span></span>
<span data-ttu-id="1cf07-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1cf07-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cf07-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1cf07-114">-LoadBalancer</span></span>
<span data-ttu-id="1cf07-115">Bu cmdlet 'in kaldırıldığı kural yapılandırmasını içeren **LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1cf07-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1cf07-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1cf07-116">-Name</span></span>
<span data-ttu-id="1cf07-117">Bu cmdlet 'in kaldırıldığı yük dengeleyici kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1cf07-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1cf07-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf07-118">CommonParameters</span></span>
<span data-ttu-id="1cf07-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1cf07-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf07-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cf07-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf07-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1cf07-121">INPUTS</span></span>

### <span data-ttu-id="1cf07-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1cf07-122">PSLoadBalancer</span></span>
<span data-ttu-id="1cf07-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1cf07-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1cf07-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1cf07-124">OUTPUTS</span></span>

### <span data-ttu-id="1cf07-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1cf07-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1cf07-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1cf07-126">NOTES</span></span>

## <span data-ttu-id="1cf07-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1cf07-127">RELATED LINKS</span></span>

[<span data-ttu-id="1cf07-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cf07-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1cf07-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1cf07-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="1cf07-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cf07-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1cf07-131">Yeni-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cf07-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="1cf07-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1cf07-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


