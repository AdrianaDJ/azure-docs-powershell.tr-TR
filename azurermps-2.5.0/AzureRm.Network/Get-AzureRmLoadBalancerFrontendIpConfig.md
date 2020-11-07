---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: a80fa84beaaea0307447f25767d665c465e8c2aa
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938808"
---
# <span data-ttu-id="84724-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="84724-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="84724-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84724-102">SYNOPSIS</span></span>
<span data-ttu-id="84724-103">Bir yük dengeleyicide ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="84724-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84724-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84724-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84724-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84724-105">DESCRIPTION</span></span>
<span data-ttu-id="84724-106">**Get-Azurermloadbalancerfrontenınconfıg** cmdlet 'i, ön uç IP yapılandırmasını veya bir yük dengeleyicideki ön uç IP yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="84724-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="84724-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84724-107">EXAMPLES</span></span>

### <span data-ttu-id="84724-108">Örnek 1: yük dengeleyicide ön uç IP yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="84724-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="84724-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="84724-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="84724-110">İkinci komut, bu yük dengeleyiciyle ilişkilendirilmiş ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="84724-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="84724-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84724-111">PARAMETERS</span></span>

### <span data-ttu-id="84724-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84724-112">-DefaultProfile</span></span>
<span data-ttu-id="84724-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="84724-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84724-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84724-114">-LoadBalancer</span></span>
<span data-ttu-id="84724-115">Alınacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="84724-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="84724-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="84724-116">-Name</span></span>
<span data-ttu-id="84724-117">Alınacak ön uç IP yapılandırmasını içeren yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="84724-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="84724-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84724-118">CommonParameters</span></span>
<span data-ttu-id="84724-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84724-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84724-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84724-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84724-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84724-121">INPUTS</span></span>

### <span data-ttu-id="84724-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84724-122">PSLoadBalancer</span></span>
<span data-ttu-id="84724-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="84724-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="84724-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84724-124">OUTPUTS</span></span>

### <span data-ttu-id="84724-125">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="84724-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="84724-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84724-126">NOTES</span></span>

## <span data-ttu-id="84724-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84724-127">RELATED LINKS</span></span>

[<span data-ttu-id="84724-128">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="84724-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="84724-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="84724-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="84724-130">Yeni-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="84724-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="84724-131">Remove-Azurermloadbalancerfrontendıconfig</span><span class="sxs-lookup"><span data-stu-id="84724-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="84724-132">Set-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="84724-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


