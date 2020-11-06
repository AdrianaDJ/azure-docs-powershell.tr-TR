---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: e49245fabd4387c48def797168e1d572a43d6bfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588859"
---
# <span data-ttu-id="ab143-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab143-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ab143-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab143-102">SYNOPSIS</span></span>
<span data-ttu-id="ab143-103">Bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="ab143-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab143-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab143-104">SYNTAX</span></span>

### <span data-ttu-id="ab143-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ab143-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab143-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="ab143-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab143-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ab143-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab143-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="ab143-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab143-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab143-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab143-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab143-110">DESCRIPTION</span></span>
<span data-ttu-id="ab143-111">Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini durdurur.</span><span class="sxs-lookup"><span data-stu-id="ab143-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="ab143-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab143-112">EXAMPLES</span></span>

### <span data-ttu-id="ab143-113">Örnek 1: bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="ab143-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="ab143-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini durdurmamız</span><span class="sxs-lookup"><span data-stu-id="ab143-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="ab143-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab143-115">PARAMETERS</span></span>

### <span data-ttu-id="ab143-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="ab143-116">-AsJob</span></span>
<span data-ttu-id="ab143-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ab143-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab143-118">-Confirm</span></span>
<span data-ttu-id="ab143-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab143-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab143-120">-DefaultProfile</span></span>
<span data-ttu-id="ab143-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab143-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab143-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab143-122">-InputObject</span></span>
<span data-ttu-id="ab143-123">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ab143-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="ab143-124">-Location</span></span>
<span data-ttu-id="ab143-125">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="ab143-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab143-126">-Name</span></span>
<span data-ttu-id="ab143-127">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="ab143-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-128">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab143-128">-NetworkWatcher</span></span>
<span data-ttu-id="ab143-129">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="ab143-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="ab143-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ab143-130">-NetworkWatcherName</span></span>
<span data-ttu-id="ab143-131">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="ab143-131">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ab143-132">-PassThru</span></span>
<span data-ttu-id="ab143-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ab143-133">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab143-134">-ResourceGroupName</span></span>
<span data-ttu-id="ab143-135">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ab143-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ab143-136">-ResourceId</span></span>
<span data-ttu-id="ab143-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ab143-137">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab143-138">-WhatIf</span></span>
<span data-ttu-id="ab143-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab143-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab143-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ab143-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab143-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab143-141">CommonParameters</span></span>
<span data-ttu-id="ab143-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab143-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ab143-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab143-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab143-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab143-144">INPUTS</span></span>

### <span data-ttu-id="ab143-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab143-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ab143-146">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ab143-146">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="ab143-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab143-147">OUTPUTS</span></span>

### <span data-ttu-id="ab143-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab143-148">System.Boolean</span></span>

## <span data-ttu-id="ab143-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab143-149">NOTES</span></span>
<span data-ttu-id="ab143-150">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab143-150">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="ab143-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab143-151">RELATED LINKS</span></span>

[<span data-ttu-id="ab143-152">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab143-152">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ab143-153">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab143-153">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ab143-154">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab143-154">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="ab143-155">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ab143-155">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="ab143-156">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ab143-156">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="ab143-157">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ab143-157">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="ab143-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ab143-158">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="ab143-159">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab143-159">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ab143-160">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ab143-160">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="ab143-161">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab143-161">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ab143-162">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab143-162">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ab143-163">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ab143-163">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="ab143-164">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab143-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ab143-165">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab143-165">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ab143-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ab143-166">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="ab143-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab143-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ab143-168">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab143-168">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="ab143-169">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab143-169">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
