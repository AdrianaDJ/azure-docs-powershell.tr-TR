---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: 4fd6da3388b4058a3aa4bee2fe918fb063c8fd6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590964"
---
# <span data-ttu-id="4713e-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4713e-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="4713e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4713e-102">SYNOPSIS</span></span>
<span data-ttu-id="4713e-103">Ağ Izleyicisi 'Ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4713e-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4713e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4713e-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4713e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4713e-105">DESCRIPTION</span></span>
<span data-ttu-id="4713e-106">Remove-AzureRmNetworkWatcher cmdlet 'i ağ Izleyicisi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4713e-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="4713e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4713e-107">EXAMPLES</span></span>

### <span data-ttu-id="4713e-108">--------------------------Örnek 1: ağ Izleyicisi oluşturma ve silme--------------------------</span><span class="sxs-lookup"><span data-stu-id="4713e-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="4713e-109">Bu örnekte, kaynak grubunda bir ağ Izleyicisi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="4713e-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="4713e-110">Her abonelik için bölge başına yalnızca bir ağ Izleyicisi oluşturulabiliriz.</span><span class="sxs-lookup"><span data-stu-id="4713e-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="4713e-111">Sanal ağı silerken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="4713e-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="4713e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4713e-112">PARAMETERS</span></span>

### <span data-ttu-id="4713e-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="4713e-113">-AsJob</span></span>
<span data-ttu-id="4713e-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4713e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4713e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4713e-115">-DefaultProfile</span></span>
<span data-ttu-id="4713e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4713e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4713e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="4713e-117">-Name</span></span>
<span data-ttu-id="4713e-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4713e-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4713e-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4713e-119">-PassThru</span></span>
<span data-ttu-id="4713e-120">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="4713e-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4713e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4713e-121">-ResourceGroupName</span></span>
<span data-ttu-id="4713e-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4713e-122">The resource group name.</span></span>

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

### <span data-ttu-id="4713e-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="4713e-123">-Confirm</span></span>
<span data-ttu-id="4713e-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4713e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4713e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4713e-125">-WhatIf</span></span>
<span data-ttu-id="4713e-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4713e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4713e-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4713e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4713e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4713e-128">CommonParameters</span></span>
<span data-ttu-id="4713e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4713e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4713e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4713e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4713e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4713e-131">INPUTS</span></span>

### <span data-ttu-id="4713e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4713e-132">System.String</span></span>

## <span data-ttu-id="4713e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4713e-133">OUTPUTS</span></span>

### <span data-ttu-id="4713e-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="4713e-134">System.Object</span></span>

## <span data-ttu-id="4713e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4713e-135">NOTES</span></span>
<span data-ttu-id="4713e-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="4713e-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="4713e-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4713e-137">RELATED LINKS</span></span>

[<span data-ttu-id="4713e-138">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4713e-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4713e-139">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="4713e-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4713e-140">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4713e-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4713e-141">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4713e-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4713e-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4713e-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4713e-143">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4713e-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4713e-144">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4713e-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4713e-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4713e-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4713e-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4713e-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="4713e-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4713e-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4713e-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4713e-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4713e-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4713e-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
