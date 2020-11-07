---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935507"
---
# <span data-ttu-id="a3aea-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a3aea-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="a3aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3aea-102">SYNOPSIS</span></span>
<span data-ttu-id="a3aea-103">Bir kaynaktaki akış günlüğünün durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a3aea-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="a3aea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3aea-104">SYNTAX</span></span>

### <span data-ttu-id="a3aea-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a3aea-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3aea-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a3aea-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3aea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3aea-107">DESCRIPTION</span></span>
<span data-ttu-id="a3aea-108">Get-AzNetworkWatcherFlowLogStatus cmdlet 'i bir kaynaktaki akış günlüğünün durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="a3aea-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="a3aea-109">Bu durum, sağlanan kaynak için akış günlüğünün etkinleştirilip etkinleştirilmeyeceğini, günlükleri gönderecek yapılandırılmış depolama hesabının ve günlüklerin bekletme ilkesinin etkinleştirilip etkinleştirilmediğini içerir.</span><span class="sxs-lookup"><span data-stu-id="a3aea-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="a3aea-110">Ağ güvenlik grupları akış günlüğü için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="a3aea-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="a3aea-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3aea-111">EXAMPLES</span></span>

### <span data-ttu-id="a3aea-112">---Örnek 1: belirli bir NSG için akış günlüğü durumunu alma---</span><span class="sxs-lookup"><span data-stu-id="a3aea-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="a3aea-113">Bu örnekte, bir ağ güvenlik grubunun akış günlüğü durumu.</span><span class="sxs-lookup"><span data-stu-id="a3aea-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="a3aea-114">Belirtilen NSG 'de akış günlüğü etkinleştirilmiş ve bekletme ilkesi ayarlanmamış.</span><span class="sxs-lookup"><span data-stu-id="a3aea-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="a3aea-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3aea-115">PARAMETERS</span></span>

### <span data-ttu-id="a3aea-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="a3aea-116">-AsJob</span></span>
<span data-ttu-id="a3aea-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a3aea-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3aea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3aea-118">-DefaultProfile</span></span>
<span data-ttu-id="a3aea-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3aea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3aea-120">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="a3aea-120">-NetworkWatcher</span></span>
<span data-ttu-id="a3aea-121">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="a3aea-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="a3aea-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a3aea-122">-NetworkWatcherName</span></span>
<span data-ttu-id="a3aea-123">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="a3aea-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="a3aea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3aea-124">-ResourceGroupName</span></span>
<span data-ttu-id="a3aea-125">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a3aea-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a3aea-126">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="a3aea-126">-TargetResourceId</span></span>
<span data-ttu-id="a3aea-127">Hedef kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a3aea-127">The target resource ID.</span></span>

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

### <span data-ttu-id="a3aea-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3aea-128">CommonParameters</span></span>
<span data-ttu-id="a3aea-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3aea-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3aea-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3aea-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3aea-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3aea-131">INPUTS</span></span>

### <span data-ttu-id="a3aea-132">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="a3aea-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a3aea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a3aea-133">System.String</span></span>

## <span data-ttu-id="a3aea-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3aea-134">OUTPUTS</span></span>

### <span data-ttu-id="a3aea-135">Microsoft. Azure. Commands. Network. modeller. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="a3aea-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="a3aea-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3aea-136">NOTES</span></span>
<span data-ttu-id="a3aea-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, akış, Günlükler, akışgünlüğü, günlüğe kaydetme</span><span class="sxs-lookup"><span data-stu-id="a3aea-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="a3aea-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3aea-138">RELATED LINKS</span></span>

[<span data-ttu-id="a3aea-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a3aea-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a3aea-140">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="a3aea-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a3aea-141">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="a3aea-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a3aea-142">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="a3aea-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a3aea-143">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3aea-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a3aea-144">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a3aea-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a3aea-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3aea-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a3aea-146">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3aea-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a3aea-147">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3aea-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a3aea-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a3aea-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a3aea-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a3aea-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a3aea-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a3aea-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a3aea-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a3aea-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a3aea-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a3aea-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a3aea-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a3aea-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
