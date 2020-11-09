---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualHubRouteTable.md
ms.openlocfilehash: a5b846ebd78c35e1aee35b4b477407877c485cfa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325909"
---
# <span data-ttu-id="9c925-101">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="9c925-101">Add-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="9c925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c925-102">SYNOPSIS</span></span>
<span data-ttu-id="9c925-103">VirtualHub 'ın alt öğesi olan bir sanal hub yol tablosu kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c925-103">Creates a Virtual Hub Route Table resource which is a child of VirtualHub.</span></span>

## <span data-ttu-id="9c925-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c925-104">SYNTAX</span></span>

```
Add-AzVirtualHubRouteTable -Name <String> -Route <PSVirtualHubRoute[]> -Connection <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c925-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c925-105">DESCRIPTION</span></span>
<span data-ttu-id="9c925-106">Sanal hub yol tablosu kaynağı, yolların listesini ve iliştirilebilecek bağlantıların listesini içerir ve sanal bir hub 'da trafiği yönlendirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="9c925-106">The virtual hub route table resource contains the list of routes and a list of connections to which it can be attached to and is used to route traffic in a Virtual Hub.</span></span>

## <span data-ttu-id="9c925-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c925-107">EXAMPLES</span></span>

### <span data-ttu-id="9c925-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c925-108">Example 1</span></span>
```powershell
PS C:\> $route1�=�Add-AzVirtualHubRoute�-DestinationType�"CIDR"�-Destination�@("10.4.0.0/16",�"10.5.0.0/16")�-NextHopType�"IPAddress"�-NextHop�@("10.0.0.68")
PS C:\> Add-AzVirtualHubRouteTable�-Route�@($route1)�-Connection�@("All_Vnets")�-Name�"routeTable1"

Name                : routeTable1
Id                  :
Routes              : {Microsoft.Azure.Commands.Network.Models.PSVirtualHubRoute}
Connections : {All_Vnets}
ProvisioningState   :
```

<span data-ttu-id="9c925-109">Yukarıdaki komut, geçirilen yollardan bir sanal hub yol tablosu kaynağı oluşturur ve bu nesne sanal bir hub 'da trafiği yönlendirmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9c925-109">The above command will create a Virtual Hub Route Table resource from the routes passed to it and this object can be used for routing traffic in a Virtual Hub.</span></span>  

## <span data-ttu-id="9c925-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c925-110">PARAMETERS</span></span>

### <span data-ttu-id="9c925-111">-Bağlantı</span><span class="sxs-lookup"><span data-stu-id="9c925-111">-Connection</span></span>
<span data-ttu-id="9c925-112">Bu yol tablosunun iliştirildiği bağlantıların listesi.</span><span class="sxs-lookup"><span data-stu-id="9c925-112">List of connections this route table is attached to.</span></span>

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

### <span data-ttu-id="9c925-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c925-113">-DefaultProfile</span></span>
<span data-ttu-id="9c925-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c925-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c925-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c925-115">-Name</span></span>
<span data-ttu-id="9c925-116">Yol tablosunun adı.</span><span class="sxs-lookup"><span data-stu-id="9c925-116">Name of the route table.</span></span>

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

### <span data-ttu-id="9c925-117">-Route</span><span class="sxs-lookup"><span data-stu-id="9c925-117">-Route</span></span>
<span data-ttu-id="9c925-118">Sanal hub yollarının listesi.</span><span class="sxs-lookup"><span data-stu-id="9c925-118">List of virtual hub routes.</span></span>

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

### <span data-ttu-id="9c925-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c925-119">CommonParameters</span></span>
<span data-ttu-id="9c925-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c925-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c925-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9c925-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c925-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c925-122">INPUTS</span></span>

### <span data-ttu-id="9c925-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9c925-123">None</span></span>

## <span data-ttu-id="9c925-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c925-124">OUTPUTS</span></span>

### <span data-ttu-id="9c925-125">Microsoft. Azure. Commands. Network. modeller. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="9c925-125">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

## <span data-ttu-id="9c925-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c925-126">NOTES</span></span>

## <span data-ttu-id="9c925-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c925-127">RELATED LINKS</span></span>
