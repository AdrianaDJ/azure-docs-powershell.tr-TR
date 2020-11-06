---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 02756d382cf785d4cfecfa6f73a580e125dc5e39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592194"
---
# <span data-ttu-id="829e6-101">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="829e6-101">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="829e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="829e6-102">SYNOPSIS</span></span>
<span data-ttu-id="829e6-103">Bir yük dengeleyicide ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="829e6-103">Gets a front-end IP configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="829e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="829e6-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="829e6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="829e6-105">DESCRIPTION</span></span>
<span data-ttu-id="829e6-106">**Get-Azurermloadbalancerfrontenınconfıg** cmdlet 'i, ön uç IP yapılandırmasını veya bir yük dengeleyicideki ön uç IP yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="829e6-106">The **Get-AzureRmLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="829e6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="829e6-107">EXAMPLES</span></span>

### <span data-ttu-id="829e6-108">Örnek 1: yük dengeleyicide ön uç IP yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="829e6-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="829e6-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="829e6-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="829e6-110">İkinci komut, bu yük dengeleyiciyle ilişkilendirilmiş ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="829e6-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="829e6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="829e6-111">PARAMETERS</span></span>

### <span data-ttu-id="829e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="829e6-112">-DefaultProfile</span></span>
<span data-ttu-id="829e6-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="829e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="829e6-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="829e6-114">-LoadBalancer</span></span>
<span data-ttu-id="829e6-115">Alınacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="829e6-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="829e6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="829e6-116">-Name</span></span>
<span data-ttu-id="829e6-117">Alınacak ön uç IP yapılandırmasını içeren yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="829e6-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="829e6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829e6-118">CommonParameters</span></span>
<span data-ttu-id="829e6-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="829e6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829e6-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="829e6-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829e6-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="829e6-121">INPUTS</span></span>

### <span data-ttu-id="829e6-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="829e6-122">PSLoadBalancer</span></span>
<span data-ttu-id="829e6-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="829e6-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="829e6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="829e6-124">OUTPUTS</span></span>

### <span data-ttu-id="829e6-125">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="829e6-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="829e6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="829e6-126">NOTES</span></span>

## <span data-ttu-id="829e6-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="829e6-127">RELATED LINKS</span></span>

[<span data-ttu-id="829e6-128">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="829e6-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="829e6-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="829e6-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="829e6-130">Yeni-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="829e6-130">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="829e6-131">Remove-Azurermloadbalancerfrontendıconfig</span><span class="sxs-lookup"><span data-stu-id="829e6-131">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="829e6-132">Set-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="829e6-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


