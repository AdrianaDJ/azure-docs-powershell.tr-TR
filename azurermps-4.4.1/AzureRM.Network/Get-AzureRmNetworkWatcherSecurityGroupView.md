---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 44bba48f1d066c4a9006595092bd84c68252bbd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592182"
---
# <span data-ttu-id="06dc2-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="06dc2-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="06dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="06dc2-103">VM 'ye uygulanan yapılandırılmış ve etkin ağ güvenlik grubu kurallarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="06dc2-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06dc2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06dc2-104">SYNTAX</span></span>

### <span data-ttu-id="06dc2-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="06dc2-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06dc2-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="06dc2-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06dc2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="06dc2-107">DESCRIPTION</span></span>
<span data-ttu-id="06dc2-108">Get-AzureRmNetworkWatcherSecurityGroupView, VM 'ye uygulanan yapılandırılmış ve etkili ağ güvenlik grubu kurallarını görüntülemenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="06dc2-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="06dc2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06dc2-109">EXAMPLES</span></span>

### <span data-ttu-id="06dc2-110">Örnek 1: bir VM---bir güvenlik grubu görünümü araması yapma---</span><span class="sxs-lookup"><span data-stu-id="06dc2-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="06dc2-111">Yukarıdaki örnekte, önce bölgesel ağ Izleyicisi 'ni, ardından bölgedeki bir VM 'yi ediniyoruz.</span><span class="sxs-lookup"><span data-stu-id="06dc2-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="06dc2-112">Ardından belirtilen VM 'de bir güvenlik grubu görünümü araması yaptık.</span><span class="sxs-lookup"><span data-stu-id="06dc2-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="06dc2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06dc2-113">PARAMETERS</span></span>

### <span data-ttu-id="06dc2-114">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06dc2-114">-NetworkWatcher</span></span>
<span data-ttu-id="06dc2-115">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="06dc2-115">The network watcher resource.</span></span>

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

### <span data-ttu-id="06dc2-116">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="06dc2-116">-NetworkWatcherName</span></span>
<span data-ttu-id="06dc2-117">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="06dc2-117">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06dc2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06dc2-118">-ResourceGroupName</span></span>
<span data-ttu-id="06dc2-119">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="06dc2-119">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06dc2-120">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="06dc2-120">-TargetVirtualMachineId</span></span>
<span data-ttu-id="06dc2-121">Hedef VM kimliği</span><span class="sxs-lookup"><span data-stu-id="06dc2-121">The target VM Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06dc2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06dc2-122">-DefaultProfile</span></span>
<span data-ttu-id="06dc2-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06dc2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06dc2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06dc2-124">CommonParameters</span></span>
<span data-ttu-id="06dc2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06dc2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06dc2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06dc2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06dc2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06dc2-127">INPUTS</span></span>

### <span data-ttu-id="06dc2-128">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06dc2-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="06dc2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="06dc2-129">System.String</span></span>

## <span data-ttu-id="06dc2-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06dc2-130">OUTPUTS</span></span>

### <span data-ttu-id="06dc2-131">Microsoft. Azure. Commands. Network. model. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="06dc2-131">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="06dc2-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06dc2-132">NOTES</span></span>
<span data-ttu-id="06dc2-133">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="06dc2-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="06dc2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06dc2-134">RELATED LINKS</span></span>

[<span data-ttu-id="06dc2-135">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06dc2-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="06dc2-136">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06dc2-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="06dc2-137">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="06dc2-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="06dc2-138">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="06dc2-138">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="06dc2-139">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="06dc2-139">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="06dc2-140">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="06dc2-140">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="06dc2-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="06dc2-141">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="06dc2-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06dc2-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06dc2-143">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="06dc2-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="06dc2-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06dc2-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06dc2-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06dc2-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="06dc2-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="06dc2-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

