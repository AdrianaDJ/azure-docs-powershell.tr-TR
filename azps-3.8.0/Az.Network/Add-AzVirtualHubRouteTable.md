---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098017"
---
# <span data-ttu-id="48f96-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="48f96-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="48f96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48f96-102">SYNOPSIS</span></span>
<span data-ttu-id="48f96-103">VirtualHub 'ın alt öğesi olan bir sanal hub yol tablosu kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="48f96-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="48f96-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48f96-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48f96-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48f96-105">DESCRIPTION</span></span>
<span data-ttu-id="48f96-106">Sanal hub yol tablosu kaynağı, yolların listesini ve iliştirilebilecek bağlantıların listesini içerir ve sanal bir hub 'da trafiği yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="48f96-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="48f96-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48f96-107">EXAMPLES</span></span>

### <span data-ttu-id="48f96-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="48f96-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="48f96-109">Yukarıdaki komut, geçirilen yollardan bir sanal hub yol tablosu kaynağı oluşturur ve bu nesne sanal bir hub 'da trafiği yönlendirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="48f96-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="48f96-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48f96-110">PARAMETERS</span></span>

### <span data-ttu-id="48f96-111">-Bağlantı</span><span class="sxs-lookup"><span data-stu-id="48f96-111">-Connection</span></span>
<span data-ttu-id="48f96-112">Bu yol tablosunun iliştirildiği bağlantıların listesi.</span><span class="sxs-lookup"><span data-stu-id="48f96-112">List of connections this route table is attached to.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f96-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f96-113">-DefaultProfile</span></span>
<span data-ttu-id="48f96-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48f96-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f96-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="48f96-115">-Name</span></span>
<span data-ttu-id="48f96-116">Yol tablosunun adı.</span><span class="sxs-lookup"><span data-stu-id="48f96-116">Name of the route table.</span></span>

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

### <span data-ttu-id="48f96-117">-Route</span><span class="sxs-lookup"><span data-stu-id="48f96-117">-Route</span></span>
<span data-ttu-id="48f96-118">Sanal hub yollarının listesi.</span><span class="sxs-lookup"><span data-stu-id="48f96-118">List of virtual hub routes.</span></span>

```yaml
Type: PSVirtualHubRoute[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48f96-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f96-119">CommonParameters</span></span>
<span data-ttu-id="48f96-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48f96-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f96-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="48f96-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f96-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48f96-122">INPUTS</span></span>

### <span data-ttu-id="48f96-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="48f96-123">None</span></span>

## <span data-ttu-id="48f96-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48f96-124">OUTPUTS</span></span>

### <span data-ttu-id="48f96-125">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="48f96-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="48f96-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48f96-126">NOTES</span></span>

## <span data-ttu-id="48f96-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48f96-127">RELATED LINKS</span></span>
