---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalanceroutboundruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerOutboundRuleConfig.md
ms.openlocfilehash: 1bcaab526ac2fbb82d696db7197bbc8d69c0078f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765100"
---
# <span data-ttu-id="11edd-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="11edd-101">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>

## <span data-ttu-id="11edd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11edd-102">SYNOPSIS</span></span>
<span data-ttu-id="11edd-103">Bir yük dengeleyicide giden kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="11edd-103">Gets an outbound rule configuration in a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11edd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="11edd-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11edd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="11edd-105">DESCRIPTION</span></span>
<span data-ttu-id="11edd-106">**Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet 'i, bir yük dengeleyicideki giden kural yapılandırmalarının bir listesini veya bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="11edd-106">The **Get-AzureRmLoadBalancerOutboundRuleConfig** cmdlet gets an outbound rule configuration or a list of outbound rule configurations in a load balancer.</span></span>

## <span data-ttu-id="11edd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="11edd-107">EXAMPLES</span></span>

### <span data-ttu-id="11edd-108">Örnek 1: yük dengeleyicide giden kural yapılandırması alma</span><span class="sxs-lookup"><span data-stu-id="11edd-108">Example 1: Get an outbound rule configuration in a load balancer</span></span>
```powershell
PS C:\>$slb = Get-AzureRmLoadBalancer -ResourceGroupName "MyResourceGroup" -Name "MyLoadBalancer"
PS C:\>Get-AzureRmLoadBalancerOutboundRuleConfig -LoadBalancer $slb -Name "MyRule"
```

<span data-ttu-id="11edd-109">İlk komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu $slb değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="11edd-109">The first command gets the load balancer named MyLoadBalancer, and then stores it in the variable $slb.</span></span>
<span data-ttu-id="11edd-110">İkinci komut, bu yük dengeleyiciyle ilişkilendirilmiş MyRule adlı giden kuralı yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="11edd-110">The second command gets the outbound rule configuration named MyRule associated with that load balancer.</span></span>

## <span data-ttu-id="11edd-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="11edd-111">PARAMETERS</span></span>

### <span data-ttu-id="11edd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11edd-112">-DefaultProfile</span></span>
<span data-ttu-id="11edd-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="11edd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11edd-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="11edd-114">-LoadBalancer</span></span>
<span data-ttu-id="11edd-115">Yük dengeleyici kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="11edd-115">The reference of the load balancer resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11edd-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="11edd-116">-Name</span></span>
<span data-ttu-id="11edd-117">Giden kuralının adı.</span><span class="sxs-lookup"><span data-stu-id="11edd-117">Name of the outbound rule.</span></span>

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

### <span data-ttu-id="11edd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11edd-118">CommonParameters</span></span>
<span data-ttu-id="11edd-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="11edd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11edd-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11edd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11edd-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="11edd-121">INPUTS</span></span>

### <span data-ttu-id="11edd-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="11edd-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="11edd-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="11edd-123">OUTPUTS</span></span>

### <span data-ttu-id="11edd-124">Microsoft. Azure. Commands. Network. model. PSOutboundRule</span><span class="sxs-lookup"><span data-stu-id="11edd-124">Microsoft.Azure.Commands.Network.Models.PSOutboundRule</span></span>

## <span data-ttu-id="11edd-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="11edd-125">NOTES</span></span>

## <span data-ttu-id="11edd-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="11edd-126">RELATED LINKS</span></span>
