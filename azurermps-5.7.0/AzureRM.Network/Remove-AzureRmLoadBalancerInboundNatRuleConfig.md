---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D818C404-60E4-42DB-AADF-063305D9541B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6dcd7c51a43387139de85a3a9f0c17c0b19cfe12
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590966"
---
# <span data-ttu-id="7713c-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7713c-101">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="7713c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7713c-102">SYNOPSIS</span></span>
<span data-ttu-id="7713c-103">Bir yük dengeleyiciden gelen NAT kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7713c-103">Removes an inbound NAT rule configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7713c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7713c-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7713c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7713c-105">DESCRIPTION</span></span>
<span data-ttu-id="7713c-106">**Remove-Azurermloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure yük dengeleyiciden gelen ağ adresi ÇEVIRISI (NAT) kuralı yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7713c-106">The **Remove-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet removes an inbound network address translation (NAT) rule configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="7713c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7713c-107">EXAMPLES</span></span>

### <span data-ttu-id="7713c-108">1: Azure yük dengeleyiciden gelen NAT kuralını silme</span><span class="sxs-lookup"><span data-stu-id="7713c-108">1: Delete an inbound NAT rule from an Azure load balancer</span></span>
```
$loadbalancer = Get-AzureRmLoadBalancer -Name mylb -ResourceGroupName myrg

 Remove-AzureRmLoadBalancerInboundNatRuleConfig -Name "myinboundnatrule" -LoadBalancer $loadbalancer
```

<span data-ttu-id="7713c-109">İlk komut, önceden "mylb" adlı bir yük dengeleyicisi yükler ve bunu değişken $load dengeleyicide depolar.</span><span class="sxs-lookup"><span data-stu-id="7713c-109">The first command loads an already existing load balancer called "mylb" and stores it in the variable $load balancer.</span></span> <span data-ttu-id="7713c-110">İkinci komut bu yük dengeleyiciyle ilişkili gelen NAT kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7713c-110">The second command removes the inbound NAT rule associated with this load balancer.</span></span>

## <span data-ttu-id="7713c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7713c-111">PARAMETERS</span></span>

### <span data-ttu-id="7713c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7713c-112">-DefaultProfile</span></span>
<span data-ttu-id="7713c-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7713c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7713c-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7713c-114">-LoadBalancer</span></span>
<span data-ttu-id="7713c-115">Bu cmdlet 'in kaldırıldığı gelen NAT kuralı yapılandırmasını içeren **LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7713c-115">Specifies the **LoadBalancer** object that contains the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7713c-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="7713c-116">-Name</span></span>
<span data-ttu-id="7713c-117">Bu cmdlet 'in kaldırıldığı gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7713c-117">Specifies the name of the inbound NAT rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7713c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7713c-118">CommonParameters</span></span>
<span data-ttu-id="7713c-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7713c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7713c-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7713c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7713c-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7713c-121">INPUTS</span></span>

### <span data-ttu-id="7713c-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7713c-122">PSLoadBalancer</span></span>
<span data-ttu-id="7713c-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="7713c-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="7713c-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7713c-124">OUTPUTS</span></span>

### <span data-ttu-id="7713c-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7713c-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="7713c-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7713c-126">NOTES</span></span>

## <span data-ttu-id="7713c-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7713c-127">RELATED LINKS</span></span>

[<span data-ttu-id="7713c-128">Add-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="7713c-128">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7713c-129">Get-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="7713c-129">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7713c-130">New-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="7713c-130">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="7713c-131">Set-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="7713c-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)

