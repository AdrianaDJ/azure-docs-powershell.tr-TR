---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointfilteritemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject.md
ms.openlocfilehash: c06052ee28d849c5d07a941366efd15cbfeefe25
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108901"
---
# <span data-ttu-id="90b83-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span><span class="sxs-lookup"><span data-stu-id="90b83-101">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject</span></span>

## <span data-ttu-id="90b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90b83-102">SYNOPSIS</span></span>
<span data-ttu-id="90b83-103">Bir bağlantı İzleyicisi uç nokta filtresi öğesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90b83-103">Creates a connection monitor endpoint filter item.</span></span>

## <span data-ttu-id="90b83-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="90b83-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b83-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="90b83-105">DESCRIPTION</span></span>
<span data-ttu-id="90b83-106">New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet 'i Endpoint Filter öğesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="90b83-106">The New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject cmdlet creates endpoint filter item.</span></span>

## <span data-ttu-id="90b83-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="90b83-107">EXAMPLES</span></span>

### <span data-ttu-id="90b83-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="90b83-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "10.0.0.1"
```

<span data-ttu-id="90b83-109">Tür: Bu adres: 10.0.0.1</span><span class="sxs-lookup"><span data-stu-id="90b83-109">Type    : AgentAddress Address : 10.0.0.1</span></span>

## <span data-ttu-id="90b83-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="90b83-110">PARAMETERS</span></span>

### <span data-ttu-id="90b83-111">-Adres</span><span class="sxs-lookup"><span data-stu-id="90b83-111">-Address</span></span>
<span data-ttu-id="90b83-112">Filtre öğesinin adresi.</span><span class="sxs-lookup"><span data-stu-id="90b83-112">The address of the filter item.</span></span>

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

### <span data-ttu-id="90b83-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b83-113">-DefaultProfile</span></span>
<span data-ttu-id="90b83-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="90b83-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90b83-115">-Tür</span><span class="sxs-lookup"><span data-stu-id="90b83-115">-Type</span></span>
<span data-ttu-id="90b83-116">Filtreye dahil edilen öğenin türü.</span><span class="sxs-lookup"><span data-stu-id="90b83-116">The type of item included in the filter.</span></span> <span data-ttu-id="90b83-117">Şu anda yalnızca ' me adresi ' destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="90b83-117">Currently only 'AgentAddress' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90b83-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="90b83-118">-Confirm</span></span>
<span data-ttu-id="90b83-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="90b83-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b83-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b83-120">-WhatIf</span></span>
<span data-ttu-id="90b83-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="90b83-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b83-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="90b83-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b83-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b83-123">CommonParameters</span></span>
<span data-ttu-id="90b83-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="90b83-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b83-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="90b83-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b83-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="90b83-126">INPUTS</span></span>

### <span data-ttu-id="90b83-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="90b83-127">None</span></span>

## <span data-ttu-id="90b83-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="90b83-128">OUTPUTS</span></span>

### <span data-ttu-id="90b83-129">Microsoft. Azure. Commands. Network. model. Psconnectionmonitorendpointfilterıtem</span><span class="sxs-lookup"><span data-stu-id="90b83-129">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorEndpointFilterItem</span></span>

## <span data-ttu-id="90b83-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="90b83-130">NOTES</span></span>

## <span data-ttu-id="90b83-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="90b83-131">RELATED LINKS</span></span>
