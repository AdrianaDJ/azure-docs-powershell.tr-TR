---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1FDA90C0-D01F-45E1-9149-16AD04046271
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerinboundnatruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 6b866dc04975c2cde17509182e21936a2d6c9363
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935531"
---
# <span data-ttu-id="1d658-101">Get-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d658-101">Get-AzLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="1d658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d658-102">SYNOPSIS</span></span>
<span data-ttu-id="1d658-103">Bir yük dengeleyicinin gelen NAT kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="1d658-103">Gets an inbound NAT rule configuration for a load balancer.</span></span>

## <span data-ttu-id="1d658-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1d658-104">SYNTAX</span></span>

```
Get-AzLoadBalancerInboundNatRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d658-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1d658-105">DESCRIPTION</span></span>
<span data-ttu-id="1d658-106">**Get-Azloadbalancerınboundnatruleconfig** cmdlet 'i, bir Azure Yük dengeleyicide bir veya birden çok gelen ağ adresi ÇEVIRISI (NAT) kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="1d658-106">The **Get-AzLoadBalancerInboundNatRuleConfig** cmdlet gets one or more inbound network address translation (NAT) rules in an Azure load balancer.</span></span>

## <span data-ttu-id="1d658-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1d658-107">EXAMPLES</span></span>

### <span data-ttu-id="1d658-108">Örnek 1: gelen NAT kural yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="1d658-108">Example 1: Get an inbound NAT rule configuration</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule1" -LoadBalancer $slb
```

<span data-ttu-id="1d658-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="1d658-109">The first command gets the load balancer named MyLoadBalancer, and stores it in the variable $slb.</span></span>

<span data-ttu-id="1d658-110">İkinci komut, $slb MyInboundNatRule1 adındaki ilişkili NAT kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="1d658-110">The second command gets the associated NAT rule named MyInboundNatRule1 from the load balancer in $slb.</span></span>

## <span data-ttu-id="1d658-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1d658-111">PARAMETERS</span></span>

### <span data-ttu-id="1d658-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d658-112">-DefaultProfile</span></span>
<span data-ttu-id="1d658-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1d658-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d658-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1d658-114">-LoadBalancer</span></span>
<span data-ttu-id="1d658-115">Alınacak gelen NAT kuralı yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d658-115">Specifies the load balancer that is associated with the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="1d658-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="1d658-116">-Name</span></span>
<span data-ttu-id="1d658-117">Alınacak gelen NAT kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1d658-117">Specifies the name of the inbound NAT rule configuration to get.</span></span>

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

### <span data-ttu-id="1d658-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d658-118">CommonParameters</span></span>
<span data-ttu-id="1d658-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1d658-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d658-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d658-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d658-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1d658-121">INPUTS</span></span>

### <span data-ttu-id="1d658-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1d658-122">PSLoadBalancer</span></span>
<span data-ttu-id="1d658-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="1d658-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="1d658-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1d658-124">OUTPUTS</span></span>

### <span data-ttu-id="1d658-125">Microsoft. Azure. Commands. Network. model. Psınboundnatrule</span><span class="sxs-lookup"><span data-stu-id="1d658-125">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="1d658-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1d658-126">NOTES</span></span>

## <span data-ttu-id="1d658-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1d658-127">RELATED LINKS</span></span>

[<span data-ttu-id="1d658-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1d658-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="1d658-129">New-Azloadbalancerınboundnatruleconfig</span><span class="sxs-lookup"><span data-stu-id="1d658-129">New-AzLoadBalancerInboundNatRuleConfig</span></span>](./New-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1d658-130">Remove-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d658-130">Remove-AzLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="1d658-131">Set-AzLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1d658-131">Set-AzLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzLoadBalancerInboundNatRuleConfig.md)


