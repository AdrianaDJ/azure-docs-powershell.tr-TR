---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
ms.openlocfilehash: fad852ff589b2929df83775a2fa955e72663cfa2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938948"
---
# <span data-ttu-id="4b5f7-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4b5f7-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="4b5f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5f7-103">VM 'ye uygulanan yapılandırılmış ve etkin ağ güvenlik grubu kurallarını görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b5f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b5f7-104">SYNTAX</span></span>

### <span data-ttu-id="4b5f7-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b5f7-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b5f7-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4b5f7-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b5f7-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b5f7-107">DESCRIPTION</span></span>
<span data-ttu-id="4b5f7-108">Get-AzureRmNetworkWatcherSecurityGroupView, VM 'ye uygulanan yapılandırılmış ve etkili ağ güvenlik grubu kurallarını görüntülemenize izin verir.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="4b5f7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b5f7-109">EXAMPLES</span></span>

### <span data-ttu-id="4b5f7-110">Örnek 1: bir VM---bir güvenlik grubu görünümü araması yapma---</span><span class="sxs-lookup"><span data-stu-id="4b5f7-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="4b5f7-111">Yukarıdaki örnekte, önce bölgesel ağ Izleyicisi 'ni, ardından bölgedeki bir VM 'yi ediniyoruz.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="4b5f7-112">Ardından belirtilen VM 'de bir güvenlik grubu görünümü araması yaptık.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="4b5f7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b5f7-113">PARAMETERS</span></span>

### <span data-ttu-id="4b5f7-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="4b5f7-114">-AsJob</span></span>
<span data-ttu-id="4b5f7-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4b5f7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b5f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5f7-116">-DefaultProfile</span></span>
<span data-ttu-id="4b5f7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b5f7-118">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4b5f7-118">-NetworkWatcher</span></span>
<span data-ttu-id="4b5f7-119">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="4b5f7-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4b5f7-120">-NetworkWatcherName</span></span>
<span data-ttu-id="4b5f7-121">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="4b5f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="4b5f7-123">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4b5f7-124">-Targetvirtualmachineıd</span><span class="sxs-lookup"><span data-stu-id="4b5f7-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="4b5f7-125">Hedef VM kimliği</span><span class="sxs-lookup"><span data-stu-id="4b5f7-125">The target VM Id</span></span>

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

### <span data-ttu-id="4b5f7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5f7-126">CommonParameters</span></span>
<span data-ttu-id="4b5f7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b5f7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5f7-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5f7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5f7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b5f7-129">INPUTS</span></span>

### <span data-ttu-id="4b5f7-130">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4b5f7-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4b5f7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5f7-131">System.String</span></span>

## <span data-ttu-id="4b5f7-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b5f7-132">OUTPUTS</span></span>

### <span data-ttu-id="4b5f7-133">Microsoft. Azure. Commands. Network. model. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="4b5f7-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="4b5f7-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b5f7-134">NOTES</span></span>
<span data-ttu-id="4b5f7-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, akış, IP</span><span class="sxs-lookup"><span data-stu-id="4b5f7-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="4b5f7-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b5f7-136">RELATED LINKS</span></span>

[<span data-ttu-id="4b5f7-137">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4b5f7-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4b5f7-138">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4b5f7-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4b5f7-139">Remove-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4b5f7-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4b5f7-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4b5f7-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4b5f7-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4b5f7-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4b5f7-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4b5f7-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4b5f7-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4b5f7-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4b5f7-144">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b5f7-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b5f7-145">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4b5f7-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4b5f7-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b5f7-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b5f7-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b5f7-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4b5f7-148">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4b5f7-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

