---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: ee92fd78d3a69b38620b2af543e01db7569d3b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586882"
---
# <span data-ttu-id="71358-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="71358-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="71358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71358-102">SYNOPSIS</span></span>
<span data-ttu-id="71358-103">Ağ Izleyicisi 'Ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71358-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71358-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="71358-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71358-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="71358-105">DESCRIPTION</span></span>
<span data-ttu-id="71358-106">Remove-AzureRmNetworkWatcher cmdlet 'i ağ Izleyicisi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="71358-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="71358-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="71358-107">EXAMPLES</span></span>

### <span data-ttu-id="71358-108">--------------------------Örnek 1: ağ Izleyicisi oluşturma ve silme--------------------------</span><span class="sxs-lookup"><span data-stu-id="71358-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="71358-109">Bu örnekte, kaynak grubunda bir ağ Izleyicisi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="71358-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="71358-110">Her abonelik için bölge başına yalnızca bir ağ Izleyicisi oluşturulabiliriz.</span><span class="sxs-lookup"><span data-stu-id="71358-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="71358-111">Sanal ağı silerken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="71358-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="71358-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="71358-112">PARAMETERS</span></span>

### <span data-ttu-id="71358-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="71358-113">-Name</span></span>
<span data-ttu-id="71358-114">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="71358-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71358-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="71358-115">-PassThru</span></span>
<span data-ttu-id="71358-116">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="71358-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71358-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71358-117">-ResourceGroupName</span></span>
<span data-ttu-id="71358-118">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="71358-118">The resource group name.</span></span>

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

### <span data-ttu-id="71358-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="71358-119">-Confirm</span></span>
<span data-ttu-id="71358-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="71358-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71358-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71358-121">-WhatIf</span></span>
<span data-ttu-id="71358-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="71358-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71358-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="71358-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71358-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71358-124">-DefaultProfile</span></span>
<span data-ttu-id="71358-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="71358-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71358-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71358-126">CommonParameters</span></span>
<span data-ttu-id="71358-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="71358-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71358-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71358-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71358-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="71358-129">INPUTS</span></span>

### <span data-ttu-id="71358-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71358-130">System.String</span></span>

## <span data-ttu-id="71358-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="71358-131">OUTPUTS</span></span>

### <span data-ttu-id="71358-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="71358-132">System.Object</span></span>

## <span data-ttu-id="71358-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="71358-133">NOTES</span></span>
<span data-ttu-id="71358-134">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="71358-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="71358-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="71358-135">RELATED LINKS</span></span>

[<span data-ttu-id="71358-136">Yeni-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="71358-136">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="71358-137">Get-Azurermnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="71358-137">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="71358-138">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71358-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71358-139">Yeni-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="71358-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="71358-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71358-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71358-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71358-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71358-142">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="71358-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="71358-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="71358-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="71358-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="71358-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="71358-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="71358-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="71358-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="71358-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="71358-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="71358-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
