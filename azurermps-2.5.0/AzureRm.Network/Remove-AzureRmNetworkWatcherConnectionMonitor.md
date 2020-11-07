---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 046a2ee4591eb345efd71163d27140799cb229e2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939503"
---
# <span data-ttu-id="ab793-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ab793-101">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="ab793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab793-102">SYNOPSIS</span></span>
<span data-ttu-id="ab793-103">Bağlantı izleyicisini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="ab793-103">Remove connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab793-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab793-104">SYNTAX</span></span>

### <span data-ttu-id="ab793-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ab793-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ab793-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ab793-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ab793-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ab793-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ab793-108">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="ab793-108">SetByResourceId</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="ab793-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab793-109">SetByInputObject</span></span>
```
Remove-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="ab793-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab793-110">DESCRIPTION</span></span>
<span data-ttu-id="ab793-111">Remove-AzureRmNetworkWatcherConnectionMonitor cmdlet 'i belirtilen bağlantı izleyicisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ab793-111">The remove-AzureRmNetworkWatcherConnectionMonitor cmdlet removes the specified connection monitor.</span></span>

## <span data-ttu-id="ab793-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab793-112">EXAMPLES</span></span>

### <span data-ttu-id="ab793-113">---------------Örnek 1: belirtilen bağlantı izleyicisini---------------</span><span class="sxs-lookup"><span data-stu-id="ab793-113">---------------  Example 1: Remove the specified connection monitor ---------------</span></span>
```
PS C:\> Remove-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="ab793-114">Bu örnekte, konum ve adla belirtilen bağlantı izleyicisini sileriz.</span><span class="sxs-lookup"><span data-stu-id="ab793-114">In this example we delete the connection monitor specified by location and name.</span></span>

## <span data-ttu-id="ab793-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab793-115">PARAMETERS</span></span>

### <span data-ttu-id="ab793-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="ab793-116">-AsJob</span></span>
<span data-ttu-id="ab793-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ab793-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ab793-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab793-118">-Confirm</span></span>
<span data-ttu-id="ab793-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab793-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab793-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab793-120">-DefaultProfile</span></span>
<span data-ttu-id="ab793-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab793-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab793-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab793-122">-InputObject</span></span>
<span data-ttu-id="ab793-123">Bağlantı İzleyicisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ab793-123">Connection monitor object.</span></span>

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

### <span data-ttu-id="ab793-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="ab793-124">-Location</span></span>
<span data-ttu-id="ab793-125">Ağ İzleyicisi 'nin konumu.</span><span class="sxs-lookup"><span data-stu-id="ab793-125">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ab793-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="ab793-126">-Name</span></span>
<span data-ttu-id="ab793-127">Bağlantı izleyici adı.</span><span class="sxs-lookup"><span data-stu-id="ab793-127">The connection monitor name.</span></span>

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

### <span data-ttu-id="ab793-128">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab793-128">-NetworkWatcher</span></span>
<span data-ttu-id="ab793-129">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="ab793-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="ab793-130">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ab793-130">-NetworkWatcherName</span></span>
<span data-ttu-id="ab793-131">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="ab793-131">The name of network watcher.</span></span>

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

### <span data-ttu-id="ab793-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ab793-132">-PassThru</span></span>
<span data-ttu-id="ab793-133">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ab793-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ab793-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab793-134">-ResourceGroupName</span></span>
<span data-ttu-id="ab793-135">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ab793-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ab793-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ab793-136">-ResourceId</span></span>
<span data-ttu-id="ab793-137">Kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ab793-137">Resource ID.</span></span>

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

### <span data-ttu-id="ab793-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab793-138">-WhatIf</span></span>
<span data-ttu-id="ab793-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab793-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab793-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ab793-140">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="ab793-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab793-141">INPUTS</span></span>

### <span data-ttu-id="ab793-142">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab793-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ab793-143">System. String Microsoft. Azure. Commands. Network. modeller. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="ab793-143">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="ab793-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab793-144">OUTPUTS</span></span>

### <span data-ttu-id="ab793-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab793-145">System.Boolean</span></span>


## <span data-ttu-id="ab793-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab793-146">NOTES</span></span>
<span data-ttu-id="ab793-147">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, Bağlantı İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="ab793-147">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="ab793-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab793-148">RELATED LINKS</span></span>
<span data-ttu-id="ab793-149">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="ab793-149">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="ab793-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="ab793-150">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="ab793-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="ab793-151">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="ab793-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="ab793-152">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>

