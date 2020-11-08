---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097282"
---
# <span data-ttu-id="aab8a-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="aab8a-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="aab8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aab8a-102">SYNOPSIS</span></span>
<span data-ttu-id="aab8a-103">Bir yük dengeleyici için arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aab8a-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="aab8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aab8a-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aab8a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aab8a-105">DESCRIPTION</span></span>
<span data-ttu-id="aab8a-106">**Yeni-AzLoadBalancerBackendAddressPoolConfig** cmdlet 'ı bir Azure yük dengeleyicisi için arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aab8a-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="aab8a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aab8a-107">EXAMPLES</span></span>

### <span data-ttu-id="aab8a-108">Örnek 1: yük dengeleyici için arka uç adres havuzu yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="aab8a-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="aab8a-109">Bu komut, BackendAddressPool02 adlı bir arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aab8a-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="aab8a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aab8a-110">PARAMETERS</span></span>

### <span data-ttu-id="aab8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aab8a-111">-DefaultProfile</span></span>
<span data-ttu-id="aab8a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aab8a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aab8a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="aab8a-113">-Name</span></span>
<span data-ttu-id="aab8a-114">Oluşturulacak adres havuzu yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aab8a-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="aab8a-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="aab8a-115">-Confirm</span></span>
<span data-ttu-id="aab8a-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aab8a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aab8a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aab8a-117">-WhatIf</span></span>
<span data-ttu-id="aab8a-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aab8a-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aab8a-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aab8a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aab8a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aab8a-120">CommonParameters</span></span>
<span data-ttu-id="aab8a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aab8a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aab8a-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aab8a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aab8a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aab8a-123">INPUTS</span></span>

### <span data-ttu-id="aab8a-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="aab8a-124">None</span></span>

## <span data-ttu-id="aab8a-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aab8a-125">OUTPUTS</span></span>

### <span data-ttu-id="aab8a-126">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="aab8a-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="aab8a-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aab8a-127">NOTES</span></span>

## <span data-ttu-id="aab8a-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aab8a-128">RELATED LINKS</span></span>

[<span data-ttu-id="aab8a-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="aab8a-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="aab8a-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="aab8a-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="aab8a-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="aab8a-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


