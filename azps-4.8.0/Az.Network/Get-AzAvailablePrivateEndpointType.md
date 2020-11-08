---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266074"
---
# <span data-ttu-id="707b9-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="707b9-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="707b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="707b9-102">SYNOPSIS</span></span>
<span data-ttu-id="707b9-103">Konumdaki kullanılabilir özel uç nokta türlerini döndürün.</span><span class="sxs-lookup"><span data-stu-id="707b9-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="707b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="707b9-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="707b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="707b9-105">DESCRIPTION</span></span>
<span data-ttu-id="707b9-106">**Get-AzAvailablePrivateEndpointType** cmdlet 'i, konumdaki kullanılabilir tüm özel uç nokta türlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="707b9-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="707b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="707b9-107">EXAMPLES</span></span>

### <span data-ttu-id="707b9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="707b9-108">Example 1</span></span>
```powershell
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="707b9-109">Bu örnekte, konumdaki kullanılabilir tüm özel uç nokta türleri döndürülür.</span><span class="sxs-lookup"><span data-stu-id="707b9-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="707b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="707b9-110">PARAMETERS</span></span>

### <span data-ttu-id="707b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="707b9-111">-DefaultProfile</span></span>
<span data-ttu-id="707b9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="707b9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="707b9-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="707b9-113">-Location</span></span>
<span data-ttu-id="707b9-114">Konum.</span><span class="sxs-lookup"><span data-stu-id="707b9-114">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707b9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="707b9-115">-ResourceGroupName</span></span>
<span data-ttu-id="707b9-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="707b9-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="707b9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="707b9-117">CommonParameters</span></span>
<span data-ttu-id="707b9-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="707b9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="707b9-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="707b9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="707b9-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="707b9-120">INPUTS</span></span>

### <span data-ttu-id="707b9-121">System. String</span><span class="sxs-lookup"><span data-stu-id="707b9-121">System.String</span></span>

## <span data-ttu-id="707b9-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="707b9-122">OUTPUTS</span></span>

### <span data-ttu-id="707b9-123">Microsoft. Azure. Commands. Network. model. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="707b9-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="707b9-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="707b9-124">NOTES</span></span>

## <span data-ttu-id="707b9-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="707b9-125">RELATED LINKS</span></span>
