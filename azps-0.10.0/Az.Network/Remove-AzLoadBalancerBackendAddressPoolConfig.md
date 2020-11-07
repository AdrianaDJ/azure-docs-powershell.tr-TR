---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F965A9DE-645C-471B-84E8-58D648B1CA57
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 30abb6f2d11eeae9749e7285a91ddeb93a1bf743
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935302"
---
# <span data-ttu-id="4ae0e-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4ae0e-101">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="4ae0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ae0e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae0e-103">Bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-103">Removes a backend address pool configuration from a load balancer.</span></span>

## <span data-ttu-id="4ae0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ae0e-104">SYNTAX</span></span>

```
Remove-AzLoadBalancerBackendAddressPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ae0e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ae0e-106">**Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet 'i, bir yük dengeleyiciden bir arka uç adres havuzunu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-106">The **Remove-AzLoadBalancerBackendAddressPoolConfig** cmdlet removes a backend address pool from a load balancer.</span></span>

## <span data-ttu-id="4ae0e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ae0e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ae0e-108">Örnek 1: bir yük dengeleyiciden bir arka uç adres havuzu yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="4ae0e-108">Example 1: Remove a backend address pool configuration from a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup" | Remove-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="4ae0e-109">Bu komut MyLoadBalancer adlı yük dengeleyiciden alır ve BackendAddressPool02 yapılandırmasını MyLoadBalancer 'dan kaldıran **-AzLoadBalancerBackendAddressPoolConfig** öğesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-109">This command gets the load balancer named MyLoadBalancer and passes it to **Remove-AzLoadBalancerBackendAddressPoolConfig** , which removes the BackendAddressPool02 configuration from MyLoadBalancer.</span></span>
<span data-ttu-id="4ae0e-110">Son olarak, Set-AzLoadBalancer cmdlet MyLoadBalancer öğesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-110">Finally, the Set-AzLoadBalancer cmdlet updates MyLoadBalancer.</span></span>
<span data-ttu-id="4ae0e-111">Arka uç adres havuzu yapılandırmasının silebilmek için mevcut olması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-111">Note that a backend address pool configuration must exist before you can delete it.</span></span>

## <span data-ttu-id="4ae0e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ae0e-112">PARAMETERS</span></span>

### <span data-ttu-id="4ae0e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae0e-113">-DefaultProfile</span></span>
<span data-ttu-id="4ae0e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ae0e-115">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ae0e-115">-LoadBalancer</span></span>
<span data-ttu-id="4ae0e-116">Kaldırılacak arka uç adres havuzunu içeren yük dengeleyicisinin belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-116">Specifies the load balancer that contains the backend address pool to remove.</span></span>

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

### <span data-ttu-id="4ae0e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ae0e-117">-Name</span></span>
<span data-ttu-id="4ae0e-118">Bu cmdlet 'in kaldırıldığı arka uç adres havuzunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-118">Specifies the name of the backend address pool that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4ae0e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae0e-119">CommonParameters</span></span>
<span data-ttu-id="4ae0e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae0e-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae0e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae0e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ae0e-122">INPUTS</span></span>

### <span data-ttu-id="4ae0e-123">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ae0e-123">PSLoadBalancer</span></span>
<span data-ttu-id="4ae0e-124">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="4ae0e-124">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="4ae0e-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ae0e-125">OUTPUTS</span></span>

### <span data-ttu-id="4ae0e-126">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ae0e-126">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="4ae0e-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ae0e-127">NOTES</span></span>

## <span data-ttu-id="4ae0e-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ae0e-128">RELATED LINKS</span></span>

[<span data-ttu-id="4ae0e-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4ae0e-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4ae0e-130">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="4ae0e-130">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="4ae0e-131">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4ae0e-131">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="4ae0e-132">Yeni-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="4ae0e-132">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)


