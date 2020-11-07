---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubRoute.md
ms.openlocfilehash: 8a9184eddaf5b614b4338a95e1d895d645e0832e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918188"
---
# <span data-ttu-id="7f7ba-101">New-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7f7ba-101">New-AzVirtualHubRoute</span></span>

## <span data-ttu-id="7f7ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f7ba-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7ba-103">Azure sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f7ba-103">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="7f7ba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f7ba-104">SYNTAX</span></span>

```
New-AzVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f7ba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f7ba-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7ba-106">Azure sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f7ba-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="7f7ba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f7ba-107">EXAMPLES</span></span>

### <span data-ttu-id="7f7ba-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f7ba-108">Example 1</span></span>

```powershell
PS C:\> $route1 = New-AzVirtualHubRoute -AddressPrefix @("10.0.0.0/16", "11.0.0.0/16") -NextHopIpAddress "12.0.0.5"

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="7f7ba-109">Yukarıdaki, sanal hub yol tablosuna dahil edilmiş bir sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f7ba-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="7f7ba-110">Sanal hub rotası, VirtualHubRouteTable nesnesini oluşturmak için kullanılabilecek bir bellek içi nesnedir.</span><span class="sxs-lookup"><span data-stu-id="7f7ba-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="7f7ba-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f7ba-111">PARAMETERS</span></span>

### <span data-ttu-id="7f7ba-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="7f7ba-112">-AddressPrefix</span></span>
<span data-ttu-id="7f7ba-113">Adres önekleri listesi.</span><span class="sxs-lookup"><span data-stu-id="7f7ba-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="7f7ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7ba-114">-DefaultProfile</span></span>
<span data-ttu-id="7f7ba-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f7ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f7ba-116">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="7f7ba-116">-NextHopIpAddress</span></span>
<span data-ttu-id="7f7ba-117">Sonraki atlama IP adresi.</span><span class="sxs-lookup"><span data-stu-id="7f7ba-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="7f7ba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7ba-118">CommonParameters</span></span>
<span data-ttu-id="7f7ba-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f7ba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7ba-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f7ba-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7ba-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f7ba-121">INPUTS</span></span>

### <span data-ttu-id="7f7ba-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7f7ba-122">None</span></span>

## <span data-ttu-id="7f7ba-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f7ba-123">OUTPUTS</span></span>

### <span data-ttu-id="7f7ba-124">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7f7ba-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="7f7ba-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f7ba-125">NOTES</span></span>

## <span data-ttu-id="7f7ba-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f7ba-126">RELATED LINKS</span></span>

[<span data-ttu-id="7f7ba-127">New-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7f7ba-127">New-AzVirtualHubRouteTable</span></span>](./New-AzVirtualHubRouteTable.md)
