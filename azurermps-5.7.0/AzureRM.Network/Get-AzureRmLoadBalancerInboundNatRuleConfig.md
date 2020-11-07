---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6464b1a7794278bf8bf350add937ac49f23431f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764438"
---
# <span data-ttu-id="4b350-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b350-101">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="4b350-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b350-102">SYNOPSIS</span></span>
<span data-ttu-id="4b350-103">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="4b350-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b350-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b350-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b350-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b350-105">DESCRIPTION</span></span>
<span data-ttu-id="4b350-106">**Get-Azurermloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure Yük dengeleyicide bir veya birden çok gelen ağ adresi ÇEVIRI (NAT) kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="4b350-106">The **Get-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="4b350-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b350-107">EXAMPLES</span></span>

### <span data-ttu-id="4b350-108">Örnek 1: gelen NAT kural yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="4b350-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="4b350-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="4b350-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="4b350-110">İkinci komut, $slb MyInboundNatRule1 adındaki ilişkili NAT kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="4b350-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="4b350-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b350-111">PARAMETERS</span></span>

### <span data-ttu-id="4b350-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b350-112">-DefaultProfile</span></span>
<span data-ttu-id="4b350-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b350-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b350-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b350-114">-LoadBalancer</span></span>
<span data-ttu-id="4b350-115">Alınacak gelen NAT kuralı yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b350-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="4b350-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b350-116">-Name</span></span>
<span data-ttu-id="4b350-117">Alınacak gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b350-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="4b350-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b350-118">CommonParameters</span></span>
<span data-ttu-id="4b350-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b350-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b350-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b350-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b350-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b350-121">INPUTS</span></span>

### <span data-ttu-id="4b350-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b350-122">PSLoadBalancer</span></span>
<span data-ttu-id="4b350-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4b350-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4b350-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b350-124">OUTPUTS</span></span>

### <span data-ttu-id="4b350-125">Microsoft. Azure. Commands. Network. model. Psınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="4b350-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="4b350-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b350-126">NOTES</span></span>

## <span data-ttu-id="4b350-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b350-127">RELATED LINKS</span></span>

[<span data-ttu-id="4b350-128">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4b350-128">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="4b350-129">New-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="4b350-129">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./New-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4b350-130">Remove-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="4b350-130">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="4b350-131">Set-Azurermloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="4b350-131">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


