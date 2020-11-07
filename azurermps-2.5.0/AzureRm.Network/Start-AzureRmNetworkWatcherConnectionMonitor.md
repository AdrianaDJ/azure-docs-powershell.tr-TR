---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: c8464183646ee9a78bad4f8f94a8e2093ad6b21d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939071"
---
# <span data-ttu-id="89ab2-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="89ab2-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="89ab2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89ab2-102">SYNOPSIS</span></span>
<span data-ttu-id="89ab2-103">Bağlantı izleyicisini başlatma</span><span class="sxs-lookup"><span data-stu-id="89ab2-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89ab2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89ab2-104">SYNTAX</span></span>

### <span data-ttu-id="89ab2-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="89ab2-105">SetByResource (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="89ab2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="89ab2-106">SetByName</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="89ab2-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="89ab2-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="89ab2-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="89ab2-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="89ab2-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="89ab2-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="89ab2-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="89ab2-110">DESCRIPTION</span></span>
<span data-ttu-id="89ab2-111">Start-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini başlatır.</span><span class="sxs-lookup"><span data-stu-id="89ab2-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="89ab2-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89ab2-112">EXAMPLES</span></span>

### <span data-ttu-id="89ab2-113">---------------Örnek 1: Bağlantı İzleyicisi başlatma---------------</span><span class="sxs-lookup"><span data-stu-id="89ab2-113">---------------  Example 1: Start a connection monitor ---------------</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="89ab2-114">Bu örnekte, ad ve Ağ İzleyicisi tarafından belirtilen bağlantı izleyicisini başlatabiliriz</span><span class="sxs-lookup"><span data-stu-id="89ab2-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="89ab2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89ab2-115">PARAMETERS</span></span>

### <span data-ttu-id="89ab2-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="89ab2-116">-AsJob</span></span>
<span data-ttu-id="89ab2-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="89ab2-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89ab2-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="89ab2-118">-Confirm</span></span>
<span data-ttu-id="89ab2-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89ab2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ab2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ab2-120">-DefaultProfile</span></span>
<span data-ttu-id="89ab2-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89ab2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ab2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89ab2-122">-InputObject</span></span>
<span data-ttu-id="89ab2-123">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="89ab2-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="89ab2-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="89ab2-124">-Location</span></span>
<span data-ttu-id="89ab2-125">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="89ab2-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="89ab2-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="89ab2-126">-Name</span></span>
<span data-ttu-id="89ab2-127">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="89ab2-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="89ab2-128">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="89ab2-128">-NetworkWatcher</span></span>
<span data-ttu-id="89ab2-129">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="89ab2-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="89ab2-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="89ab2-130">-NetworkWatcherName</span></span>
<span data-ttu-id="89ab2-131">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="89ab2-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="89ab2-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="89ab2-132">-PassThru</span></span>
<span data-ttu-id="89ab2-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="89ab2-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="89ab2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ab2-134">-ResourceGroupName</span></span>
<span data-ttu-id="89ab2-135">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="89ab2-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="89ab2-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="89ab2-136">-ResourceId</span></span>
<span data-ttu-id="89ab2-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="89ab2-137">Resource ID.</span></span>

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

### <span data-ttu-id="89ab2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ab2-138">-WhatIf</span></span>
<span data-ttu-id="89ab2-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89ab2-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ab2-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89ab2-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="89ab2-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89ab2-141">INPUTS</span></span>

### <span data-ttu-id="89ab2-142">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="89ab2-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="89ab2-143">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="89ab2-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="89ab2-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89ab2-144">OUTPUTS</span></span>

### <span data-ttu-id="89ab2-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89ab2-145">System.Boolean</span></span>


## <span data-ttu-id="89ab2-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89ab2-146">NOTES</span></span>
<span data-ttu-id="89ab2-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="89ab2-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="89ab2-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89ab2-148">RELATED LINKS</span></span>
<span data-ttu-id="89ab2-149">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="89ab2-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="89ab2-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="89ab2-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="89ab2-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="89ab2-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="89ab2-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="89ab2-152">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)
[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
