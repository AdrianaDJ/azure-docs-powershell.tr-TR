---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3cb69a6dbf2a08c242d0a49e6d023692663b7f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591336"
---
# <span data-ttu-id="fd054-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd054-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="fd054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd054-102">SYNOPSIS</span></span>
<span data-ttu-id="fd054-103">Bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="fd054-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd054-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd054-104">SYNTAX</span></span>

### <span data-ttu-id="fd054-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fd054-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd054-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="fd054-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd054-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="fd054-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd054-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="fd054-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd054-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd054-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd054-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd054-110">DESCRIPTION</span></span>
<span data-ttu-id="fd054-111">Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini durdurur.</span><span class="sxs-lookup"><span data-stu-id="fd054-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="fd054-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd054-112">EXAMPLES</span></span>

### <span data-ttu-id="fd054-113">Örnek 1: bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="fd054-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="fd054-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini durdurmamız</span><span class="sxs-lookup"><span data-stu-id="fd054-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="fd054-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd054-115">PARAMETERS</span></span>

### <span data-ttu-id="fd054-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="fd054-116">-AsJob</span></span>
<span data-ttu-id="fd054-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fd054-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd054-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd054-118">-DefaultProfile</span></span>
<span data-ttu-id="fd054-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fd054-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd054-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd054-120">-InputObject</span></span>
<span data-ttu-id="fd054-121">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="fd054-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="fd054-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="fd054-122">-Location</span></span>
<span data-ttu-id="fd054-123">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="fd054-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="fd054-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd054-124">-Name</span></span>
<span data-ttu-id="fd054-125">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="fd054-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="fd054-126">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="fd054-126">-NetworkWatcher</span></span>
<span data-ttu-id="fd054-127">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="fd054-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="fd054-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fd054-128">-NetworkWatcherName</span></span>
<span data-ttu-id="fd054-129">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="fd054-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="fd054-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fd054-130">-PassThru</span></span>
<span data-ttu-id="fd054-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="fd054-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fd054-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd054-132">-ResourceGroupName</span></span>
<span data-ttu-id="fd054-133">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fd054-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fd054-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fd054-134">-ResourceId</span></span>
<span data-ttu-id="fd054-135">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="fd054-135">Resource ID.</span></span>

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

### <span data-ttu-id="fd054-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd054-136">-Confirm</span></span>
<span data-ttu-id="fd054-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd054-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd054-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd054-138">-WhatIf</span></span>
<span data-ttu-id="fd054-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd054-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd054-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd054-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd054-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd054-141">CommonParameters</span></span>
<span data-ttu-id="fd054-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd054-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd054-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd054-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd054-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd054-144">INPUTS</span></span>

### <span data-ttu-id="fd054-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="fd054-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="fd054-146">Parametreler: Ağizleyicisi (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd054-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="fd054-147">System. String</span><span class="sxs-lookup"><span data-stu-id="fd054-147">System.String</span></span>

### <span data-ttu-id="fd054-148">Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="fd054-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="fd054-149">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fd054-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fd054-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd054-150">OUTPUTS</span></span>

### <span data-ttu-id="fd054-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fd054-151">System.Boolean</span></span>

## <span data-ttu-id="fd054-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd054-152">NOTES</span></span>
<span data-ttu-id="fd054-153">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="fd054-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="fd054-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd054-154">RELATED LINKS</span></span>

[<span data-ttu-id="fd054-155">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="fd054-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fd054-156">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="fd054-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fd054-157">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="fd054-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="fd054-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fd054-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="fd054-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fd054-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="fd054-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fd054-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="fd054-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="fd054-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="fd054-162">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd054-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fd054-163">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fd054-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="fd054-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd054-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fd054-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd054-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fd054-166">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fd054-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="fd054-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd054-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd054-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="fd054-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="fd054-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd054-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd054-170">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd054-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd054-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd054-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd054-172">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd054-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd054-173">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd054-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="fd054-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fd054-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="fd054-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="fd054-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="fd054-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fd054-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="fd054-177">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="fd054-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="fd054-178">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="fd054-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="fd054-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="fd054-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="fd054-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="fd054-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="fd054-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="fd054-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
