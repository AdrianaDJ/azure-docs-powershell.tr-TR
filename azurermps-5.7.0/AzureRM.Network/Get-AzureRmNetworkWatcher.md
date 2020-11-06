---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: 9df0d0855ca22e9ea7141a99c69c8b44f16f489d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594930"
---
# <span data-ttu-id="22623-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="22623-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="22623-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22623-102">SYNOPSIS</span></span>
<span data-ttu-id="22623-103">Ağ Izleyicisi özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="22623-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22623-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22623-104">SYNTAX</span></span>

### <span data-ttu-id="22623-105">Al</span><span class="sxs-lookup"><span data-stu-id="22623-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22623-106">Listeniz</span><span class="sxs-lookup"><span data-stu-id="22623-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22623-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="22623-107">DESCRIPTION</span></span>
<span data-ttu-id="22623-108">Get-AzureRmNetworkWatcher cmdlet bir veya birden çok Azure ağ Izleyicisi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="22623-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="22623-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22623-109">EXAMPLES</span></span>

### <span data-ttu-id="22623-110">--------------------------Örnek 1: ağ Izleyicisi--------------------------</span><span class="sxs-lookup"><span data-stu-id="22623-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="22623-111">NetworkWatcherRG kaynak grubundaki ağ Izleyicisi NetworkWatcher_westcentralus 'Ni alır.</span><span class="sxs-lookup"><span data-stu-id="22623-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="22623-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22623-112">PARAMETERS</span></span>

### <span data-ttu-id="22623-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22623-113">-DefaultProfile</span></span>
<span data-ttu-id="22623-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22623-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22623-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="22623-115">-Name</span></span>
<span data-ttu-id="22623-116">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="22623-116">The network watcher name.</span></span>

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

### <span data-ttu-id="22623-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22623-117">-ResourceGroupName</span></span>
<span data-ttu-id="22623-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="22623-118">The resource group name.</span></span>

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

### <span data-ttu-id="22623-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22623-119">CommonParameters</span></span>
<span data-ttu-id="22623-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22623-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22623-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22623-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22623-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22623-122">INPUTS</span></span>

### <span data-ttu-id="22623-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="22623-123">None</span></span>

## <span data-ttu-id="22623-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22623-124">OUTPUTS</span></span>

### <span data-ttu-id="22623-125">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="22623-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="22623-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22623-126">NOTES</span></span>
<span data-ttu-id="22623-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="22623-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="22623-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22623-128">RELATED LINKS</span></span>

[<span data-ttu-id="22623-129">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="22623-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="22623-130">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="22623-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="22623-131">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22623-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22623-132">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="22623-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="22623-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22623-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22623-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22623-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22623-135">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="22623-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="22623-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="22623-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="22623-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="22623-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="22623-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="22623-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="22623-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="22623-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="22623-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="22623-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
