---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936622"
---
# <span data-ttu-id="2b2ef-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2b2ef-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="2b2ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="2b2ef-103">Ağ Izleyicisi 'Ni kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="2b2ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b2ef-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b2ef-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b2ef-105">DESCRIPTION</span></span>
<span data-ttu-id="2b2ef-106">Remove-AzNetworkWatcher cmdlet 'i ağ Izleyicisi kaynağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="2b2ef-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b2ef-107">EXAMPLES</span></span>

### <span data-ttu-id="2b2ef-108">--------------------------Örnek 1: ağ Izleyicisi oluşturma ve silme--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b2ef-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="2b2ef-109">Bu örnekte, kaynak grubunda bir ağ Izleyicisi oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="2b2ef-110">Her abonelik için bölge başına yalnızca bir ağ Izleyicisi oluşturulabiliriz.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="2b2ef-111">Sanal ağı silerken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="2b2ef-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b2ef-112">PARAMETERS</span></span>

### <span data-ttu-id="2b2ef-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="2b2ef-113">-AsJob</span></span>
<span data-ttu-id="2b2ef-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2b2ef-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b2ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b2ef-115">-DefaultProfile</span></span>
<span data-ttu-id="2b2ef-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b2ef-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b2ef-117">-Name</span></span>
<span data-ttu-id="2b2ef-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-118">The resource name.</span></span>

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

### <span data-ttu-id="2b2ef-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2b2ef-119">-PassThru</span></span>
<span data-ttu-id="2b2ef-120">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2b2ef-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2b2ef-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b2ef-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b2ef-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-122">The resource group name.</span></span>

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

### <span data-ttu-id="2b2ef-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b2ef-123">-Confirm</span></span>
<span data-ttu-id="2b2ef-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b2ef-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b2ef-125">-WhatIf</span></span>
<span data-ttu-id="2b2ef-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b2ef-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b2ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b2ef-128">CommonParameters</span></span>
<span data-ttu-id="2b2ef-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b2ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b2ef-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b2ef-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b2ef-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b2ef-131">INPUTS</span></span>

### <span data-ttu-id="2b2ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2b2ef-132">System.String</span></span>

## <span data-ttu-id="2b2ef-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b2ef-133">OUTPUTS</span></span>

### <span data-ttu-id="2b2ef-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="2b2ef-134">System.Object</span></span>

## <span data-ttu-id="2b2ef-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b2ef-135">NOTES</span></span>
<span data-ttu-id="2b2ef-136">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="2b2ef-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="2b2ef-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b2ef-137">RELATED LINKS</span></span>

[<span data-ttu-id="2b2ef-138">Yeni-Azağ Izleyicisi</span><span class="sxs-lookup"><span data-stu-id="2b2ef-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2b2ef-139">Get-Azağizleyicisi</span><span class="sxs-lookup"><span data-stu-id="2b2ef-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2b2ef-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b2ef-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b2ef-141">Yeni-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2b2ef-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2b2ef-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b2ef-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b2ef-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b2ef-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b2ef-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2b2ef-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2b2ef-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2b2ef-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2b2ef-146">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2b2ef-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2b2ef-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2b2ef-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2b2ef-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2b2ef-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2b2ef-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2b2ef-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
