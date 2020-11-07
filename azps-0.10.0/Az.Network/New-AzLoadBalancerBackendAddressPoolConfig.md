---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 11ac1df9032f86d5265b78efcfc02c08b441cdd3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935398"
---
# <span data-ttu-id="f22d2-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f22d2-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="f22d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f22d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f22d2-103">Bir yük dengeleyici için arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f22d2-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="f22d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f22d2-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f22d2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f22d2-105">DESCRIPTION</span></span>
<span data-ttu-id="f22d2-106">**Yeni-AzLoadBalancerBackendAddressPoolConfig** cmdlet 'ı bir Azure yük dengeleyicisi için arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f22d2-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="f22d2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f22d2-107">EXAMPLES</span></span>

### <span data-ttu-id="f22d2-108">Örnek 1: yük dengeleyici için arka uç adres havuzu yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="f22d2-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="f22d2-109">Bu komut, BackendAddressPool02 adlı bir arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f22d2-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="f22d2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f22d2-110">PARAMETERS</span></span>

### <span data-ttu-id="f22d2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22d2-111">-DefaultProfile</span></span>
<span data-ttu-id="f22d2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f22d2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f22d2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f22d2-113">-Name</span></span>
<span data-ttu-id="f22d2-114">Oluşturulacak adres havuzu yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f22d2-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="f22d2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22d2-115">CommonParameters</span></span>
<span data-ttu-id="f22d2-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f22d2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22d2-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f22d2-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22d2-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f22d2-118">INPUTS</span></span>

## <span data-ttu-id="f22d2-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f22d2-119">OUTPUTS</span></span>

### <span data-ttu-id="f22d2-120">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f22d2-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="f22d2-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f22d2-121">NOTES</span></span>

## <span data-ttu-id="f22d2-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f22d2-122">RELATED LINKS</span></span>

[<span data-ttu-id="f22d2-123">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f22d2-123">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f22d2-124">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f22d2-124">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="f22d2-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="f22d2-125">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


