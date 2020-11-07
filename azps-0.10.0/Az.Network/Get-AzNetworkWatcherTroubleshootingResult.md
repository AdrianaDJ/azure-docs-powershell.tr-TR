---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: c3d1e7e3a76a2561c77c8d580b7365f8fd2e6fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935500"
---
# <span data-ttu-id="839a0-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="839a0-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="839a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="839a0-102">SYNOPSIS</span></span>
<span data-ttu-id="839a0-103">Önceden çalıştırılmış veya çalışmakta olan sorun giderme işleminin sorun giderme sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="839a0-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="839a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="839a0-104">SYNTAX</span></span>

### <span data-ttu-id="839a0-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="839a0-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="839a0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="839a0-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839a0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="839a0-107">DESCRIPTION</span></span>
<span data-ttu-id="839a0-108">Get-AzNetworkWatcherTroubleshootingResult cmdlet 'i, daha önce çalıştırılan veya çalışmakta olan Start-AzNetworkWatcherResourceTroubleshooting işleminin sorun giderme sonucunu alır.</span><span class="sxs-lookup"><span data-stu-id="839a0-108">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="839a0-109">Sorun giderme işlemi devam ediyorsa, bu işlemin tamamlanması birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="839a0-109">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="839a0-110">Şu anda sanal ağ geçitleri ve bağlantılar desteklenir.</span><span class="sxs-lookup"><span data-stu-id="839a0-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="839a0-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="839a0-111">EXAMPLES</span></span>

### <span data-ttu-id="839a0-112">---Örnek 1: sanal ağ geçidinde sorun gidermeye başlayın ve sonucu alın---</span><span class="sxs-lookup"><span data-stu-id="839a0-112">--- Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="839a0-113">Yukarıdaki örnek sanal ağ geçidinde sorun gidermeyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="839a0-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="839a0-114">İşlemin tamamlanması birkaç dakika sürebilir.</span><span class="sxs-lookup"><span data-stu-id="839a0-114">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="839a0-115">Sorun giderme başlatıldıktan sonra, bu çağrının sonucunu almak için kaynağa bir Get-AzNetworkWatcherTroubleshootingResult çağrısı yapılır.</span><span class="sxs-lookup"><span data-stu-id="839a0-115">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="839a0-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="839a0-116">PARAMETERS</span></span>

### <span data-ttu-id="839a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839a0-117">-DefaultProfile</span></span>
<span data-ttu-id="839a0-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="839a0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="839a0-119">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="839a0-119">-NetworkWatcher</span></span>
<span data-ttu-id="839a0-120">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="839a0-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="839a0-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="839a0-121">-NetworkWatcherName</span></span>
<span data-ttu-id="839a0-122">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="839a0-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="839a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="839a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="839a0-124">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="839a0-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="839a0-125">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="839a0-125">-TargetResourceId</span></span>
<span data-ttu-id="839a0-126">Hedef kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="839a0-126">The target resource ID.</span></span>

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

### <span data-ttu-id="839a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839a0-127">CommonParameters</span></span>
<span data-ttu-id="839a0-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="839a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839a0-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839a0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839a0-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="839a0-130">INPUTS</span></span>

### <span data-ttu-id="839a0-131">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="839a0-131">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="839a0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="839a0-132">System.String</span></span>

## <span data-ttu-id="839a0-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="839a0-133">OUTPUTS</span></span>

### <span data-ttu-id="839a0-134">Microsoft. Azure. Commands. Network. model. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="839a0-134">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="839a0-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="839a0-135">NOTES</span></span>
<span data-ttu-id="839a0-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, sorun giderme, VPN, bağlantı</span><span class="sxs-lookup"><span data-stu-id="839a0-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="839a0-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="839a0-137">RELATED LINKS</span></span>

[<span data-ttu-id="839a0-138">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="839a0-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="839a0-139">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="839a0-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="839a0-140">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="839a0-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="839a0-141">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="839a0-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="839a0-142">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="839a0-142">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="839a0-143">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="839a0-143">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="839a0-144">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="839a0-144">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="839a0-145">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="839a0-145">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="839a0-146">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="839a0-146">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="839a0-147">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="839a0-147">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="839a0-148">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="839a0-148">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="839a0-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="839a0-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="839a0-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="839a0-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)
