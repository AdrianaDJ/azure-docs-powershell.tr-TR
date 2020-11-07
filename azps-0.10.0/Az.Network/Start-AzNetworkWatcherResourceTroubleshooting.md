---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: a72f494518b3a511eac3e4b1a92330f666bbca64
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936486"
---
# <span data-ttu-id="1a87f-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1a87f-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="1a87f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a87f-102">SYNOPSIS</span></span>
<span data-ttu-id="1a87f-103">Azure 'daki bir ağ kaynağında sorun gidermeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="1a87f-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="1a87f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1a87f-104">SYNTAX</span></span>

### <span data-ttu-id="1a87f-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1a87f-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a87f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1a87f-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a87f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1a87f-107">DESCRIPTION</span></span>
<span data-ttu-id="1a87f-108">Start-AzNetworkWatcherResourceTroubleshooting cmdlet 'i Azure 'daki bir ağ kaynağında sorun gidermeyi başlatır ve olası sorunlar ve Azaltıcı Etkenler hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="1a87f-108">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="1a87f-109">Şu anda sanal ağ geçitleri ve bağlantılar desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1a87f-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="1a87f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1a87f-110">EXAMPLES</span></span>

### <span data-ttu-id="1a87f-111">---Örnek 1: sanal ağ geçidinde sorun giderme---</span><span class="sxs-lookup"><span data-stu-id="1a87f-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="1a87f-112">Yukarıdaki örnek sanal ağ geçidinde sorun gidermeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="1a87f-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="1a87f-113">İşlemin tamamlanması birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="1a87f-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="1a87f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1a87f-114">PARAMETERS</span></span>

### <span data-ttu-id="1a87f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a87f-115">-DefaultProfile</span></span>
<span data-ttu-id="1a87f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1a87f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a87f-117">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1a87f-117">-NetworkWatcher</span></span>
<span data-ttu-id="1a87f-118">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="1a87f-118">The network watcher resource.</span></span>

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

### <span data-ttu-id="1a87f-119">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1a87f-119">-NetworkWatcherName</span></span>
<span data-ttu-id="1a87f-120">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="1a87f-120">The name of network watcher.</span></span>

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

### <span data-ttu-id="1a87f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a87f-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a87f-122">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1a87f-122">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1a87f-123">-Storageıd</span><span class="sxs-lookup"><span data-stu-id="1a87f-123">-StorageId</span></span>
<span data-ttu-id="1a87f-124">Depolama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1a87f-124">The storage ID.</span></span>

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

### <span data-ttu-id="1a87f-125">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="1a87f-125">-StoragePath</span></span>
<span data-ttu-id="1a87f-126">Depolama yolu.</span><span class="sxs-lookup"><span data-stu-id="1a87f-126">The storage path.</span></span>

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

### <span data-ttu-id="1a87f-127">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="1a87f-127">-TargetResourceId</span></span>
<span data-ttu-id="1a87f-128">Sorunu gidermek için kaynağın kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1a87f-128">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="1a87f-129">Örnek biçim: "/Subscriptions/$ {SubscriptionID}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="1a87f-129">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="1a87f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a87f-130">CommonParameters</span></span>
<span data-ttu-id="1a87f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1a87f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a87f-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a87f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a87f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1a87f-133">INPUTS</span></span>

### <span data-ttu-id="1a87f-134">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1a87f-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1a87f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1a87f-135">System.String</span></span>

## <span data-ttu-id="1a87f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1a87f-136">OUTPUTS</span></span>

### <span data-ttu-id="1a87f-137">Microsoft. Azure. Commands. Network. model. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="1a87f-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="1a87f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1a87f-138">NOTES</span></span>
<span data-ttu-id="1a87f-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sorun giderme, VPN, bağlantı</span><span class="sxs-lookup"><span data-stu-id="1a87f-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="1a87f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1a87f-140">RELATED LINKS</span></span>

[<span data-ttu-id="1a87f-141">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1a87f-141">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1a87f-142">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="1a87f-142">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1a87f-143">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1a87f-143">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1a87f-144">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1a87f-144">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1a87f-145">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a87f-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a87f-146">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1a87f-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1a87f-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a87f-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a87f-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a87f-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a87f-149">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1a87f-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1a87f-150">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1a87f-150">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1a87f-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1a87f-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1a87f-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1a87f-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1a87f-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1a87f-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
