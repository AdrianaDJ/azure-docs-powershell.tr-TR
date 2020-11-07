---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerRuleConfig.md
ms.openlocfilehash: 9c50452acd832c7ac7ca0c4bc2827b8f320115b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935287"
---
# <span data-ttu-id="b5e22-101">Remove-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5e22-101">Remove-AzLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="b5e22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5e22-102">SYNOPSIS</span></span>
<span data-ttu-id="b5e22-103">Bir yük dengeleyicinin kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5e22-103">Removes a rule configuration for a load balancer.</span></span>

## <span data-ttu-id="b5e22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5e22-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5e22-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5e22-105">DESCRIPTION</span></span>
<span data-ttu-id="b5e22-106">**Remove-AzLoadBalancerRuleConfig** cmdlet 'i, bir Azure Yük dengeleyicinin bir kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5e22-106">The **Remove-AzLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="b5e22-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5e22-107">EXAMPLES</span></span>

### <span data-ttu-id="b5e22-108">Örnek 1: yük dengeleyiciden bir kural yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b5e22-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="b5e22-109">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b5e22-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="b5e22-110">İkinci komut, $loadbalancer 'daki yük dengeleyiciden MyLBruleName adlı kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5e22-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="b5e22-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5e22-111">PARAMETERS</span></span>

### <span data-ttu-id="b5e22-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5e22-112">-DefaultProfile</span></span>
<span data-ttu-id="b5e22-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5e22-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5e22-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b5e22-114">-LoadBalancer</span></span>
<span data-ttu-id="b5e22-115">Bu cmdlet 'in kaldırıldığı kural yapılandırmasını içeren **LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e22-115">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b5e22-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5e22-116">-Name</span></span>
<span data-ttu-id="b5e22-117">Bu cmdlet 'in kaldırıldığı yük dengeleyici kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5e22-117">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b5e22-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5e22-118">CommonParameters</span></span>
<span data-ttu-id="b5e22-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5e22-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5e22-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5e22-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5e22-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5e22-121">INPUTS</span></span>

### <span data-ttu-id="b5e22-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b5e22-122">PSLoadBalancer</span></span>
<span data-ttu-id="b5e22-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b5e22-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="b5e22-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5e22-124">OUTPUTS</span></span>

### <span data-ttu-id="b5e22-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b5e22-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b5e22-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5e22-126">NOTES</span></span>

## <span data-ttu-id="b5e22-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5e22-127">RELATED LINKS</span></span>

[<span data-ttu-id="b5e22-128">Add-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5e22-128">Add-AzLoadBalancerRuleConfig</span></span>](./Add-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b5e22-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b5e22-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b5e22-130">Get-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5e22-130">Get-AzLoadBalancerRuleConfig</span></span>](./Get-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b5e22-131">New-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5e22-131">New-AzLoadBalancerRuleConfig</span></span>](./New-AzLoadBalancerRuleConfig.md)

[<span data-ttu-id="b5e22-132">Set-AzLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b5e22-132">Set-AzLoadBalancerRuleConfig</span></span>](./Set-AzLoadBalancerRuleConfig.md)


