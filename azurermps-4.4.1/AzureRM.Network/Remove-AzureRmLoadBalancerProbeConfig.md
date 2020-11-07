---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B15B224-E36C-454B-B6C2-F2BE032AE962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 132ec5259a6d03591860dceaaa215f8db57c27dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762055"
---
# <span data-ttu-id="21d96-101">Remove-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="21d96-101">Remove-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="21d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21d96-102">SYNOPSIS</span></span>
<span data-ttu-id="21d96-103">Bir yük dengeleyiciden bir yoklama yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="21d96-103">Removes a probe configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21d96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21d96-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerProbeConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21d96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21d96-105">DESCRIPTION</span></span>
<span data-ttu-id="21d96-106">**Remove-AzureRmLoadBalancerProbeConfig** cmdlet 'i yük dengeleyiciden bir yoklama yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="21d96-106">The **Remove-AzureRmLoadBalancerProbeConfig** cmdlet removes a probe configuration from a load balancer.</span></span>

## <span data-ttu-id="21d96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21d96-107">EXAMPLES</span></span>

### <span data-ttu-id="21d96-108">Örnek 1: yük dengeleyiciden yoklama yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="21d96-108">Example 1: Remove a probe configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -LoadBalancer $loadbalancer
```

<span data-ttu-id="21d96-109">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="21d96-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="21d96-110">İkinci komut, $loadbalancer 'daki yük dengeleyiciden Myyoklama adlı yapılandırmayı siler.</span><span class="sxs-lookup"><span data-stu-id="21d96-110">The second command deletes the configuration named MyProbe from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="21d96-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21d96-111">PARAMETERS</span></span>

### <span data-ttu-id="21d96-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21d96-112">-LoadBalancer</span></span>
<span data-ttu-id="21d96-113">Bu cmdlet 'in kaldırıldığı yoklama yapılandırmasını içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="21d96-113">Specifies the load balancer that contains the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="21d96-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="21d96-114">-Name</span></span>
<span data-ttu-id="21d96-115">Bu cmdlet 'in kaldırıldığı yoklama yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="21d96-115">Specifies the name of the probe configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="21d96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d96-116">-DefaultProfile</span></span>
<span data-ttu-id="21d96-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21d96-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21d96-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d96-118">CommonParameters</span></span>
<span data-ttu-id="21d96-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21d96-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d96-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d96-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d96-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21d96-121">INPUTS</span></span>

### <span data-ttu-id="21d96-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21d96-122">PSLoadBalancer</span></span>
<span data-ttu-id="21d96-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="21d96-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="21d96-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21d96-124">OUTPUTS</span></span>

### <span data-ttu-id="21d96-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21d96-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="21d96-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21d96-126">NOTES</span></span>

## <span data-ttu-id="21d96-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21d96-127">RELATED LINKS</span></span>

[<span data-ttu-id="21d96-128">Add-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="21d96-128">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="21d96-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="21d96-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="21d96-130">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="21d96-130">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="21d96-131">Yeni-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="21d96-131">New-AzureRmLoadBalancerProbeConfig</span></span>](./New-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="21d96-132">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="21d96-132">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


