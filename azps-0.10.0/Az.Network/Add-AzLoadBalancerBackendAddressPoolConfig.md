---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9EB11283-0189-4333-8142-DCC3F770F91A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: e97e8f3ed5769e4f81175b29f097aa4946d28881
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935640"
---
# <span data-ttu-id="ae7c5-101">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae7c5-101">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="ae7c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae7c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7c5-103">Bir yük dengeleyicisine arka uç adres havuzu yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-103">Adds a backend address pool configuration to a load balancer.</span></span>

## <span data-ttu-id="ae7c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ae7c5-104">SYNTAX</span></span>

```
Add-AzLoadBalancerBackendAddressPoolConfig -Name <String> -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae7c5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ae7c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ae7c5-106">**Add-Azloadbalancerarka uç** cmdlet 'ı bir Azure yük dengeleyicisine bir arka uç adres havuzu ekler.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-106">The **Add-AzLoadBalancerBackend** cmdlet adds a backend address pool to an Azure load balancer.</span></span>

## <span data-ttu-id="ae7c5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ae7c5-107">EXAMPLES</span></span>

### <span data-ttu-id="ae7c5-108">Örnek 1 yük dengeleyicisine arka uç adres havuzu yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="ae7c5-108">Example 1 Add a backend address pool configuration to a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myrg" | Add-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" | Set-AzLoadBalancer
```

<span data-ttu-id="ae7c5-109">Bu komut MyLoadBalancer adındaki yük dengeleyiciden alır, BackendAddressPool02 adlı arka uç adres havuzunu MyLoadBalancer 'e ekler ve MyLoadBalancer öğesini güncelleştirmek için **set-AzLoadBalancer** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-109">This command gets the load balancer named MyLoadBalancer, adds the backend address pool named BackendAddressPool02 to MyLoadBalancer, and then uses the **Set-AzLoadBalancer** cmdlet to update MyLoadBalancer.</span></span>

## <span data-ttu-id="ae7c5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ae7c5-110">PARAMETERS</span></span>

### <span data-ttu-id="ae7c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae7c5-111">-DefaultProfile</span></span>
<span data-ttu-id="ae7c5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae7c5-113">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae7c5-113">-LoadBalancer</span></span>
<span data-ttu-id="ae7c5-114">**LoadBalancer** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-114">Specifies a **LoadBalancer** object.</span></span>

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

### <span data-ttu-id="ae7c5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ae7c5-115">-Name</span></span>
<span data-ttu-id="ae7c5-116">Eklenecek arka uç adres havuzu yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-116">Specifies the name of the backend address pool configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7c5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7c5-117">CommonParameters</span></span>
<span data-ttu-id="ae7c5-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ae7c5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7c5-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae7c5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7c5-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ae7c5-120">INPUTS</span></span>

### <span data-ttu-id="ae7c5-121">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae7c5-121">PSLoadBalancer</span></span>
<span data-ttu-id="ae7c5-122">' LoadBalancer ' parametresi ardışık düzenin ' PSLoadBalancer ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ae7c5-122">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ae7c5-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ae7c5-123">OUTPUTS</span></span>

### <span data-ttu-id="ae7c5-124">Microsoft. Azure. Commands. Network. model. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae7c5-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="ae7c5-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ae7c5-125">NOTES</span></span>

## <span data-ttu-id="ae7c5-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ae7c5-126">RELATED LINKS</span></span>

[<span data-ttu-id="ae7c5-127">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae7c5-127">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="ae7c5-128">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ae7c5-128">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="ae7c5-129">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae7c5-129">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="ae7c5-130">Yeni-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae7c5-130">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="ae7c5-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae7c5-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


