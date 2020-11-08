---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLoadBalancer.md
ms.openlocfilehash: 17af7cc61ec3d254133dd0563e8ea09fc0e3043f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936544"
---
# <span data-ttu-id="6cf12-101">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cf12-101">Set-AzLoadBalancer</span></span>

## <span data-ttu-id="6cf12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cf12-102">SYNOPSIS</span></span>
<span data-ttu-id="6cf12-103">Bir yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6cf12-103">Sets the goal state for a load balancer.</span></span>

## <span data-ttu-id="6cf12-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6cf12-104">SYNTAX</span></span>

```
Set-AzLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cf12-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6cf12-105">DESCRIPTION</span></span>
<span data-ttu-id="6cf12-106">**Set-AzLoadBalancer** cmdlet 'ı bir Azure Yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6cf12-106">The **Set-AzLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="6cf12-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6cf12-107">EXAMPLES</span></span>

### <span data-ttu-id="6cf12-108">Örnek 1: yük dengeleyiciyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="6cf12-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzLoadBalancer
```

<span data-ttu-id="6cf12-109">İlk komut NRPLB adlı yük dengeleyicın alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="6cf12-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="6cf12-110">İkinci $slb komut, (NewRule adlı bir gelen NAT kuralı ekleyen-AzLoadBalancerInboundNatRuleConfig öğesini ekleme</span><span class="sxs-lookup"><span data-stu-id="6cf12-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="6cf12-111">Üçüncü komut yük dengeleyicın **Ayarla-AzLoadBalancer** 'yi, yük dengeleyici yapılandırmasını güncelleştirir ve kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6cf12-111">The third command passes the load balancer to **Set-AzLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="6cf12-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6cf12-112">PARAMETERS</span></span>

### <span data-ttu-id="6cf12-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="6cf12-113">-AsJob</span></span>
<span data-ttu-id="6cf12-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6cf12-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cf12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cf12-115">-DefaultProfile</span></span>
<span data-ttu-id="6cf12-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6cf12-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cf12-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cf12-117">-LoadBalancer</span></span>
<span data-ttu-id="6cf12-118">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="6cf12-118">Specifies a load balancer.</span></span>
<span data-ttu-id="6cf12-119">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6cf12-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="6cf12-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cf12-120">CommonParameters</span></span>
<span data-ttu-id="6cf12-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6cf12-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cf12-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cf12-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cf12-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6cf12-123">INPUTS</span></span>

### <span data-ttu-id="6cf12-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cf12-124">PSLoadBalancer</span></span>
<span data-ttu-id="6cf12-125">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="6cf12-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="6cf12-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6cf12-126">OUTPUTS</span></span>

### <span data-ttu-id="6cf12-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cf12-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="6cf12-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6cf12-128">NOTES</span></span>

## <span data-ttu-id="6cf12-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6cf12-129">RELATED LINKS</span></span>

[<span data-ttu-id="6cf12-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cf12-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="6cf12-131">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cf12-131">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="6cf12-132">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="6cf12-132">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

