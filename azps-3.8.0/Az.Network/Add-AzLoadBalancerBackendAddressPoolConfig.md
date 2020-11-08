---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: a1e0f8abdc8951155ab56b85f516145c9b6b1d1a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097547"
---
# <span data-ttu-id="d3134-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d3134-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="d3134-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3134-102">SYNOPSIS</span></span>
<span data-ttu-id="d3134-103">Bir yük dengeleyicisine arka uç adres havuzu yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="d3134-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="d3134-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3134-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3134-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3134-105">DESCRIPTION</span></span>
<span data-ttu-id="d3134-106">**Add-Azloadbalancerarka uç** cmdlet 'ı bir Azure yük dengeleyicisine bir arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="d3134-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="d3134-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3134-107">EXAMPLES</span></span>

### <span data-ttu-id="d3134-108">Örnek 1 yük dengeleyicisine arka uç adres havuzu yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="d3134-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="d3134-109">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır, BackendAddressPool02 adlı arka uç adres havuzunu MyLoadBalancer 'e ekler ve MyLoadBalancer öğesini güncelleştirmek için **set-AzLoadBalancer** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d3134-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="d3134-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3134-110">PARAMETERS</span></span>

### <span data-ttu-id="d3134-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3134-111">-DefaultProfile</span></span>
<span data-ttu-id="d3134-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3134-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3134-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3134-113">-LoadBalancer</span></span>
<span data-ttu-id="d3134-114">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3134-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="d3134-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3134-115">-Name</span></span>
<span data-ttu-id="d3134-116">Eklenecek arka uç adres havuzu yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3134-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3134-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3134-117">-Confirm</span></span>
<span data-ttu-id="d3134-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3134-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3134-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3134-119">-WhatIf</span></span>
<span data-ttu-id="d3134-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3134-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3134-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3134-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3134-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3134-122">CommonParameters</span></span>
<span data-ttu-id="d3134-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3134-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3134-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3134-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3134-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3134-125">INPUTS</span></span>

### <span data-ttu-id="d3134-126">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3134-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d3134-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3134-127">OUTPUTS</span></span>

### <span data-ttu-id="d3134-128">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3134-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d3134-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3134-129">NOTES</span></span>

## <span data-ttu-id="d3134-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3134-130">RELATED LINKS</span></span>

[<span data-ttu-id="d3134-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d3134-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="d3134-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d3134-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="d3134-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d3134-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d3134-134">Yeni-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d3134-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="d3134-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="d3134-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)

