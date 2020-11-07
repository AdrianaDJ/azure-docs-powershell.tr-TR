---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8e8462ded1f122a050c85877e8e82b2ecc0dd9d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938926"
---
# <span data-ttu-id="4481b-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="4481b-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="4481b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4481b-102">SYNOPSIS</span></span>
<span data-ttu-id="4481b-103">Hedef kaynak için akış günlüğünü yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="4481b-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4481b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4481b-104">SYNTAX</span></span>

### <span data-ttu-id="4481b-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4481b-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4481b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4481b-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4481b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4481b-107">DESCRIPTION</span></span>
<span data-ttu-id="4481b-108">Set-AzureRmNetworkWatcherConfigFlowLog hedef kaynağın akış günlüğünü yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="4481b-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="4481b-109">Yapılandırılacak Özellikler: sağlanan kaynak için akış günlüğünün etkinleştirilip etkinleştirilmeyeceği, günlükleri gönderecek yapılandırılmış depolama hesabı ve Günlükler için bekletme ilkesi.</span><span class="sxs-lookup"><span data-stu-id="4481b-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="4481b-110">Ağ güvenlik grupları akış günlüğü için desteklenir.</span><span class="sxs-lookup"><span data-stu-id="4481b-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="4481b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4481b-111">EXAMPLES</span></span>

### <span data-ttu-id="4481b-112">---Örnek 1: belirli bir NSG---akış günlüğünü yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4481b-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="4481b-113">Bu örnekte, ağ güvenlik grubu için akış günlüğü durumunu yapılandırmamız.</span><span class="sxs-lookup"><span data-stu-id="4481b-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="4481b-114">Yanıtta, belirtilen NSG 'da akış günlüğünün etkin olduğunu ve bekletme ilkesi ayarlanmamış olduğunu görüyoruz.</span><span class="sxs-lookup"><span data-stu-id="4481b-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="4481b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4481b-115">PARAMETERS</span></span>

### <span data-ttu-id="4481b-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="4481b-116">-AsJob</span></span>
<span data-ttu-id="4481b-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4481b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4481b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4481b-118">-DefaultProfile</span></span>
<span data-ttu-id="4481b-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4481b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4481b-120">-Enabsolaltgünlük</span><span class="sxs-lookup"><span data-stu-id="4481b-120">-EnableFlowLog</span></span>
<span data-ttu-id="4481b-121">Akış günlüğünü etkinleştirme/devre dışı bırakma bayrağı.</span><span class="sxs-lookup"><span data-stu-id="4481b-121">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="4481b-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="4481b-122">-EnableRetention</span></span>
<span data-ttu-id="4481b-123">Bekletmenin etkinleştirileceği/devre dışı bırakılması bayrağı.</span><span class="sxs-lookup"><span data-stu-id="4481b-123">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="4481b-124">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4481b-124">-NetworkWatcher</span></span>
<span data-ttu-id="4481b-125">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="4481b-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="4481b-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4481b-126">-NetworkWatcherName</span></span>
<span data-ttu-id="4481b-127">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="4481b-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="4481b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4481b-128">-ResourceGroupName</span></span>
<span data-ttu-id="4481b-129">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4481b-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4481b-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4481b-130">-RetentionInDays</span></span>
<span data-ttu-id="4481b-131">Akış günlüğü kayıtlarının tutulacağı gün sayısı.</span><span class="sxs-lookup"><span data-stu-id="4481b-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="4481b-132">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="4481b-132">-StorageAccountId</span></span>
<span data-ttu-id="4481b-133">Akış günlüğünün depolanacağı depolama hesabının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4481b-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="4481b-134">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="4481b-134">-TargetResourceId</span></span>
<span data-ttu-id="4481b-135">Hedef kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="4481b-135">The target resource ID.</span></span>

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

### <span data-ttu-id="4481b-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="4481b-136">-Confirm</span></span>
<span data-ttu-id="4481b-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4481b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4481b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4481b-138">-WhatIf</span></span>
<span data-ttu-id="4481b-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4481b-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4481b-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4481b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4481b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4481b-141">CommonParameters</span></span>
<span data-ttu-id="4481b-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4481b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4481b-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4481b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4481b-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4481b-144">INPUTS</span></span>

### <span data-ttu-id="4481b-145">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4481b-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4481b-146">System. String System. Boolean System. Int32</span><span class="sxs-lookup"><span data-stu-id="4481b-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="4481b-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4481b-147">OUTPUTS</span></span>

### <span data-ttu-id="4481b-148">Microsoft. Azure. Commands. Network. modeller. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="4481b-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="4481b-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4481b-149">NOTES</span></span>
<span data-ttu-id="4481b-150">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, akış, Günlükler, akışgünlüğü, günlüğe kaydetme</span><span class="sxs-lookup"><span data-stu-id="4481b-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="4481b-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4481b-151">RELATED LINKS</span></span>

[<span data-ttu-id="4481b-152">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="4481b-152">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="4481b-153">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4481b-153">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4481b-154">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4481b-154">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4481b-155">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4481b-155">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4481b-156">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4481b-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4481b-157">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4481b-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4481b-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4481b-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4481b-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4481b-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4481b-160">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4481b-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4481b-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4481b-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4481b-162">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4481b-162">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4481b-163">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4481b-163">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4481b-164">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4481b-164">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4481b-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4481b-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4481b-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="4481b-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
