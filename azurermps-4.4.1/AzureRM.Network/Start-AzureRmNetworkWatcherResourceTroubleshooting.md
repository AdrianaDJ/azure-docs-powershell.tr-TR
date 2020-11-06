---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: f220f029b25963fa07d582b6ddd70b572791924a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593813"
---
# <span data-ttu-id="5c7a2-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5c7a2-101">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="5c7a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7a2-103">Azure 'daki bir ağ kaynağında sorun gidermeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c7a2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c7a2-104">SYNTAX</span></span>

### <span data-ttu-id="5c7a2-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5c7a2-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c7a2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5c7a2-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c7a2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c7a2-107">DESCRIPTION</span></span>
<span data-ttu-id="5c7a2-108">Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet 'i Azure 'daki bir ağ kaynağında sorun gidermeyi başlatır ve olası sorunlar ve Azaltıcı Etkenler hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-108">The Start-AzureRmNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="5c7a2-109">Şu anda sanal ağ geçitleri ve bağlantılar desteklenir.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-109">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="5c7a2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c7a2-110">EXAMPLES</span></span>

### <span data-ttu-id="5c7a2-111">---Örnek 1: sanal ağ geçidinde sorun giderme---</span><span class="sxs-lookup"><span data-stu-id="5c7a2-111">--- Example 1: Start Troubleshooting on a Virtual Network Gateway ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="5c7a2-112">Yukarıdaki örnek sanal ağ geçidinde sorun gidermeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-112">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="5c7a2-113">İşlemin tamamlanması birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-113">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="5c7a2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c7a2-114">PARAMETERS</span></span>

### <span data-ttu-id="5c7a2-115">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5c7a2-115">-NetworkWatcher</span></span>
<span data-ttu-id="5c7a2-116">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-116">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c7a2-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5c7a2-117">-NetworkWatcherName</span></span>
<span data-ttu-id="5c7a2-118">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-118">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c7a2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c7a2-119">-ResourceGroupName</span></span>
<span data-ttu-id="5c7a2-120">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-120">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c7a2-121">-Storageıd</span><span class="sxs-lookup"><span data-stu-id="5c7a2-121">-StorageId</span></span>
<span data-ttu-id="5c7a2-122">Depolama KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-122">The storage ID.</span></span>

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

### <span data-ttu-id="5c7a2-123">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="5c7a2-123">-StoragePath</span></span>
<span data-ttu-id="5c7a2-124">Depolama yolu.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-124">The storage path.</span></span>

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

### <span data-ttu-id="5c7a2-125">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="5c7a2-125">-TargetResourceId</span></span>
<span data-ttu-id="5c7a2-126">Sorunu gidermek için kaynağın kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-126">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="5c7a2-127">Örnek biçim: "/Subscriptions/$ {SubscriptionID}/resourceGroups/$ {resourceGroupName}/providers/Microsoft.Network/connections/$ {connectionName}"</span><span class="sxs-lookup"><span data-stu-id="5c7a2-127">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="5c7a2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7a2-128">-DefaultProfile</span></span>
<span data-ttu-id="5c7a2-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c7a2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7a2-130">CommonParameters</span></span>
<span data-ttu-id="5c7a2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c7a2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7a2-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c7a2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7a2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c7a2-133">INPUTS</span></span>

### <span data-ttu-id="5c7a2-134">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5c7a2-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5c7a2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5c7a2-135">System.String</span></span>

## <span data-ttu-id="5c7a2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c7a2-136">OUTPUTS</span></span>

### <span data-ttu-id="5c7a2-137">Microsoft. Azure. Commands. Network. model. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="5c7a2-137">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="5c7a2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c7a2-138">NOTES</span></span>
<span data-ttu-id="5c7a2-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sorun giderme, VPN, bağlantı</span><span class="sxs-lookup"><span data-stu-id="5c7a2-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="5c7a2-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c7a2-140">RELATED LINKS</span></span>

[<span data-ttu-id="5c7a2-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5c7a2-141">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5c7a2-142">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5c7a2-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5c7a2-143">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5c7a2-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5c7a2-144">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="5c7a2-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5c7a2-145">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c7a2-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5c7a2-146">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5c7a2-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5c7a2-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c7a2-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5c7a2-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c7a2-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5c7a2-149">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5c7a2-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5c7a2-150">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5c7a2-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5c7a2-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5c7a2-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5c7a2-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5c7a2-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5c7a2-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5c7a2-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)
