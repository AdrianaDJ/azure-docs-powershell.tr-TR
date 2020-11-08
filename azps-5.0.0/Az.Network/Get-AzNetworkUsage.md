---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkUsage.md
ms.openlocfilehash: e02527c0f206607ae778d6447e65a1c93c620b02
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275977"
---
# <span data-ttu-id="cf20c-101">Get-AzNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="cf20c-101">Get-AzNetworkUsage</span></span>

## <span data-ttu-id="cf20c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf20c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf20c-103">Abonelik için ağ kullanımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="cf20c-103">Lists network usages for a subscription</span></span>

## <span data-ttu-id="cf20c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf20c-104">SYNTAX</span></span>

```
Get-AzNetworkUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf20c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf20c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf20c-106">Get-AzNetworkUsage cmdlet 'i ağ kaynaklarının sınırlarını ve geçerli kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="cf20c-106">The Get-AzNetworkUsage cmdlet gets limits and current usage for Network resources.</span></span>

## <span data-ttu-id="cf20c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf20c-107">EXAMPLES</span></span>

### <span data-ttu-id="cf20c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cf20c-108">Example 1</span></span>
```
PS C:\> Get-AzNetworkUsage -Location westcentralus

ResourceType : Virtual Networks
CurrentValue : 6
Limit        : 50

ResourceType : Static Public IP Addresses
CurrentValue : 1
Limit        : 20

ResourceType : Network Security Groups
CurrentValue : 2
Limit        : 100

ResourceType : Public IP Addresses
CurrentValue : 6
Limit        : 60

ResourceType : Network Interfaces
CurrentValue : 1
Limit        : 300

ResourceType : Load Balancers
CurrentValue : 1
Limit        : 100

ResourceType : Application Gateways
CurrentValue : 1
Limit        : 50

ResourceType : Route Tables
CurrentValue : 0
Limit        : 100

ResourceType : Route Filters
CurrentValue : 0
Limit        : 1000

ResourceType : Network Watchers
CurrentValue : 1
Limit        : 1

ResourceType : Packet Captures
CurrentValue : 0
Limit        : 10
```

<span data-ttu-id="cf20c-109">Westcentralus bölgesindeki kaynak kullanım verilerini alır</span><span class="sxs-lookup"><span data-stu-id="cf20c-109">Gets resources usage data in westcentralus region</span></span>

## <span data-ttu-id="cf20c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf20c-110">PARAMETERS</span></span>

### <span data-ttu-id="cf20c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf20c-111">-DefaultProfile</span></span>
<span data-ttu-id="cf20c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf20c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf20c-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="cf20c-113">-Location</span></span>
<span data-ttu-id="cf20c-114">Kaynak kullanımının sorguladığı konum.</span><span class="sxs-lookup"><span data-stu-id="cf20c-114">The location where resource usage is queried.</span></span>

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

### <span data-ttu-id="cf20c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf20c-115">CommonParameters</span></span>
<span data-ttu-id="cf20c-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf20c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf20c-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cf20c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf20c-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf20c-118">INPUTS</span></span>

### <span data-ttu-id="cf20c-119">System. String</span><span class="sxs-lookup"><span data-stu-id="cf20c-119">System.String</span></span>

## <span data-ttu-id="cf20c-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf20c-120">OUTPUTS</span></span>

### <span data-ttu-id="cf20c-121">Microsoft. Azure. Commands. Network. modeller. PSUsage</span><span class="sxs-lookup"><span data-stu-id="cf20c-121">Microsoft.Azure.Commands.Network.Models.PSUsage</span></span>

## <span data-ttu-id="cf20c-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf20c-122">NOTES</span></span>

## <span data-ttu-id="cf20c-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf20c-123">RELATED LINKS</span></span>
