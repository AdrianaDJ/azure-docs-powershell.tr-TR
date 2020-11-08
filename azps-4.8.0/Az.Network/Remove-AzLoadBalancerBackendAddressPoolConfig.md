---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 26f7e0dde825305e888d598a23af0b2fbaff81cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265960"
---
# <span data-ttu-id="0469e-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0469e-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="0469e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0469e-102">SYNOPSIS</span></span>
<span data-ttu-id="0469e-103">Bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0469e-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="0469e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0469e-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0469e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0469e-105">DESCRIPTION</span></span>
<span data-ttu-id="0469e-106">**Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet 'i, bir yük dengeleyiciden bir arka uç adres havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0469e-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="0469e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0469e-107">EXAMPLES</span></span>

### <span data-ttu-id="0469e-108">Örnek 1: bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0469e-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="0469e-109">Bu komut MyLoadBalancer adlı yük dengeleyiciden alır ve BackendAddressPool02 yapılandırmasını MyLoadBalancer 'dan kaldıran **-AzLoadBalancerBackendAddressPoolConfig** öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0469e-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="0469e-110">Son olarak, Set-AzLoadBalancer cmdlet MyLoadBalancer öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0469e-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="0469e-111">Arka uç adres havuzu yapılandırmasının silebilmek için mevcut olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="0469e-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="0469e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0469e-112">PARAMETERS</span></span>

### <span data-ttu-id="0469e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0469e-113">-DefaultProfile</span></span>
<span data-ttu-id="0469e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0469e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0469e-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0469e-115">-LoadBalancer</span></span>
<span data-ttu-id="0469e-116">Kaldırılacak arka uç adres havuzunu içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="0469e-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="0469e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0469e-117">-Name</span></span>
<span data-ttu-id="0469e-118">Bu cmdlet 'in kaldırıldığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0469e-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0469e-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="0469e-119">-Confirm</span></span>
<span data-ttu-id="0469e-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0469e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0469e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0469e-121">-WhatIf</span></span>
<span data-ttu-id="0469e-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0469e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0469e-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0469e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0469e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0469e-124">CommonParameters</span></span>
<span data-ttu-id="0469e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0469e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0469e-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0469e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0469e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0469e-127">INPUTS</span></span>

### <span data-ttu-id="0469e-128">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0469e-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0469e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0469e-129">OUTPUTS</span></span>

### <span data-ttu-id="0469e-130">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0469e-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0469e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0469e-131">NOTES</span></span>

## <span data-ttu-id="0469e-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0469e-132">RELATED LINKS</span></span>

[<span data-ttu-id="0469e-133">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0469e-133">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="0469e-134">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0469e-134">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="0469e-135">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0469e-135">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="0469e-136">Yeni-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0469e-136">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


