---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935519"
---
# <span data-ttu-id="d83a5-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d83a5-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="d83a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d83a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d83a5-103">Ağ Izleyicisi özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="d83a5-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="d83a5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d83a5-104">SYNTAX</span></span>

### <span data-ttu-id="d83a5-105">Al</span><span class="sxs-lookup"><span data-stu-id="d83a5-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d83a5-106">Listeniz</span><span class="sxs-lookup"><span data-stu-id="d83a5-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d83a5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d83a5-107">DESCRIPTION</span></span>
<span data-ttu-id="d83a5-108">Get-AzNetworkWatcher cmdlet bir veya birden çok Azure ağ Izleyicisi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="d83a5-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="d83a5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d83a5-109">EXAMPLES</span></span>

### <span data-ttu-id="d83a5-110">--------------------------Örnek 1: ağ Izleyicisi--------------------------</span><span class="sxs-lookup"><span data-stu-id="d83a5-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="d83a5-111">NetworkWatcherRG kaynak grubundaki ağ Izleyicisi NetworkWatcher_westcentralus 'Ni alır.</span><span class="sxs-lookup"><span data-stu-id="d83a5-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="d83a5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d83a5-112">PARAMETERS</span></span>

### <span data-ttu-id="d83a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d83a5-113">-DefaultProfile</span></span>
<span data-ttu-id="d83a5-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d83a5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83a5-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d83a5-115">-Name</span></span>
<span data-ttu-id="d83a5-116">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="d83a5-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83a5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d83a5-117">-ResourceGroupName</span></span>
<span data-ttu-id="d83a5-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d83a5-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d83a5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d83a5-119">CommonParameters</span></span>
<span data-ttu-id="d83a5-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d83a5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d83a5-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d83a5-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d83a5-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d83a5-122">INPUTS</span></span>

### <span data-ttu-id="d83a5-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d83a5-123">None</span></span>

## <span data-ttu-id="d83a5-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d83a5-124">OUTPUTS</span></span>

### <span data-ttu-id="d83a5-125">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d83a5-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="d83a5-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d83a5-126">NOTES</span></span>
<span data-ttu-id="d83a5-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="d83a5-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="d83a5-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d83a5-128">RELATED LINKS</span></span>

[<span data-ttu-id="d83a5-129">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="d83a5-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d83a5-130">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d83a5-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d83a5-131">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d83a5-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d83a5-132">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d83a5-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d83a5-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d83a5-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d83a5-134">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d83a5-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d83a5-135">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d83a5-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d83a5-136">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d83a5-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d83a5-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d83a5-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d83a5-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d83a5-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d83a5-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d83a5-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d83a5-140">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d83a5-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
