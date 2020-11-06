---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 494E185D-3746-4959-846E-660017A1F392
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLoadBalancer.md
ms.openlocfilehash: 463b9cf07bbb04273e1653f4d84805de3802b616
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588878"
---
# <span data-ttu-id="d8ad9-101">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8ad9-101">Set-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="d8ad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ad9-103">Bir yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-103">Sets the goal state for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8ad9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8ad9-104">SYNTAX</span></span>

```
Set-AzureRmLoadBalancer -LoadBalancer <PSLoadBalancer> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8ad9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ad9-106">**Set-AzureRmLoadBalancer** cmdlet 'ı bir Azure Yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-106">The **Set-AzureRmLoadBalancer** cmdlet sets the goal state for an Azure load balancer.</span></span>

## <span data-ttu-id="d8ad9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8ad9-107">EXAMPLES</span></span>

### <span data-ttu-id="d8ad9-108">Örnek 1: yük dengeleyiciyi değiştirme</span><span class="sxs-lookup"><span data-stu-id="d8ad9-108">Example 1: Modify a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "NRPLB" -ResourceGroupName "NRP-RG"
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatRuleConfig -Name "NewRule" -FrontendIpConfiguration $slb.FrontendIpConfigurations[0] -FrontendPort 81 -BackendPort 8181 -Protocol "TCP"
PS C:\> $slb | Set-AzureRmLoadBalancer
```

<span data-ttu-id="d8ad9-109">İlk komut NRPLB adlı yük dengeleyicın alır ve $slb değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-109">The first command gets the load balancer named NRPLB, and then stores it in the $slb variable.</span></span>

<span data-ttu-id="d8ad9-110">İkinci $slb komut, (NewRule adlı bir gelen NAT kuralı ekleyen-AzureRmLoadBalancerInboundNatRuleConfig öğesini ekleme</span><span class="sxs-lookup"><span data-stu-id="d8ad9-110">The second command uses the pipeline operator to pass the load balancer in $slb to Add-AzureRmLoadBalancerInboundNatRuleConfig, which adds an inbound NAT rule named NewRule.</span></span>

<span data-ttu-id="d8ad9-111">Üçüncü komut yük dengeleyiciyi, yük dengeleyici yapılandırmasını güncelleştiren ve kaydeden **-AzureRmLoadBalancer** değerini geçirir.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-111">The third command passes the load balancer to **Set-AzureRmLoadBalancer** , which updates the load balancer configuration and saves it.</span></span>

## <span data-ttu-id="d8ad9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8ad9-112">PARAMETERS</span></span>

### <span data-ttu-id="d8ad9-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d8ad9-113">-AsJob</span></span>
<span data-ttu-id="d8ad9-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d8ad9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8ad9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ad9-115">-DefaultProfile</span></span>
<span data-ttu-id="d8ad9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8ad9-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8ad9-117">-LoadBalancer</span></span>
<span data-ttu-id="d8ad9-118">Bir yük dengeleyici belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-118">Specifies a load balancer.</span></span>
<span data-ttu-id="d8ad9-119">Bu cmdlet, bu parametrenin belirttiği yük dengeleyicinin hedef durumunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-119">This cmdlet sets the goal state for the load balancer that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8ad9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ad9-120">CommonParameters</span></span>
<span data-ttu-id="d8ad9-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ad9-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ad9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ad9-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8ad9-123">INPUTS</span></span>

### <span data-ttu-id="d8ad9-124">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8ad9-124">PSLoadBalancer</span></span>
<span data-ttu-id="d8ad9-125">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d8ad9-125">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d8ad9-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8ad9-126">OUTPUTS</span></span>

### <span data-ttu-id="d8ad9-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8ad9-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d8ad9-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8ad9-128">NOTES</span></span>

## <span data-ttu-id="d8ad9-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8ad9-129">RELATED LINKS</span></span>

[<span data-ttu-id="d8ad9-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8ad9-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d8ad9-131">Yeni-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8ad9-131">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="d8ad9-132">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d8ad9-132">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)


