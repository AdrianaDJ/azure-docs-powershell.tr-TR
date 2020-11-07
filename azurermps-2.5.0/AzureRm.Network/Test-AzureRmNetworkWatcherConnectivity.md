---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/test-azurermnetworkwatcherconnectivity
schema: 2.0.0
ms.openlocfilehash: 55dc2682c4c3e62b42a6a23ac12f93991e4873fc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939055"
---
# <span data-ttu-id="d652c-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d652c-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="d652c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d652c-102">SYNOPSIS</span></span>
<span data-ttu-id="d652c-103">Belirtilen kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d652c-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d652c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d652c-104">SYNTAX</span></span>

### <span data-ttu-id="d652c-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d652c-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d652c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d652c-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d652c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d652c-107">DESCRIPTION</span></span>
<span data-ttu-id="d652c-108">Test-AzureRmNetworkWatcherConnectivity cmdlet 'i, belirli bir kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d652c-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="d652c-109">Kaynak ile hedef arasındaki bağlantı kurulamazsa, cmdlet sorun hakkında ayrıntılı bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="d652c-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="d652c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d652c-110">EXAMPLES</span></span>

### <span data-ttu-id="d652c-111">Örnek 1: bir VM 'den bir Web sitesine ağ Izleyicisi bağlantısını test edin------------------------------</span><span class="sxs-lookup"><span data-stu-id="d652c-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="d652c-112">Bu örnekte, Azure 'daki bir VM 'den www.bing.com 'e bağlantıyı test ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="d652c-112">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="d652c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d652c-113">PARAMETERS</span></span>

### <span data-ttu-id="d652c-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="d652c-114">-AsJob</span></span>
<span data-ttu-id="d652c-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d652c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d652c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d652c-116">-DefaultProfile</span></span>
<span data-ttu-id="d652c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d652c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d652c-118">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="d652c-118">-DestinationAddress</span></span>
<span data-ttu-id="d652c-119">Bir bağlantı girişiminin gerçekleştirildiği kaynağın IP adresi veya URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="d652c-119">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652c-120">-Destinationıd</span><span class="sxs-lookup"><span data-stu-id="d652c-120">-DestinationId</span></span>
<span data-ttu-id="d652c-121">Bağlantı girişiminin gerçekleştirildiği kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d652c-121">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652c-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="d652c-122">-DestinationPort</span></span>
<span data-ttu-id="d652c-123">Denetim bağlantısının gerçekleştirileceği bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="d652c-123">Port on which check connectivity will be performed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d652c-124">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d652c-124">-NetworkWatcher</span></span>
<span data-ttu-id="d652c-125">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="d652c-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="d652c-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d652c-126">-NetworkWatcherName</span></span>
<span data-ttu-id="d652c-127">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="d652c-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d652c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d652c-128">-ResourceGroupName</span></span>
<span data-ttu-id="d652c-129">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d652c-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d652c-130">-SourceID</span><span class="sxs-lookup"><span data-stu-id="d652c-130">-SourceId</span></span>
<span data-ttu-id="d652c-131">Bağlantı denetiminin başlatılacağı kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="d652c-131">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="d652c-132">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="d652c-132">-SourcePort</span></span>
<span data-ttu-id="d652c-133">Bağlantı denetiminin gerçekleştirileceği kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="d652c-133">The source port from which a connectivity check will be performed.</span></span>

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

### <span data-ttu-id="d652c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d652c-134">CommonParameters</span></span>
<span data-ttu-id="d652c-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d652c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d652c-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d652c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d652c-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d652c-137">INPUTS</span></span>

### <span data-ttu-id="d652c-138">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="d652c-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d652c-139">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="d652c-139">System.String System.Int32</span></span>

## <span data-ttu-id="d652c-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d652c-140">OUTPUTS</span></span>

### <span data-ttu-id="d652c-141">Microsoft. Azure. Commands. Network. model. Psconnectivityınformation</span><span class="sxs-lookup"><span data-stu-id="d652c-141">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="d652c-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d652c-142">NOTES</span></span>
<span data-ttu-id="d652c-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="d652c-143">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="d652c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d652c-144">RELATED LINKS</span></span>

<span data-ttu-id="d652c-145">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="d652c-145">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="d652c-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="d652c-146">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="d652c-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="d652c-147">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
