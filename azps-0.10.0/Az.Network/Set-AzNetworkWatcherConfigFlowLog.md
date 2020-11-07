---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936522"
---
# <span data-ttu-id="1108c-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1108c-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="1108c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1108c-102">SYNOPSIS</span></span>
<span data-ttu-id="1108c-103">Hedef kaynak için akış günlüğünü yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="1108c-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="1108c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1108c-104">SYNTAX</span></span>

### <span data-ttu-id="1108c-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1108c-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1108c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1108c-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1108c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1108c-107">DESCRIPTION</span></span>
<span data-ttu-id="1108c-108">Set-AzNetworkWatcherConfigFlowLog hedef kaynağın akış günlüğünü yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="1108c-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="1108c-109">Yapılandırılacak Özellikler: sağlanan kaynak için akış günlüğünün etkinleştirilip etkinleştirilmeyeceği, günlükleri gönderecek yapılandırılmış depolama hesabı ve Günlükler için bekletme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="1108c-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="1108c-110">Ağ güvenlik grupları akış günlüğü için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="1108c-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="1108c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1108c-111">EXAMPLES</span></span>

### <span data-ttu-id="1108c-112">---Örnek 1: belirli bir NSG---akış günlüğünü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="1108c-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="1108c-113">Bu örnekte, ağ güvenlik grubu için akış günlüğü durumunu yapılandırmamız.</span><span class="sxs-lookup"><span data-stu-id="1108c-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="1108c-114">Yanıtta, belirtilen NSG 'da akış günlüğünün etkin olduğunu ve bekletme ilkesi ayarlanmamış olduğunu görüyoruz.</span><span class="sxs-lookup"><span data-stu-id="1108c-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="1108c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1108c-115">PARAMETERS</span></span>

### <span data-ttu-id="1108c-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="1108c-116">-AsJob</span></span>
<span data-ttu-id="1108c-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1108c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1108c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1108c-118">-DefaultProfile</span></span>
<span data-ttu-id="1108c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1108c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1108c-120">-Enabsolaltgünlük</span><span class="sxs-lookup"><span data-stu-id="1108c-120">-EnableFlowLog</span></span>
<span data-ttu-id="1108c-121">Akış günlüğünü etkinleştirme/devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="1108c-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108c-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="1108c-122">-EnableRetention</span></span>
<span data-ttu-id="1108c-123">Bekletmenin etkinleştirileceği/devre dışı bırakılması bayrağı.</span><span class="sxs-lookup"><span data-stu-id="1108c-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108c-124">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1108c-124">-NetworkWatcher</span></span>
<span data-ttu-id="1108c-125">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="1108c-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="1108c-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1108c-126">-NetworkWatcherName</span></span>
<span data-ttu-id="1108c-127">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="1108c-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="1108c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1108c-128">-ResourceGroupName</span></span>
<span data-ttu-id="1108c-129">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="1108c-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1108c-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1108c-130">-RetentionInDays</span></span>
<span data-ttu-id="1108c-131">Akış günlüğü kayıtlarının tutulacağı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="1108c-131">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108c-132">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="1108c-132">-StorageAccountId</span></span>
<span data-ttu-id="1108c-133">Akış günlüğünün depolanacağı depolama hesabının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1108c-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="1108c-134">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="1108c-134">-TargetResourceId</span></span>
<span data-ttu-id="1108c-135">Hedef kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="1108c-135">The target resource ID.</span></span>

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

### <span data-ttu-id="1108c-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="1108c-136">-Confirm</span></span>
<span data-ttu-id="1108c-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1108c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1108c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1108c-138">-WhatIf</span></span>
<span data-ttu-id="1108c-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1108c-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1108c-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1108c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1108c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1108c-141">CommonParameters</span></span>
<span data-ttu-id="1108c-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1108c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1108c-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1108c-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1108c-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1108c-144">INPUTS</span></span>

### <span data-ttu-id="1108c-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1108c-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1108c-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="1108c-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="1108c-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1108c-147">OUTPUTS</span></span>

### <span data-ttu-id="1108c-148">Microsoft. Azure. Commands. Network. modeller. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="1108c-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="1108c-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1108c-149">NOTES</span></span>
<span data-ttu-id="1108c-150">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, akış, Günlükler, akışgünlüğü, günlüğe kaydetme</span><span class="sxs-lookup"><span data-stu-id="1108c-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="1108c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1108c-151">RELATED LINKS</span></span>

[<span data-ttu-id="1108c-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1108c-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1108c-153">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="1108c-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1108c-154">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1108c-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1108c-155">Remove-Aznetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="1108c-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1108c-156">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1108c-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1108c-157">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1108c-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1108c-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1108c-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1108c-159">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1108c-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1108c-160">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1108c-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1108c-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1108c-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1108c-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1108c-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1108c-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1108c-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1108c-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1108c-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1108c-165">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1108c-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1108c-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1108c-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
