---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
ms.openlocfilehash: 367e5d74b9d2c1d29199a7af3c132e147b5ae620
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939289"
---
# <span data-ttu-id="129f1-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="129f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="129f1-102">SYNOPSIS</span></span>
<span data-ttu-id="129f1-103">Bir yük dengeleyici için arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="129f1-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="129f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="129f1-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="129f1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="129f1-105">DESCRIPTION</span></span>
<span data-ttu-id="129f1-106">**Yeni-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet 'i Azure Yük Dengeleyici için bir arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="129f1-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="129f1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="129f1-107">EXAMPLES</span></span>

### <span data-ttu-id="129f1-108">Örnek 1: yük dengeleyici için arka uç adres havuzu yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="129f1-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="129f1-109">Bu komut, BackendAddressPool02 adlı bir arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="129f1-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="129f1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="129f1-110">PARAMETERS</span></span>

### <span data-ttu-id="129f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="129f1-111">-DefaultProfile</span></span>
<span data-ttu-id="129f1-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="129f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="129f1-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="129f1-113">-Name</span></span>
<span data-ttu-id="129f1-114">Oluşturulacak adres havuzu yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="129f1-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="129f1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="129f1-115">CommonParameters</span></span>
<span data-ttu-id="129f1-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="129f1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="129f1-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="129f1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="129f1-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="129f1-118">INPUTS</span></span>

## <span data-ttu-id="129f1-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="129f1-119">OUTPUTS</span></span>

### <span data-ttu-id="129f1-120">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="129f1-120">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="129f1-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="129f1-121">NOTES</span></span>

## <span data-ttu-id="129f1-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="129f1-122">RELATED LINKS</span></span>

[<span data-ttu-id="129f1-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-123">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="129f1-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-124">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="129f1-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="129f1-125">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


