---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubRoute.md
ms.openlocfilehash: 7197c90e5d5cb0c8a0e15b5e16d1a3c05aaeebf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592295"
---
# <span data-ttu-id="1769f-101">New-AzureRmVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1769f-101">New-AzureRmVirtualHubRoute</span></span>

## <span data-ttu-id="1769f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1769f-102">SYNOPSIS</span></span>
<span data-ttu-id="1769f-103">Azure sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1769f-103">Creates an Azure Virtual Hub Route object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1769f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1769f-104">SYNTAX</span></span>

```
New-AzureRmVirtualHubRoute -AddressPrefix <String[]> -NextHopIpAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1769f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1769f-105">DESCRIPTION</span></span>
<span data-ttu-id="1769f-106">Azure sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1769f-106">Creates an Azure Virtual Hub Route object.</span></span>

## <span data-ttu-id="1769f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1769f-107">EXAMPLES</span></span>

### <span data-ttu-id="1769f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1769f-108">Example 1</span></span>

```powershell
PS C:\> $route1 = 

AddressPrefixes            NextHopIpAddress
---------------            ----------------
{10.0.0.0/16, 11.0.0.0/16} 12.0.0.5
```

<span data-ttu-id="1769f-109">Yukarıdaki, sanal hub yol tablosuna dahil edilmiş bir sanal hub yol nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1769f-109">The above will create a virtual hub route object that can be included in the virtual hub route table.</span></span>

<span data-ttu-id="1769f-110">Sanal hub rotası, VirtualHubRouteTable nesnesini oluşturmak için kullanılabilecek bir bellek içi nesnedir.</span><span class="sxs-lookup"><span data-stu-id="1769f-110">The virtual hub route is an in-memory object that can be used to create a VirtualHubRouteTable object.</span></span>

## <span data-ttu-id="1769f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1769f-111">PARAMETERS</span></span>

### <span data-ttu-id="1769f-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="1769f-112">-AddressPrefix</span></span>
<span data-ttu-id="1769f-113">Adres önekleri listesi.</span><span class="sxs-lookup"><span data-stu-id="1769f-113">List of Address Prefixes.</span></span>

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

### <span data-ttu-id="1769f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1769f-114">-DefaultProfile</span></span>
<span data-ttu-id="1769f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1769f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1769f-116">-Nexthopıpaddress</span><span class="sxs-lookup"><span data-stu-id="1769f-116">-NextHopIpAddress</span></span>
<span data-ttu-id="1769f-117">Sonraki atlama IP adresi.</span><span class="sxs-lookup"><span data-stu-id="1769f-117">The Next Hop IpAddress.</span></span>

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

### <span data-ttu-id="1769f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1769f-118">CommonParameters</span></span>
<span data-ttu-id="1769f-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1769f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1769f-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1769f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1769f-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1769f-121">INPUTS</span></span>

### <span data-ttu-id="1769f-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1769f-122">None</span></span>

## <span data-ttu-id="1769f-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1769f-123">OUTPUTS</span></span>

### <span data-ttu-id="1769f-124">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="1769f-124">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute</span></span>

## <span data-ttu-id="1769f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1769f-125">NOTES</span></span>

## <span data-ttu-id="1769f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1769f-126">RELATED LINKS</span></span>
