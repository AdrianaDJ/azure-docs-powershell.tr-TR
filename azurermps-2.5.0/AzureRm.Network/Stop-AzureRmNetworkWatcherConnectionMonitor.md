---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: a67dde4b1e8f3f97038304086b63d02d75ff8fec
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939067"
---
# <span data-ttu-id="770f5-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="770f5-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="770f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770f5-102">SYNOPSIS</span></span>
<span data-ttu-id="770f5-103">Bağlantı izleyicisini durdurma</span><span class="sxs-lookup"><span data-stu-id="770f5-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="770f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="770f5-104">SYNTAX</span></span>

### <span data-ttu-id="770f5-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="770f5-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="770f5-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="770f5-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="770f5-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="770f5-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="770f5-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="770f5-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="770f5-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="770f5-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="770f5-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="770f5-110">DESCRIPTION</span></span>
<span data-ttu-id="770f5-111">Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini durdurur.</span><span class="sxs-lookup"><span data-stu-id="770f5-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="770f5-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="770f5-112">EXAMPLES</span></span>

### <span data-ttu-id="770f5-113">---------------Örnek 1: bağlantı izleyicisini---------------</span><span class="sxs-lookup"><span data-stu-id="770f5-113">---------------  Example 1: Stop a connection monitor ---------------</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="770f5-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini durdurmamız</span><span class="sxs-lookup"><span data-stu-id="770f5-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="770f5-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="770f5-115">PARAMETERS</span></span>

### <span data-ttu-id="770f5-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="770f5-116">-AsJob</span></span>
<span data-ttu-id="770f5-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="770f5-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="770f5-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="770f5-118">-Confirm</span></span>
<span data-ttu-id="770f5-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="770f5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770f5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770f5-120">-DefaultProfile</span></span>
<span data-ttu-id="770f5-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="770f5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770f5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="770f5-122">-InputObject</span></span>
<span data-ttu-id="770f5-123">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="770f5-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="770f5-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="770f5-124">-Location</span></span>
<span data-ttu-id="770f5-125">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="770f5-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="770f5-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="770f5-126">-Name</span></span>
<span data-ttu-id="770f5-127">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="770f5-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="770f5-128">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="770f5-128">-NetworkWatcher</span></span>
<span data-ttu-id="770f5-129">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="770f5-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="770f5-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="770f5-130">-NetworkWatcherName</span></span>
<span data-ttu-id="770f5-131">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="770f5-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="770f5-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="770f5-132">-PassThru</span></span>
<span data-ttu-id="770f5-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="770f5-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="770f5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="770f5-134">-ResourceGroupName</span></span>
<span data-ttu-id="770f5-135">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="770f5-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="770f5-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="770f5-136">-ResourceId</span></span>
<span data-ttu-id="770f5-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="770f5-137">Resource ID.</span></span>

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

### <span data-ttu-id="770f5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770f5-138">-WhatIf</span></span>
<span data-ttu-id="770f5-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="770f5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770f5-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="770f5-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="770f5-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="770f5-141">INPUTS</span></span>

### <span data-ttu-id="770f5-142">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="770f5-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="770f5-143">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="770f5-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="770f5-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="770f5-144">OUTPUTS</span></span>

### <span data-ttu-id="770f5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="770f5-145">System.Boolean</span></span>


## <span data-ttu-id="770f5-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="770f5-146">NOTES</span></span>
<span data-ttu-id="770f5-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="770f5-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="770f5-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="770f5-148">RELATED LINKS</span></span>
<span data-ttu-id="770f5-149">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="770f5-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="770f5-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="770f5-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="770f5-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="770f5-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="770f5-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="770f5-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
