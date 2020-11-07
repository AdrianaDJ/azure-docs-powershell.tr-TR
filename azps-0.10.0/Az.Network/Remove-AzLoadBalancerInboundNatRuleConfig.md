---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: b135f9a54c084eb7bc5dc4562e16c67e316f8736
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935294"
---
# <span data-ttu-id="783ea-101">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="783ea-101">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="783ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="783ea-102">SYNOPSIS</span></span>
<span data-ttu-id="783ea-103">Bir yük dengeleyiciden gelen NAT kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="783ea-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

## <span data-ttu-id="783ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="783ea-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="783ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="783ea-105">DESCRIPTION</span></span>
<span data-ttu-id="783ea-106">**Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet 'i, bir Azure yük dengeleyiciden gelen ağ adresi ÇEVIRISI (NAT) kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="783ea-106">The **Remove-AzLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="783ea-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="783ea-107">EXAMPLES</span></span>

### <span data-ttu-id="783ea-108">1: Azure yük dengeleyiciden gelen NAT kuralını silme</span><span class="sxs-lookup"><span data-stu-id="783ea-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="783ea-109">İlk komut, önceden "mylb" adlı bir yük dengeleyicisi yükler ve bunu değişken $load dengeleyicide depolar.</span><span class="sxs-lookup"><span data-stu-id="783ea-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="783ea-110">İkinci komut bu yük dengeleyiciyle ilişkili gelen NAT kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="783ea-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="783ea-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="783ea-111">PARAMETERS</span></span>

### <span data-ttu-id="783ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783ea-112">-DefaultProfile</span></span>
<span data-ttu-id="783ea-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="783ea-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="783ea-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="783ea-114">-LoadBalancer</span></span>
<span data-ttu-id="783ea-115">Bu cmdlet 'in kaldırıldığı gelen NAT kuralı yapılandırmasını içeren **LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="783ea-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="783ea-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="783ea-116">-Name</span></span>
<span data-ttu-id="783ea-117">Bu cmdlet 'in kaldırıldığı gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="783ea-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="783ea-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783ea-118">CommonParameters</span></span>
<span data-ttu-id="783ea-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="783ea-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783ea-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="783ea-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783ea-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="783ea-121">INPUTS</span></span>

### <span data-ttu-id="783ea-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="783ea-122">PSLoadBalancer</span></span>
<span data-ttu-id="783ea-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="783ea-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="783ea-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="783ea-124">OUTPUTS</span></span>

### <span data-ttu-id="783ea-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="783ea-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="783ea-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="783ea-126">NOTES</span></span>

## <span data-ttu-id="783ea-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="783ea-127">RELATED LINKS</span></span>

[<span data-ttu-id="783ea-128">Add-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="783ea-128">Add-AzLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="783ea-129">Get-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="783ea-129">Get-AzLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="783ea-130">New-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="783ea-130">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="783ea-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="783ea-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


