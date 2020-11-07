---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 192eb5ebfa21c97aa7043c4d4719831def08d93e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940046"
---
# <span data-ttu-id="d2b65-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="d2b65-101">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="d2b65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2b65-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b65-103">Bir yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2b65-103">Removes a front-end IP configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2b65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2b65-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerFrontendIpConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2b65-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2b65-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b65-106">**Remove-Azurermloadbalancerfrontendıcaconfig** cmdlet 'i, bir Azure yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2b65-106">The **Remove-AzureRmLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="d2b65-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2b65-107">EXAMPLES</span></span>

### <span data-ttu-id="d2b65-108">Örnek 1: yük dengeleyiciden ön uç IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="d2b65-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzureRmLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="d2b65-109">İlk komut, kaldırmak istediğiniz ön uç IP yapılandırmasıyla ilişkili yük dengeleyicın alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="d2b65-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>

<span data-ttu-id="d2b65-110">İkinci komut $loadbalancer ' da yük dengeleyiciden ilişkili ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d2b65-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="d2b65-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2b65-111">PARAMETERS</span></span>

### <span data-ttu-id="d2b65-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b65-112">-DefaultProfile</span></span>
<span data-ttu-id="d2b65-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2b65-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2b65-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2b65-114">-LoadBalancer</span></span>
<span data-ttu-id="d2b65-115">Kaldırılacak ön uç IP yapılandırmasını içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2b65-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="d2b65-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2b65-116">-Name</span></span>
<span data-ttu-id="d2b65-117">Kaldırılacak ön uç IP adresi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2b65-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="d2b65-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b65-118">CommonParameters</span></span>
<span data-ttu-id="d2b65-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2b65-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b65-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2b65-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b65-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2b65-121">INPUTS</span></span>

### <span data-ttu-id="d2b65-122">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2b65-122">PSLoadBalancer</span></span>
<span data-ttu-id="d2b65-123">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="d2b65-123">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="d2b65-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2b65-124">OUTPUTS</span></span>

### <span data-ttu-id="d2b65-125">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2b65-125">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d2b65-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2b65-126">NOTES</span></span>

## <span data-ttu-id="d2b65-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2b65-127">RELATED LINKS</span></span>

[<span data-ttu-id="d2b65-128">Add-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="d2b65-128">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d2b65-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d2b65-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="d2b65-130">Get-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="d2b65-130">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d2b65-131">Yeni-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="d2b65-131">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="d2b65-132">Set-Azurermloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="d2b65-132">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


