---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 0cc210563046a0ff8ee0554eb479e5eb822157fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764351"
---
# <span data-ttu-id="3a0e3-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3a0e3-101">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="3a0e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="3a0e3-103">Bir yük dengeleyicisine arka uç adres havuzu yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-103">Adds a backend address pool configuration to a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a0e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a0e3-104">SYNTAX</span></span>

```
Add-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a0e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="3a0e3-106">**Add-Azurermloadbalancerarka uç** cmdlet 'ı bir Azure yük dengeleyicisine bir arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-106">The **Add-AzureRmLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="3a0e3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a0e3-107">EXAMPLES</span></span>

### <span data-ttu-id="3a0e3-108">Örnek 1 yük dengeleyicisine arka uç adres havuzu yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="3a0e3-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="3a0e3-109">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır, BackendAddressPool02 adlı arka uç adres havuzunu MyLoadBalancer 'e ekler ve MyLoadBalancer öğesini güncelleştirmek için **set-AzureRmLoadBalancer** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzureRmLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="3a0e3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a0e3-110">PARAMETERS</span></span>

### <span data-ttu-id="3a0e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a0e3-111">-DefaultProfile</span></span>
<span data-ttu-id="3a0e3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a0e3-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3a0e3-113">-LoadBalancer</span></span>
<span data-ttu-id="3a0e3-114">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="3a0e3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a0e3-115">-Name</span></span>
<span data-ttu-id="3a0e3-116">Eklenecek arka uç adres havuzu yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-116">Specifies the name of the backend address pool configuration to add.</span></span>

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

### <span data-ttu-id="3a0e3-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a0e3-117">-Confirm</span></span>
<span data-ttu-id="3a0e3-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a0e3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a0e3-119">-WhatIf</span></span>
<span data-ttu-id="3a0e3-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a0e3-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a0e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a0e3-122">CommonParameters</span></span>
<span data-ttu-id="3a0e3-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a0e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a0e3-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a0e3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a0e3-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a0e3-125">INPUTS</span></span>

### <span data-ttu-id="3a0e3-126">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3a0e3-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="3a0e3-127">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3a0e3-127">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="3a0e3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a0e3-128">OUTPUTS</span></span>

### <span data-ttu-id="3a0e3-129">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3a0e3-129">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="3a0e3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a0e3-130">NOTES</span></span>

## <span data-ttu-id="3a0e3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a0e3-131">RELATED LINKS</span></span>

[<span data-ttu-id="3a0e3-132">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3a0e3-132">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="3a0e3-133">Get-Azurermnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="3a0e3-133">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="3a0e3-134">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3a0e3-134">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3a0e3-135">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3a0e3-135">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="3a0e3-136">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="3a0e3-136">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


