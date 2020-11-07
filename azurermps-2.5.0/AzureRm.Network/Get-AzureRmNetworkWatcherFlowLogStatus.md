---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherflowlogstatus
schema: 2.0.0
ms.openlocfilehash: 96d3bea781b0c595b54387a9b07b085f173d7b0a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939113"
---
# <span data-ttu-id="4ddc0-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4ddc0-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="4ddc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ddc0-102">SYNOPSIS</span></span>
<span data-ttu-id="4ddc0-103">Bir kaynaktaki akış günlüğünün durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ddc0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ddc0-104">SYNTAX</span></span>

### <span data-ttu-id="4ddc0-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4ddc0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ddc0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4ddc0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ddc0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ddc0-107">DESCRIPTION</span></span>
<span data-ttu-id="4ddc0-108">Get-AzureRmNetworkWatcherFlowLogStatus cmdlet 'i bir kaynaktaki akış günlüğünün durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="4ddc0-109">Bu durum, sağlanan kaynak için akış günlüğünün etkinleştirilip etkinleştirilmeyeceğini, günlükleri gönderecek yapılandırılmış depolama hesabının ve günlüklerin bekletme ilkesinin etkinleştirilip etkinleştirilmediğini içerir.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="4ddc0-110">Ağ güvenlik grupları akış günlüğü için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="4ddc0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ddc0-111">EXAMPLES</span></span>

### <span data-ttu-id="4ddc0-112">---Örnek 1: belirli bir NSG için akış günlüğü durumunu alma---</span><span class="sxs-lookup"><span data-stu-id="4ddc0-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="4ddc0-113">Bu örnekte, bir ağ güvenlik grubunun akış günlüğü durumu.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="4ddc0-114">Belirtilen NSG 'de akış günlüğü etkinleştirilmiş ve bekletme ilkesi ayarlanmamış.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="4ddc0-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ddc0-115">PARAMETERS</span></span>

### <span data-ttu-id="4ddc0-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="4ddc0-116">-AsJob</span></span>
<span data-ttu-id="4ddc0-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4ddc0-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ddc0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ddc0-118">-DefaultProfile</span></span>
<span data-ttu-id="4ddc0-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ddc0-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4ddc0-120">-NetworkWatcher</span></span>
<span data-ttu-id="4ddc0-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-121">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ddc0-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4ddc0-122">-NetworkWatcherName</span></span>
<span data-ttu-id="4ddc0-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-123">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ddc0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ddc0-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ddc0-125">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-125">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ddc0-126">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="4ddc0-126">-TargetResourceId</span></span>
<span data-ttu-id="4ddc0-127">Hedef kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-127">The target resource ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ddc0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ddc0-128">CommonParameters</span></span>
<span data-ttu-id="4ddc0-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ddc0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ddc0-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ddc0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ddc0-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ddc0-131">INPUTS</span></span>

### <span data-ttu-id="4ddc0-132">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4ddc0-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4ddc0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4ddc0-133">System.String</span></span>

## <span data-ttu-id="4ddc0-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ddc0-134">OUTPUTS</span></span>

### <span data-ttu-id="4ddc0-135">Microsoft. Azure. Commands. Network. modeller. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="4ddc0-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="4ddc0-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ddc0-136">NOTES</span></span>
<span data-ttu-id="4ddc0-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, akış, Günlükler, akışgünlüğü, günlüğe kaydetme</span><span class="sxs-lookup"><span data-stu-id="4ddc0-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="4ddc0-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ddc0-138">RELATED LINKS</span></span>

[<span data-ttu-id="4ddc0-139">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4ddc0-139">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="4ddc0-140">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4ddc0-140">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4ddc0-141">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4ddc0-141">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4ddc0-142">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4ddc0-142">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4ddc0-143">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ddc0-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ddc0-144">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4ddc0-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4ddc0-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ddc0-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ddc0-146">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ddc0-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ddc0-147">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4ddc0-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4ddc0-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4ddc0-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4ddc0-149">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4ddc0-149">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4ddc0-150">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4ddc0-150">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4ddc0-151">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4ddc0-151">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4ddc0-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4ddc0-152">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4ddc0-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4ddc0-153">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
