---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Start-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 61b23db6cfc634b318aa0070b5f784ad7067a234
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936491"
---
# <span data-ttu-id="4f18e-101">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="4f18e-101">Start-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="4f18e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f18e-102">SYNOPSIS</span></span>
<span data-ttu-id="4f18e-103">Bağlantı izleyicisini başlatma</span><span class="sxs-lookup"><span data-stu-id="4f18e-103">Start a connection monitor</span></span>

## <span data-ttu-id="4f18e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4f18e-104">SYNTAX</span></span>

### <span data-ttu-id="4f18e-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4f18e-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4f18e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4f18e-106">SetByName</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4f18e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="4f18e-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4f18e-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="4f18e-108">SetByResourceId</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4f18e-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="4f18e-109">SetByInputObject</span></span>
```
Start-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4f18e-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="4f18e-110">DESCRIPTION</span></span>
<span data-ttu-id="4f18e-111">Start-AzNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini başlatır.</span><span class="sxs-lookup"><span data-stu-id="4f18e-111">The Start-AzNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="4f18e-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4f18e-112">EXAMPLES</span></span>

### <span data-ttu-id="4f18e-113">---------------Örnek 1: Bağlantı İzleyicisi başlatma---------------</span><span class="sxs-lookup"><span data-stu-id="4f18e-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="4f18e-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini başlatabiliriz</span><span class="sxs-lookup"><span data-stu-id="4f18e-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="4f18e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4f18e-115">PARAMETERS</span></span>

### <span data-ttu-id="4f18e-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="4f18e-116">-AsJob</span></span>
<span data-ttu-id="4f18e-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4f18e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f18e-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="4f18e-118">-Confirm</span></span>
<span data-ttu-id="4f18e-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4f18e-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f18e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f18e-120">-DefaultProfile</span></span>
<span data-ttu-id="4f18e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4f18e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f18e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f18e-122">-InputObject</span></span>
<span data-ttu-id="4f18e-123">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4f18e-123">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f18e-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="4f18e-124">-Location</span></span>
<span data-ttu-id="4f18e-125">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="4f18e-125">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f18e-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="4f18e-126">-Name</span></span>
<span data-ttu-id="4f18e-127">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="4f18e-127">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f18e-128">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4f18e-128">-NetworkWatcher</span></span>
<span data-ttu-id="4f18e-129">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="4f18e-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="4f18e-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4f18e-130">-NetworkWatcherName</span></span>
<span data-ttu-id="4f18e-131">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="4f18e-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="4f18e-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4f18e-132">-PassThru</span></span>
<span data-ttu-id="4f18e-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="4f18e-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4f18e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f18e-134">-ResourceGroupName</span></span>
<span data-ttu-id="4f18e-135">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4f18e-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4f18e-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4f18e-136">-ResourceId</span></span>
<span data-ttu-id="4f18e-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4f18e-137">Resource ID.</span></span>

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

### <span data-ttu-id="4f18e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f18e-138">-WhatIf</span></span>
<span data-ttu-id="4f18e-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f18e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f18e-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4f18e-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="4f18e-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4f18e-141">INPUTS</span></span>

### <span data-ttu-id="4f18e-142">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4f18e-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4f18e-143">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="4f18e-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="4f18e-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4f18e-144">OUTPUTS</span></span>

### <span data-ttu-id="4f18e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f18e-145">System.Boolean</span></span>


## <span data-ttu-id="4f18e-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4f18e-146">NOTES</span></span>
<span data-ttu-id="4f18e-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="4f18e-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="4f18e-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4f18e-148">RELATED LINKS</span></span>
<span data-ttu-id="4f18e-149">[Yeni-Azağ İzleyicisi](./New-AzNetworkWatcher.md) 
 [Get-Azağizleyicisi](./Get-AzNetworkWatcher.md) 
 [Remove-Aznetworkizleyicisi](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="4f18e-149">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="4f18e-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="4f18e-150">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="4f18e-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [Yeni-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="4f18e-151">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="4f18e-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md) 
 [Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="4f18e-152">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)
[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)</span></span>