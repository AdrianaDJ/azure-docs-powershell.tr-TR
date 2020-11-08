---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitoroutputobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorOutputObject.md
ms.openlocfilehash: 9f5c09e87e8d02276352cd10c2a7aba937822af2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096498"
---
# <span data-ttu-id="d2f23-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="d2f23-101">New-AzNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="d2f23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f23-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f23-103">Bağlantı izleme çıkışı hedef nesnesi oluşturma.</span><span class="sxs-lookup"><span data-stu-id="d2f23-103">Create connection monitor output destination object.</span></span>

## <span data-ttu-id="d2f23-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2f23-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorOutputObject [-OutputType <String>] -WorkspaceResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f23-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2f23-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f23-106">New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet 'i Bağlantı İzleyicisi çıkış hedef nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d2f23-106">The New-AzNetworkWatcherConnectionMonitorOutputObject cmdlet creates connection monitor output destination object.</span></span>

## <span data-ttu-id="d2f23-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2f23-107">EXAMPLES</span></span>

### <span data-ttu-id="d2f23-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2f23-108">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitorOutputObject -OutputType "workspace" -ResourcWorkspaceResourceId MyWSResourceId
```

<span data-ttu-id="d2f23-109">"Çalışma alanı" çalışma alanı ayarları: {"WorkspaceResourceId": "Mywsresourceıd"}</span><span class="sxs-lookup"><span data-stu-id="d2f23-109">Type              : "workspace" WorkspaceSettings : { "WorkspaceResourceId": "MyWSResourceId" }</span></span>

## <span data-ttu-id="d2f23-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2f23-110">PARAMETERS</span></span>

### <span data-ttu-id="d2f23-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f23-111">-DefaultProfile</span></span>
<span data-ttu-id="d2f23-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2f23-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f23-113">-OutputType</span><span class="sxs-lookup"><span data-stu-id="d2f23-113">-OutputType</span></span>
<span data-ttu-id="d2f23-114">Bağlantı İzleyicisi çıkış hedefi türü.</span><span class="sxs-lookup"><span data-stu-id="d2f23-114">Connection monitor output destination type.</span></span> <span data-ttu-id="d2f23-115">Şu anda yalnızca \" çalışma alanı \" destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="d2f23-115">Currently, only \"Workspace\" is supported.</span></span>

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

### <span data-ttu-id="d2f23-116">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d2f23-116">-WorkspaceResourceId</span></span>
<span data-ttu-id="d2f23-117">Log Analytics çalışma alanı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d2f23-117">Log analytics workspace resource ID.</span></span>

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

### <span data-ttu-id="d2f23-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2f23-118">-Confirm</span></span>
<span data-ttu-id="d2f23-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2f23-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f23-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f23-120">-WhatIf</span></span>
<span data-ttu-id="d2f23-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2f23-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f23-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2f23-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f23-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f23-123">CommonParameters</span></span>
<span data-ttu-id="d2f23-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2f23-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f23-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d2f23-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f23-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2f23-126">INPUTS</span></span>

### <span data-ttu-id="d2f23-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d2f23-127">None</span></span>

## <span data-ttu-id="d2f23-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2f23-128">OUTPUTS</span></span>

### <span data-ttu-id="d2f23-129">Microsoft. Azure. Commands. Network. modeller. PSNetworkWatcherConnectionMonitorOutputObject</span><span class="sxs-lookup"><span data-stu-id="d2f23-129">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject</span></span>

## <span data-ttu-id="d2f23-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2f23-130">NOTES</span></span>

## <span data-ttu-id="d2f23-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2f23-131">RELATED LINKS</span></span>
