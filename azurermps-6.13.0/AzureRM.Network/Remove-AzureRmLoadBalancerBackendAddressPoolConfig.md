---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 065aa3718f1a66949265e7dca39880c1eff21fa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762470"
---
# <span data-ttu-id="30e6f-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="30e6f-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="30e6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="30e6f-103">Bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30e6f-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30e6f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30e6f-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30e6f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30e6f-105">DESCRIPTION</span></span>
<span data-ttu-id="30e6f-106">**Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet 'i, bir yük dengeleyiciden bir arka uç adres havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30e6f-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="30e6f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30e6f-107">EXAMPLES</span></span>

### <span data-ttu-id="30e6f-108">Örnek 1: bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="30e6f-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="30e6f-109">Bu komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu **kaldırmak** Için myloadbalancer 'dan BackendAddressPool02 yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30e6f-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="30e6f-110">Son olarak, Set-AzureRmLoadBalancer cmdlet MyLoadBalancer öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="30e6f-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="30e6f-111">Arka uç adres havuzu yapılandırmasının silebilmek için mevcut olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="30e6f-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="30e6f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30e6f-112">PARAMETERS</span></span>

### <span data-ttu-id="30e6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e6f-113">-DefaultProfile</span></span>
<span data-ttu-id="30e6f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30e6f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30e6f-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30e6f-115">-LoadBalancer</span></span>
<span data-ttu-id="30e6f-116">Kaldırılacak arka uç adres havuzunu içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e6f-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="30e6f-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="30e6f-117">-Name</span></span>
<span data-ttu-id="30e6f-118">Bu cmdlet 'in kaldırıldığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="30e6f-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="30e6f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="30e6f-119">-Confirm</span></span>
<span data-ttu-id="30e6f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30e6f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30e6f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30e6f-121">-WhatIf</span></span>
<span data-ttu-id="30e6f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30e6f-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30e6f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30e6f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30e6f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e6f-124">CommonParameters</span></span>
<span data-ttu-id="30e6f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30e6f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e6f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e6f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e6f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30e6f-127">INPUTS</span></span>

### <span data-ttu-id="30e6f-128">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30e6f-128">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="30e6f-129">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="30e6f-129">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="30e6f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30e6f-130">OUTPUTS</span></span>

### <span data-ttu-id="30e6f-131">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30e6f-131">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="30e6f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30e6f-132">NOTES</span></span>

## <span data-ttu-id="30e6f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30e6f-133">RELATED LINKS</span></span>

[<span data-ttu-id="30e6f-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="30e6f-134">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="30e6f-135">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="30e6f-135">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="30e6f-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="30e6f-136">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="30e6f-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="30e6f-137">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)


