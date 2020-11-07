---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5F8E11DF-D560-44D7-99CA-C425951A56D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 75a12ab9543eb19301cc8e17e4ebff6e4db80c00
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760164"
---
# <span data-ttu-id="c322f-101">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c322f-101">Remove-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="c322f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c322f-102">SYNOPSIS</span></span>
<span data-ttu-id="c322f-103">Bir yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c322f-103">Removes a front-end IP configuration from a load balancer.</span></span>

## <span data-ttu-id="c322f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c322f-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerFrontendIpConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c322f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c322f-105">DESCRIPTION</span></span>
<span data-ttu-id="c322f-106">**Remove-Azloadbalancerfrontendıconfıg** cmdlet 'i, bir Azure yük dengeleyiciden ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c322f-106">The **Remove-AzLoadBalancerFrontendIpConfig** cmdlet removes a front-end IP configuration from an Azure load balancer.</span></span>

## <span data-ttu-id="c322f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c322f-107">EXAMPLES</span></span>

### <span data-ttu-id="c322f-108">Örnek 1: yük dengeleyiciden ön uç IP yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c322f-108">Example 1: Remove a front-end IP configuration from a load balancer</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:> Remove-AzLoadBalancerFrontendIpConfig -Name "frontendName" -LoadBalancer $loadbalancer
```

<span data-ttu-id="c322f-109">İlk komut, kaldırmak istediğiniz ön uç IP yapılandırmasıyla ilişkili yük dengeleyicın alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c322f-109">The first command gets the load balancer that is associated with the front-end IP configuration you want to remove, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="c322f-110">İkinci komut $loadbalancer ' da yük dengeleyiciden ilişkili ön uç IP yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c322f-110">The second command removes the associated frontend IP configuration from the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="c322f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c322f-111">PARAMETERS</span></span>

### <span data-ttu-id="c322f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c322f-112">-DefaultProfile</span></span>
<span data-ttu-id="c322f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c322f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c322f-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c322f-114">-LoadBalancer</span></span>
<span data-ttu-id="c322f-115">Kaldırılacak ön uç IP yapılandırmasını içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="c322f-115">Specifies the load balancer that contains the front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="c322f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c322f-116">-Name</span></span>
<span data-ttu-id="c322f-117">Kaldırılacak ön uç IP adresi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c322f-117">Specifies the name of the front-end IP address configuration to remove.</span></span>

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

### <span data-ttu-id="c322f-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="c322f-118">-Confirm</span></span>
<span data-ttu-id="c322f-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c322f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c322f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c322f-120">-WhatIf</span></span>
<span data-ttu-id="c322f-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c322f-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c322f-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c322f-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c322f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c322f-123">CommonParameters</span></span>
<span data-ttu-id="c322f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c322f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c322f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c322f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c322f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c322f-126">INPUTS</span></span>

### <span data-ttu-id="c322f-127">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c322f-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c322f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c322f-128">OUTPUTS</span></span>

### <span data-ttu-id="c322f-129">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c322f-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c322f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c322f-130">NOTES</span></span>

## <span data-ttu-id="c322f-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c322f-131">RELATED LINKS</span></span>

[<span data-ttu-id="c322f-132">Add-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="c322f-132">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c322f-133">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c322f-133">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c322f-134">Get-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="c322f-134">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c322f-135">Yeni-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="c322f-135">New-AzLoadBalancerFrontendIpConfig</span></span>](./New-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="c322f-136">Set-Azloadbalancerfrontendıconfıg</span><span class="sxs-lookup"><span data-stu-id="c322f-136">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)

