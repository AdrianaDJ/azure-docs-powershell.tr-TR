---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 278228EB-0126-4F27-A30F-51DC498C65FE
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: bf106b9fbe4c8f069f2d7b5b1b2a9beae95cd51b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935528"
---
# <span data-ttu-id="80a9f-101">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80a9f-101">Get-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="80a9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="80a9f-103">Bir yük dengeleyicinin yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="80a9f-103">Gets a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="80a9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="80a9f-104">SYNTAX</span></span>

```
Get-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80a9f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="80a9f-105">DESCRIPTION</span></span>
<span data-ttu-id="80a9f-106">**Get-AzLoadBalancerProbeConfig** cmdlet 'i bir yük dengeleyicinin bir veya daha fazla yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="80a9f-106">The **Get-AzLoadBalancerProbeConfig** cmdlet gets one or more probe configurations for a load balancer.</span></span>

## <span data-ttu-id="80a9f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="80a9f-107">EXAMPLES</span></span>

### <span data-ttu-id="80a9f-108">Örnek 1: yük dengeleyicinin yoklama yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="80a9f-108">Example 1: Get the probe configuration of a load balancer</span></span>
```
PS C:\>$slb = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $slb
```

<span data-ttu-id="80a9f-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="80a9f-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>

<span data-ttu-id="80a9f-110">İkinci komut, $slb 'daki yük dengeleyiciden Myyoklama adlı ilişkili yoklama yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="80a9f-110">The second command gets the associated probe configuration named MyProbe from the load balancer in $slb.</span></span>

## <span data-ttu-id="80a9f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="80a9f-111">PARAMETERS</span></span>

### <span data-ttu-id="80a9f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a9f-112">-DefaultProfile</span></span>
<span data-ttu-id="80a9f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="80a9f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80a9f-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80a9f-114">-LoadBalancer</span></span>
<span data-ttu-id="80a9f-115">Alınacak yoklama yapılandırmasıyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="80a9f-115">Specifies the load balancer that is associated with the probe configuration to get.</span></span>

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

### <span data-ttu-id="80a9f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="80a9f-116">-Name</span></span>
<span data-ttu-id="80a9f-117">Alınacak yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="80a9f-117">Specifies the name of the probe configuration to get.</span></span>

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

### <span data-ttu-id="80a9f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a9f-118">CommonParameters</span></span>
<span data-ttu-id="80a9f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="80a9f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a9f-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a9f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a9f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="80a9f-121">INPUTS</span></span>

### <span data-ttu-id="80a9f-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80a9f-122">PSLoadBalancer</span></span>
<span data-ttu-id="80a9f-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="80a9f-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="80a9f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="80a9f-124">OUTPUTS</span></span>

### <span data-ttu-id="80a9f-125">Microsoft. Azure. Commands. Network. modeller. Psaraştırması</span><span class="sxs-lookup"><span data-stu-id="80a9f-125">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="80a9f-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="80a9f-126">NOTES</span></span>

## <span data-ttu-id="80a9f-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="80a9f-127">RELATED LINKS</span></span>

[<span data-ttu-id="80a9f-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80a9f-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="80a9f-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="80a9f-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="80a9f-130">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80a9f-130">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="80a9f-131">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80a9f-131">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="80a9f-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80a9f-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


