---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6BEED413-E2E4-4557-BD31-2A655E790C1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: a0b1acf49aa177d05be7361eedf644320b609797
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935541"
---
# <span data-ttu-id="bad1e-101">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="bad1e-101">Get-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="bad1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bad1e-102">SYNOPSIS</span></span>
<span data-ttu-id="bad1e-103">Bir yük dengeleyicide ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="bad1e-103">Gets a front-end IP configuration in a load balancer.</span></span>

## <span data-ttu-id="bad1e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bad1e-104">SYNTAX</span></span>

```
Get-AzLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bad1e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bad1e-105">DESCRIPTION</span></span>
<span data-ttu-id="bad1e-106">**Get-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir yük dengeleyicide ön uç IP yapılandırmalarını veya ön uç IP yapılandırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="bad1e-106">The **Get-AzLoadBalancerFrontendIpConfig** cmdlet gets a front-end IP configuration or a list of front-end IP configurations in a load balancer.</span></span>

## <span data-ttu-id="bad1e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bad1e-107">EXAMPLES</span></span>

### <span data-ttu-id="bad1e-108">Örnek 1: yük dengeleyicide ön uç IP yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="bad1e-108">Example 1: Get a front-end IP configuration in a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerFrontendIpConfig -Name "MyFrontEnd" -LoadBalancer $slb
```

<span data-ttu-id="bad1e-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="bad1e-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="bad1e-110">İkinci komut, bu yük dengeleyiciyle ilişkilendirilmiş ön uç IP yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="bad1e-110">The second command gets the front end IP configuration associated with that load balancer.</span></span>

## <span data-ttu-id="bad1e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bad1e-111">PARAMETERS</span></span>

### <span data-ttu-id="bad1e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad1e-112">-DefaultProfile</span></span>
<span data-ttu-id="bad1e-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bad1e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bad1e-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bad1e-114">-LoadBalancer</span></span>
<span data-ttu-id="bad1e-115">Alınacak ön uç IP yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad1e-115">Specifies the load balancer that is associated with the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="bad1e-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="bad1e-116">-Name</span></span>
<span data-ttu-id="bad1e-117">Alınacak ön uç IP yapılandırmasını içeren yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bad1e-117">Specifies the name of the load balancer that contains the front-end IP configuration to get.</span></span>

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

### <span data-ttu-id="bad1e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad1e-118">CommonParameters</span></span>
<span data-ttu-id="bad1e-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bad1e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad1e-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad1e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad1e-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bad1e-121">INPUTS</span></span>

### <span data-ttu-id="bad1e-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bad1e-122">PSLoadBalancer</span></span>
<span data-ttu-id="bad1e-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="bad1e-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="bad1e-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bad1e-124">OUTPUTS</span></span>

### <span data-ttu-id="bad1e-125">Microsoft. Azure. Commands. Network. model. Psfrontendıconfiguration yapılandırması</span><span class="sxs-lookup"><span data-stu-id="bad1e-125">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="bad1e-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bad1e-126">NOTES</span></span>

## <span data-ttu-id="bad1e-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bad1e-127">RELATED LINKS</span></span>

[<span data-ttu-id="bad1e-128">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="bad1e-128">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="bad1e-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="bad1e-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="bad1e-130">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="bad1e-130">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="bad1e-131">Remove-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="bad1e-131">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="bad1e-132">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="bad1e-132">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

