---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2a9fca5faf7ba024a5d5c891aa1c74ba002ac053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590173"
---
# <span data-ttu-id="792eb-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="792eb-101">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="792eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="792eb-102">SYNOPSIS</span></span>
<span data-ttu-id="792eb-103">Bir yük dengeleyicinin arka uç adres havuzu yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="792eb-103">Gets a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="792eb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="792eb-104">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="792eb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="792eb-105">DESCRIPTION</span></span>
<span data-ttu-id="792eb-106">**Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet 'i, tek bir arka uç adres havuzunu veya bir yük dengeleyicinin arka uç adresi havuzlarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="792eb-106">The **Get-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="792eb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="792eb-107">EXAMPLES</span></span>

### <span data-ttu-id="792eb-108">Örnek 1: arka uç adres havuzunu alma</span><span class="sxs-lookup"><span data-stu-id="792eb-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="792eb-109">İlk komut MyResourceGroup adlı kaynak grubunda MyLoadBalancer adlı mevcut bir yük dengeleyicisi alır ve $loadbalancer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="792eb-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="792eb-110">İkinci komut $loadbalancer 'teki yük dengeleyicinin BackendAddressPool02 adlı ilişkili arka uç adres havuzu yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="792eb-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="792eb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="792eb-111">PARAMETERS</span></span>

### <span data-ttu-id="792eb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="792eb-112">-DefaultProfile</span></span>
<span data-ttu-id="792eb-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="792eb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="792eb-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="792eb-114">-LoadBalancer</span></span>
<span data-ttu-id="792eb-115">Alınacak arka uç adres havuzuyla ilişkili yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="792eb-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="792eb-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="792eb-116">-Name</span></span>
<span data-ttu-id="792eb-117">Alınacak arka uç adres havuzunu içeren yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="792eb-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="792eb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="792eb-118">CommonParameters</span></span>
<span data-ttu-id="792eb-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="792eb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="792eb-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="792eb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="792eb-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="792eb-121">INPUTS</span></span>

### <span data-ttu-id="792eb-122">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="792eb-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="792eb-123">Parametreler: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="792eb-123">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="792eb-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="792eb-124">OUTPUTS</span></span>

### <span data-ttu-id="792eb-125">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="792eb-125">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="792eb-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="792eb-126">NOTES</span></span>

## <span data-ttu-id="792eb-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="792eb-127">RELATED LINKS</span></span>

[<span data-ttu-id="792eb-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="792eb-128">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="792eb-129">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="792eb-129">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="792eb-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="792eb-130">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="792eb-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="792eb-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


