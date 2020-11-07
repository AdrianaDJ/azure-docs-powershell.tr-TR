---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 11de4e8966b5e57e817b6c5d829536deacf229f8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935290"
---
# <span data-ttu-id="ecf67-101">Remove-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ecf67-101">Remove-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ecf67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecf67-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf67-103">Bir yük dengeleyiciden bir yoklama yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ecf67-103">Removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="ecf67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ecf67-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ecf67-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf67-106">**Remove-AzLoadBalancerProbeConfig** cmdlet 'i yük dengeleyiciden bir yoklama yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ecf67-106">The **Remove-AzLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="ecf67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ecf67-107">EXAMPLES</span></span>

### <span data-ttu-id="ecf67-108">Örnek 1: yük dengeleyiciden yoklama yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ecf67-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="ecf67-109">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ecf67-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="ecf67-110">İkinci komut, $loadbalancer 'daki yük dengeleyiciden Myyoklama adlı yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="ecf67-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="ecf67-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ecf67-111">PARAMETERS</span></span>

### <span data-ttu-id="ecf67-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf67-112">-DefaultProfile</span></span>
<span data-ttu-id="ecf67-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ecf67-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecf67-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ecf67-114">-LoadBalancer</span></span>
<span data-ttu-id="ecf67-115">Bu cmdlet 'in kaldırıldığı yoklama yapılandırmasını içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecf67-115">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ecf67-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ecf67-116">-Name</span></span>
<span data-ttu-id="ecf67-117">Bu cmdlet 'in kaldırıldığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ecf67-117">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ecf67-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf67-118">CommonParameters</span></span>
<span data-ttu-id="ecf67-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ecf67-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf67-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf67-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf67-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ecf67-121">INPUTS</span></span>

### <span data-ttu-id="ecf67-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ecf67-122">PSLoadBalancer</span></span>
<span data-ttu-id="ecf67-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ecf67-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ecf67-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ecf67-124">OUTPUTS</span></span>

### <span data-ttu-id="ecf67-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ecf67-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ecf67-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ecf67-126">NOTES</span></span>

## <span data-ttu-id="ecf67-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ecf67-127">RELATED LINKS</span></span>

[<span data-ttu-id="ecf67-128">Add-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ecf67-128">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ecf67-129">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ecf67-129">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ecf67-130">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ecf67-130">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ecf67-131">Yeni-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ecf67-131">New-AzLoadBalancerProbeConfig</span></span>](./New-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="ecf67-132">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ecf67-132">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


