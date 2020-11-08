---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 9bbfa0aec2da00ada25fc4bb8a5334f67e80e41a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940047"
---
# <span data-ttu-id="c9627-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c9627-101">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="c9627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9627-102">SYNOPSIS</span></span>
<span data-ttu-id="c9627-103">Bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9627-103">Removes a backend address pool configuration from a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9627-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9627-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9627-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9627-105">DESCRIPTION</span></span>
<span data-ttu-id="c9627-106">**Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet 'i, bir yük dengeleyiciden bir arka uç adres havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9627-106">The **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="c9627-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9627-107">EXAMPLES</span></span>

### <span data-ttu-id="c9627-108">Örnek 1: bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c9627-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzureRmLoadBalancer
```

<span data-ttu-id="c9627-109">Bu komut MyLoadBalancer adlı yük dengeleyiciden alır ve bunu **kaldırmak** Için myloadbalancer 'dan BackendAddressPool02 yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9627-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzureRmLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="c9627-110">Son olarak, Set-AzureRmLoadBalancer cmdlet MyLoadBalancer öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9627-110">Finally, the Set-AzureRmLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="c9627-111">Arka uç adres havuzu yapılandırmasının silebilmek için mevcut olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="c9627-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="c9627-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9627-112">PARAMETERS</span></span>

### <span data-ttu-id="c9627-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9627-113">-DefaultProfile</span></span>
<span data-ttu-id="c9627-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9627-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9627-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9627-115">-LoadBalancer</span></span>
<span data-ttu-id="c9627-116">Kaldırılacak arka uç adres havuzunu içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9627-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="c9627-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9627-117">-Name</span></span>
<span data-ttu-id="c9627-118">Bu cmdlet 'in kaldırıldığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9627-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c9627-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9627-119">CommonParameters</span></span>
<span data-ttu-id="c9627-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9627-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9627-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9627-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9627-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9627-122">INPUTS</span></span>

### <span data-ttu-id="c9627-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9627-123">PSLoadBalancer</span></span>
<span data-ttu-id="c9627-124">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="c9627-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="c9627-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9627-125">OUTPUTS</span></span>

### <span data-ttu-id="c9627-126">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9627-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c9627-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9627-127">NOTES</span></span>

## <span data-ttu-id="c9627-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9627-128">RELATED LINKS</span></span>

[<span data-ttu-id="c9627-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c9627-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c9627-130">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c9627-130">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c9627-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c9627-131">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c9627-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c9627-132">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzureRmLoadBalancerBackendAddressPoolConfig.md)

