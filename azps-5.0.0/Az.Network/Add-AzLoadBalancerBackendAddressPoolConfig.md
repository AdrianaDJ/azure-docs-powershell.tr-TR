---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 39e388fbdb809f136942749a0d0585189155e32b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280015"
---
# <span data-ttu-id="b941a-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b941a-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="b941a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b941a-102">SYNOPSIS</span></span>
<span data-ttu-id="b941a-103">Bir yük dengeleyicisine arka uç adres havuzu yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b941a-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="b941a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b941a-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b941a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b941a-105">DESCRIPTION</span></span>
<span data-ttu-id="b941a-106">**Add-Azloadbalancerarka uç** cmdlet 'ı bir Azure yük dengeleyicisine bir arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="b941a-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="b941a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b941a-107">EXAMPLES</span></span>

### <span data-ttu-id="b941a-108">Örnek 1: yük dengeleyicisine arka uç adres havuzu yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="b941a-108">Example 1: Add a backend address pool configuration to a load balancer</span></span>
```powershell
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="b941a-109">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır, BackendAddressPool02 adlı arka uç adres havuzunu MyLoadBalancer 'e ekler ve MyLoadBalancer öğesini güncelleştirmek için **set-AzLoadBalancer** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="b941a-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="b941a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b941a-110">PARAMETERS</span></span>

### <span data-ttu-id="b941a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b941a-111">-DefaultProfile</span></span>
<span data-ttu-id="b941a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b941a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b941a-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b941a-113">-LoadBalancer</span></span>
<span data-ttu-id="b941a-114">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b941a-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="b941a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b941a-115">-Name</span></span>
<span data-ttu-id="b941a-116">Eklenecek arka uç adres havuzu yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b941a-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="b941a-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="b941a-117">-Confirm</span></span>
<span data-ttu-id="b941a-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b941a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b941a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b941a-119">-WhatIf</span></span>
<span data-ttu-id="b941a-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b941a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b941a-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b941a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b941a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b941a-122">CommonParameters</span></span>
<span data-ttu-id="b941a-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b941a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b941a-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b941a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b941a-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b941a-125">INPUTS</span></span>

### <span data-ttu-id="b941a-126">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b941a-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b941a-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b941a-127">OUTPUTS</span></span>

### <span data-ttu-id="b941a-128">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b941a-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="b941a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b941a-129">NOTES</span></span>

## <span data-ttu-id="b941a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b941a-130">RELATED LINKS</span></span>

[<span data-ttu-id="b941a-131">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b941a-131">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="b941a-132">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="b941a-132">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="b941a-133">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b941a-133">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b941a-134">Yeni-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b941a-134">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="b941a-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="b941a-135">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


