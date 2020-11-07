---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DEBD58A3-AFAF-485C-8708-53228625138F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerRuleConfig.md
ms.openlocfilehash: 38f6223fdf1dc230dbd34310b7eda2ab45e2d4b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762053"
---
# <span data-ttu-id="62d74-101">Remove-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62d74-101">Remove-AzureRmLoadBalancerRuleConfig</span></span>

## <span data-ttu-id="62d74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62d74-102">SYNOPSIS</span></span>
<span data-ttu-id="62d74-103">Bir yük dengeleyicinin kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62d74-103">Removes a rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62d74-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62d74-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerRuleConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62d74-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62d74-105">DESCRIPTION</span></span>
<span data-ttu-id="62d74-106">**Remove-AzureRmLoadBalancerRuleConfig** cmdlet 'i, bir Azure Yük dengeleyicinin bir kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62d74-106">The **Remove-AzureRmLoadBalancerRuleConfig** cmdlet removes a rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="62d74-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62d74-107">EXAMPLES</span></span>

### <span data-ttu-id="62d74-108">Örnek 1: yük dengeleyiciden bir kural yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="62d74-108">Example 1: Remove a rule configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerRuleConfig -Name "MyLBruleName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="62d74-109">İlk komut MyLoadBalancer adındaki yük dengeleyiciden alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="62d74-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="62d74-110">İkinci komut, $loadbalancer 'daki yük dengeleyiciden MyLBruleName adlı kural yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="62d74-110">The second command removes the rule configuration named MyLBruleName from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="62d74-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62d74-111">PARAMETERS</span></span>

### <span data-ttu-id="62d74-112">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62d74-112">-LoadBalancer</span></span>
<span data-ttu-id="62d74-113">Bu cmdlet 'in kaldırıldığı kural yapılandırmasını içeren **LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="62d74-113">Specifies the **LoadBalancer** object that contains the rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="62d74-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="62d74-114">-Name</span></span>
<span data-ttu-id="62d74-115">Bu cmdlet 'in kaldırıldığı yük dengeleyici kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62d74-115">Specifies the name of the load balancer rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="62d74-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d74-116">-DefaultProfile</span></span>
<span data-ttu-id="62d74-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62d74-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62d74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d74-118">CommonParameters</span></span>
<span data-ttu-id="62d74-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62d74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d74-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62d74-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d74-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62d74-121">INPUTS</span></span>

### <span data-ttu-id="62d74-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62d74-122">PSLoadBalancer</span></span>
<span data-ttu-id="62d74-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="62d74-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="62d74-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62d74-124">OUTPUTS</span></span>

### <span data-ttu-id="62d74-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62d74-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="62d74-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62d74-126">NOTES</span></span>

## <span data-ttu-id="62d74-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62d74-127">RELATED LINKS</span></span>

[<span data-ttu-id="62d74-128">Add-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62d74-128">Add-AzureRmLoadBalancerRuleConfig</span></span>](./Add-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="62d74-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="62d74-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="62d74-130">Get-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62d74-130">Get-AzureRmLoadBalancerRuleConfig</span></span>](./Get-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="62d74-131">Yeni-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62d74-131">New-AzureRmLoadBalancerRuleConfig</span></span>](./New-AzureRmLoadBalancerRuleConfig.md)

[<span data-ttu-id="62d74-132">Set-AzureRmLoadBalancerRuleConfig</span><span class="sxs-lookup"><span data-stu-id="62d74-132">Set-AzureRmLoadBalancerRuleConfig</span></span>](./Set-AzureRmLoadBalancerRuleConfig.md)


