---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 97227c27e23c6283fd64e1660262bbec175cf0a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940072"
---
# <span data-ttu-id="ca395-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ca395-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="ca395-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca395-102">SYNOPSIS</span></span>
<span data-ttu-id="ca395-103">Ağ Izleyicisi özelliklerini alır</span><span class="sxs-lookup"><span data-stu-id="ca395-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca395-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca395-104">SYNTAX</span></span>

### <span data-ttu-id="ca395-105">Al</span><span class="sxs-lookup"><span data-stu-id="ca395-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ca395-106">Listeniz</span><span class="sxs-lookup"><span data-stu-id="ca395-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca395-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca395-107">DESCRIPTION</span></span>
<span data-ttu-id="ca395-108">Get-AzureRmNetworkWatcher cmdlet bir veya birden çok Azure ağ Izleyicisi kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="ca395-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="ca395-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca395-109">EXAMPLES</span></span>

### <span data-ttu-id="ca395-110">--------------------------Örnek 1: ağ Izleyicisi--------------------------</span><span class="sxs-lookup"><span data-stu-id="ca395-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="ca395-111">NetworkWatcherRG kaynak grubundaki ağ Izleyicisi NetworkWatcher_westcentralus 'Ni alır.</span><span class="sxs-lookup"><span data-stu-id="ca395-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="ca395-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca395-112">PARAMETERS</span></span>

### <span data-ttu-id="ca395-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca395-113">-DefaultProfile</span></span>
<span data-ttu-id="ca395-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca395-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca395-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca395-115">-Name</span></span>
<span data-ttu-id="ca395-116">Ağ İzleyici adı.</span><span class="sxs-lookup"><span data-stu-id="ca395-116">The network watcher name.</span></span>

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

### <span data-ttu-id="ca395-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca395-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca395-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ca395-118">The resource group name.</span></span>

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

### <span data-ttu-id="ca395-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca395-119">CommonParameters</span></span>
<span data-ttu-id="ca395-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca395-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca395-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca395-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca395-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca395-122">INPUTS</span></span>

### <span data-ttu-id="ca395-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ca395-123">None</span></span>

## <span data-ttu-id="ca395-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca395-124">OUTPUTS</span></span>

### <span data-ttu-id="ca395-125">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ca395-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="ca395-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca395-126">NOTES</span></span>
<span data-ttu-id="ca395-127">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="ca395-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="ca395-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca395-128">RELATED LINKS</span></span>

[<span data-ttu-id="ca395-129">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ca395-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ca395-130">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ca395-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ca395-131">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ca395-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ca395-132">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ca395-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ca395-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ca395-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ca395-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ca395-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ca395-135">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ca395-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ca395-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ca395-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ca395-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ca395-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ca395-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ca395-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ca395-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ca395-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ca395-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ca395-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
