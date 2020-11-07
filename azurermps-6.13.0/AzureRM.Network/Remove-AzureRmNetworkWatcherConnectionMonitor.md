---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 01e8a41c8d8854527037c447545f3d0601d4daf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764332"
---
# <span data-ttu-id="6dfbc-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6dfbc-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="6dfbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dfbc-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfbc-103">Bağlantı izleyicisini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6dfbc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dfbc-104">SYNTAX</span></span>

### <span data-ttu-id="6dfbc-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6dfbc-105">SetByName (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6dfbc-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6dfbc-106">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dfbc-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6dfbc-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dfbc-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="6dfbc-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dfbc-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="6dfbc-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dfbc-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dfbc-110">DESCRIPTION</span></span>
<span data-ttu-id="6dfbc-111">Remove-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="6dfbc-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dfbc-112">EXAMPLES</span></span>

### <span data-ttu-id="6dfbc-113">Örnek 1: belirtilen bağlantı izleyicisini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6dfbc-113">Example 1: Remove the specified connection monitor</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="6dfbc-114">Bu örnekte, konum ve adla belirtilen bağlantı izleyicisini sileriz.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="6dfbc-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dfbc-115">PARAMETERS</span></span>

### <span data-ttu-id="6dfbc-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="6dfbc-116">-AsJob</span></span>
<span data-ttu-id="6dfbc-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6dfbc-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfbc-118">-DefaultProfile</span></span>
<span data-ttu-id="6dfbc-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dfbc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dfbc-120">-InputObject</span></span>
<span data-ttu-id="6dfbc-121">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="6dfbc-122">-Location</span></span>
<span data-ttu-id="6dfbc-123">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-123">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="6dfbc-124">-Name</span></span>
<span data-ttu-id="6dfbc-125">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6dfbc-126">-NetworkWatcher</span></span>
<span data-ttu-id="6dfbc-127">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="6dfbc-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6dfbc-128">-NetworkWatcherName</span></span>
<span data-ttu-id="6dfbc-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="6dfbc-130">-PassThru</span></span>
<span data-ttu-id="6dfbc-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="6dfbc-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dfbc-132">-ResourceGroupName</span></span>
<span data-ttu-id="6dfbc-133">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6dfbc-134">-ResourceId</span></span>
<span data-ttu-id="6dfbc-135">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="6dfbc-136">-Confirm</span></span>
<span data-ttu-id="6dfbc-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dfbc-138">-WhatIf</span></span>
<span data-ttu-id="6dfbc-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dfbc-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfbc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfbc-141">CommonParameters</span></span>
<span data-ttu-id="6dfbc-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dfbc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfbc-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dfbc-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfbc-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dfbc-144">INPUTS</span></span>

### <span data-ttu-id="6dfbc-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6dfbc-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6dfbc-146">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6dfbc-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="6dfbc-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6dfbc-147">System.String</span></span>

### <span data-ttu-id="6dfbc-148">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="6dfbc-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="6dfbc-149">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6dfbc-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6dfbc-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dfbc-150">OUTPUTS</span></span>

### <span data-ttu-id="6dfbc-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6dfbc-151">System.Boolean</span></span>

## <span data-ttu-id="6dfbc-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dfbc-152">NOTES</span></span>
<span data-ttu-id="6dfbc-153">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="6dfbc-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="6dfbc-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dfbc-154">RELATED LINKS</span></span>

[<span data-ttu-id="6dfbc-155">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6dfbc-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6dfbc-156">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6dfbc-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6dfbc-157">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="6dfbc-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="6dfbc-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6dfbc-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="6dfbc-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6dfbc-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="6dfbc-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6dfbc-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="6dfbc-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6dfbc-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="6dfbc-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6dfbc-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6dfbc-163">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6dfbc-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="6dfbc-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6dfbc-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6dfbc-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6dfbc-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6dfbc-166">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6dfbc-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="6dfbc-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6dfbc-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6dfbc-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6dfbc-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="6dfbc-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6dfbc-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6dfbc-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6dfbc-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6dfbc-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6dfbc-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6dfbc-172">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6dfbc-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6dfbc-173">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6dfbc-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="6dfbc-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6dfbc-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="6dfbc-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6dfbc-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="6dfbc-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6dfbc-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="6dfbc-177">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6dfbc-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="6dfbc-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6dfbc-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="6dfbc-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6dfbc-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="6dfbc-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6dfbc-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="6dfbc-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6dfbc-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
