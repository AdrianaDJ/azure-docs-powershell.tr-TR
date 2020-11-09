---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointscopeitemobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject.md
ms.openlocfilehash: c0ca9e257c0686aa0f4589ef4166fec150f41967
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323290"
---
# <span data-ttu-id="7f907-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span><span class="sxs-lookup"><span data-stu-id="7f907-101">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject</span></span>

## <span data-ttu-id="7f907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f907-102">SYNOPSIS</span></span>
<span data-ttu-id="7f907-103">Bağlantı izlemesi uç noktası kapsam öğesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f907-103">Creates a connection monitor endpoint scope item.</span></span>

## <span data-ttu-id="7f907-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f907-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject [-DefaultProfile <IAzureContextContainer>]
 -Address <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f907-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f907-105">DESCRIPTION</span></span>
<span data-ttu-id="7f907-106">New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet 'i uç nokta kapsam öğesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7f907-106">The New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject cmdlet creates endpoint scope item.</span></span>

## <span data-ttu-id="7f907-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f907-107">EXAMPLES</span></span>

### <span data-ttu-id="7f907-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7f907-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "10.0.1.0/24"
```


## <span data-ttu-id="7f907-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f907-109">PARAMETERS</span></span>

### <span data-ttu-id="7f907-110">-Adres</span><span class="sxs-lookup"><span data-stu-id="7f907-110">-Address</span></span>
<span data-ttu-id="7f907-111">Kapsam öğesinin adresi.</span><span class="sxs-lookup"><span data-stu-id="7f907-111">The address of the scope item.</span></span>

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

### <span data-ttu-id="7f907-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f907-112">-DefaultProfile</span></span>
<span data-ttu-id="7f907-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f907-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f907-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f907-114">-Confirm</span></span>
<span data-ttu-id="7f907-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f907-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f907-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f907-116">-WhatIf</span></span>
<span data-ttu-id="7f907-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f907-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f907-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f907-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f907-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f907-119">CommonParameters</span></span>
<span data-ttu-id="7f907-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f907-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f907-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7f907-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f907-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f907-122">INPUTS</span></span>

### <span data-ttu-id="7f907-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7f907-123">None</span></span>

## <span data-ttu-id="7f907-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f907-124">OUTPUTS</span></span>

### <span data-ttu-id="7f907-125">Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherConnectionMonitorEndpointScopeItem</span><span class="sxs-lookup"><span data-stu-id="7f907-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem</span></span>

## <span data-ttu-id="7f907-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f907-126">NOTES</span></span>

## <span data-ttu-id="7f907-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f907-127">RELATED LINKS</span></span>
