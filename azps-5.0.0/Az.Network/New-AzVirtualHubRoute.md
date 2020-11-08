---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: baf349f56d3ebbf55c21d99dbfefd64ad7b295a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278531"
---
# <span data-ttu-id="d3d3f-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d3d3f-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="d3d3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3d3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d3f-103">Azure sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="d3d3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3d3f-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3d3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3d3f-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d3f-106">Azure sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="d3d3f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3d3f-107">EXAMPLES</span></span>

### <span data-ttu-id="d3d3f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3d3f-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="d3d3f-109">Yukarıdaki, sanal hub yol tablosuna dahil edilmiş bir sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="d3d3f-110">Sanal hub rotası, VirtualHubRouteTable nesnesini oluşturmak için kullanılabilecek bir bellek içi nesnedir.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="d3d3f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3d3f-111">PARAMETERS</span></span>

### <span data-ttu-id="d3d3f-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="d3d3f-112">-AddressPrefix</span></span>
<span data-ttu-id="d3d3f-113">Adres önekleri listesi.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-113">List of Address Prefixes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d3f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d3f-114">-DefaultProfile</span></span>
<span data-ttu-id="d3d3f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3d3f-116">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="d3d3f-116">-NextHopIpAddress</span></span>
<span data-ttu-id="d3d3f-117">Sonraki atlama IP adresi.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="d3d3f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d3f-118">CommonParameters</span></span>
<span data-ttu-id="d3d3f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3d3f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d3f-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3d3f-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d3f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3d3f-121">INPUTS</span></span>

### <span data-ttu-id="d3d3f-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d3d3f-122">None</span></span>

## <span data-ttu-id="d3d3f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3d3f-123">OUTPUTS</span></span>

### <span data-ttu-id="d3d3f-124">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="d3d3f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="d3d3f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3d3f-125">NOTES</span></span>

## <span data-ttu-id="d3d3f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3d3f-126">RELATED LINKS</span></span>

[<span data-ttu-id="d3d3f-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="d3d3f-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
