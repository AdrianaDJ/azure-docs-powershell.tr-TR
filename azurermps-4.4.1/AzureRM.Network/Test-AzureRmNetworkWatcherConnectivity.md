---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherConnectivity.md
ms.openlocfilehash: 4e9c99f2985be335f2750e500ee0c01394195c39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764256"
---
# <span data-ttu-id="58538-101">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="58538-101">Test-AzureRmNetworkWatcherConnectivity</span></span>

## <span data-ttu-id="58538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58538-102">SYNOPSIS</span></span>
<span data-ttu-id="58538-103">Belirtilen kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="58538-103">Returns connectivity information for a specified source VM and a destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58538-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58538-104">SYNTAX</span></span>

### <span data-ttu-id="58538-105">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58538-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcher <PSNetworkWatcher> -SourceId <String>
 [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58538-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="58538-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherConnectivity -NetworkWatcherName <String> -ResourceGroupName <String>
 -SourceId <String> [-SourcePort <Int32>] [-DestinationId <String>] [-DestinationAddress <String>]
 [-DestinationPort <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58538-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="58538-107">DESCRIPTION</span></span>
<span data-ttu-id="58538-108">Test-AzureRmNetworkWatcherConnectivity cmdlet 'i, belirli bir kaynak VM ve bir hedefin bağlantı bilgilerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="58538-108">The Test-AzureRmNetworkWatcherConnectivity cmdlet returns connectivity information for a specified source VM and a destination.</span></span> <span data-ttu-id="58538-109">Kaynak ile hedef arasındaki bağlantı kurulamazsa, cmdlet sorun hakkında ayrıntılı bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="58538-109">If connectivity between the source and destination cannot be established, the cmdlet returns details about the issue.</span></span>

## <span data-ttu-id="58538-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58538-110">EXAMPLES</span></span>

### <span data-ttu-id="58538-111">Örnek 1: bir VM 'den bir Web sitesine ağ Izleyicisi bağlantısını test edin------------------------------</span><span class="sxs-lookup"><span data-stu-id="58538-111">---------------  Example 1: Test Network Watcher Connectivity from a VM to a website  ---------------</span></span>
<span data-ttu-id="58538-112">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="58538-112">@{paragraph=PS C:\\\>}</span></span>










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

<span data-ttu-id="58538-113">Bu örnekte, Azure 'daki bir VM 'den www.bing.com 'e bağlantıyı test ediyoruz.</span><span class="sxs-lookup"><span data-stu-id="58538-113">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="58538-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58538-114">PARAMETERS</span></span>

### <span data-ttu-id="58538-115">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="58538-115">-DestinationAddress</span></span>
<span data-ttu-id="58538-116">Bir bağlantı girişiminin gerçekleştirildiği kaynağın IP adresi veya URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="58538-116">The IP address or URI the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58538-117">-Destinationıd</span><span class="sxs-lookup"><span data-stu-id="58538-117">-DestinationId</span></span>
<span data-ttu-id="58538-118">Bağlantı girişiminin gerçekleştirildiği kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="58538-118">The ID of the resource to which a connection attempt will be made.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58538-119">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="58538-119">-DestinationPort</span></span>
<span data-ttu-id="58538-120">Denetim bağlantısının gerçekleştirileceği bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="58538-120">Port on which check connectivity will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58538-121">-Networkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="58538-121">-NetworkWatcher</span></span>
<span data-ttu-id="58538-122">Ağ İzleyicisi kaynağı.</span><span class="sxs-lookup"><span data-stu-id="58538-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="58538-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="58538-123">-NetworkWatcherName</span></span>
<span data-ttu-id="58538-124">Ağ İzleyicisi 'nin adı.</span><span class="sxs-lookup"><span data-stu-id="58538-124">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58538-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58538-125">-ResourceGroupName</span></span>
<span data-ttu-id="58538-126">Ağ İzleyicisi kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="58538-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="58538-127">-SourceID</span><span class="sxs-lookup"><span data-stu-id="58538-127">-SourceId</span></span>
<span data-ttu-id="58538-128">Bağlantı denetiminin başlatılacağı kaynağın KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="58538-128">The ID of the resource from which a connectivity check will be initiated.</span></span>

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

### <span data-ttu-id="58538-129">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="58538-129">-SourcePort</span></span>
<span data-ttu-id="58538-130">Bağlantı denetiminin gerçekleştirileceği kaynak bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="58538-130">The source port from which a connectivity check will be performed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58538-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58538-131">-DefaultProfile</span></span>
<span data-ttu-id="58538-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58538-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58538-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58538-133">CommonParameters</span></span>
<span data-ttu-id="58538-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58538-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58538-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58538-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58538-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58538-136">INPUTS</span></span>

### <span data-ttu-id="58538-137">Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi</span><span class="sxs-lookup"><span data-stu-id="58538-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="58538-138">System. String System. Int32</span><span class="sxs-lookup"><span data-stu-id="58538-138">System.String System.Int32</span></span>

## <span data-ttu-id="58538-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58538-139">OUTPUTS</span></span>

### <span data-ttu-id="58538-140">Microsoft. Azure. Commands. Network. model. Psconnectivityınformation</span><span class="sxs-lookup"><span data-stu-id="58538-140">Microsoft.Azure.Commands.Network.Models.PSConnectivityInformation</span></span>

## <span data-ttu-id="58538-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58538-141">NOTES</span></span>
<span data-ttu-id="58538-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, bağlanabilirlik, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi</span><span class="sxs-lookup"><span data-stu-id="58538-142">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="58538-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58538-143">RELATED LINKS</span></span>

<span data-ttu-id="58538-144">[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md) 
 [Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md) 
 [Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="58538-144">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="58538-145">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="58538-145">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="58538-146">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="58538-146">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>
