---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 71c093573f4384884702c72e586c36bbdb9b4066
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592192"
---
# <span data-ttu-id="2a732-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2a732-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="2a732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a732-102">SYNOPSIS</span></span>
<span data-ttu-id="2a732-103">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="2a732-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a732-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a732-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a732-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a732-105">DESCRIPTION</span></span>
<span data-ttu-id="2a732-106">**Get-Azurermloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure Yük dengeleyicide bir veya birden çok gelen ağ adresi ÇEVIRI (NAT) kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="2a732-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="2a732-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a732-107">EXAMPLES</span></span>

### <span data-ttu-id="2a732-108">Örnek 1: gelen NAT kural yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="2a732-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="2a732-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="2a732-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="2a732-110">İkinci komut, $slb MyInboundNatRule1 adındaki ilişkili NAT kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="2a732-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="2a732-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a732-111">PARAMETERS</span></span>

### <span data-ttu-id="2a732-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a732-112">-LoadBalancer</span></span>
<span data-ttu-id="2a732-113">Alınacak gelen NAT kuralı yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a732-113">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="2a732-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="2a732-114">-Name</span></span>
<span data-ttu-id="2a732-115">Alınacak gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2a732-115">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="2a732-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a732-116">-DefaultProfile</span></span>
<span data-ttu-id="2a732-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a732-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a732-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a732-118">CommonParameters</span></span>
<span data-ttu-id="2a732-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a732-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a732-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a732-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a732-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a732-121">INPUTS</span></span>

### <span data-ttu-id="2a732-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a732-122">PSLoadBalancer</span></span>
<span data-ttu-id="2a732-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="2a732-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="2a732-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a732-124">OUTPUTS</span></span>

### <span data-ttu-id="2a732-125">Microsoft. Azure. Commands. Network. model. Psınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="2a732-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="2a732-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a732-126">NOTES</span></span>

## <span data-ttu-id="2a732-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a732-127">RELATED LINKS</span></span>

[<span data-ttu-id="2a732-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2a732-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2a732-129">New-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="2a732-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2a732-130">Remove-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="2a732-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="2a732-131">Set-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="2a732-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


