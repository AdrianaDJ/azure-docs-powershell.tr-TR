---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: 3c69884e988b10f41da4d41d98318ee96c019112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594859"
---
# New-AzureRmPacketCaptureFilterConfig

## SYNOPSIS
Yeni bir paket yakalama filtresi nesnesi oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
New-AzureRmPacketCaptureFilterConfig cmdlet 'i yeni bir paket yakalama filtresi nesnesi oluşturur. Bu nesne, belirtilen ölçütleri kullanarak paket yakalama oturumu sırasında yakalanan paketlerin türünü sınırlandırmak için kullanılır. New-AzureRmNetworkWatcherPacketCapture cmdlet, birleştirilebilir yakalama oturumlarını etkinleştirmek için birden çok filtre nesnesi kabul edebilir.

## ÖRNEKLERDEN

### Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım. Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir. Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -LocalIPAddress
Filtre uygulanacak yerel IP adresini belirtir.
Örnek girişler: tek bir adres girişi için "127.0.0.1".
Aralık için "127.0.0.1-127.0.0.255".
birden çok girdi için "127.0.0.1; 127.0.0.5;".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalPort
Filtre uygulanacak yerel IP adresini belirtir.
Örnek girişler: tek bir adres girişi için "127.0.0.1".
Aralık için "127.0.0.1-127.0.0.255".
birden çok girdi için "127.0.0.1; 127.0.0.5;".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -İletişim kuralı
Filtre uygulanacak procotol belirtir. Kabul edilebilir değerler "TCP", "UDP", "Any"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Remoteıpaddress
Filtre uygulanacak uzak IP adresini belirtir.
Örnek girişler: tek bir adres girişi için "127.0.0.1".
Aralık için "127.0.0.1-127.0.0.255".
birden çok girdi için "127.0.0.1; 127.0.0.5;".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RemotePort
Filtre uygulanacak uzak bağlantı noktasını belirtir.
Uzak bağlantı noktası örnek girişleri: tek çıkışlı girdi için "80".
Aralık için "80-85".
birden çok girdi için "80; 443;".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String
Parametreler: Protocol (ByValue)

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. PSPacketCaptureFilter

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, izleyici, paket, yakalama, trafik, filtre 

## ILGILI BAĞLANTıLAR

[Yeni-Azurermnetworkizleyicisi](./New-AzureRmNetworkWatcher.md)

[Get-Azurermnetworkizleyicisi](./Get-AzureRmNetworkWatcher.md)

[Remove-Azurermnetworkizleyicisi](./Remove-AzureRmNetworkWatcher.md)

[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)

[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)

[Start-AzureRmNetworkWatcherResourceTroubleshooting](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)

[Yeni-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)

[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)

[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[New-AzureRmNetworkWatcherProtocolConfiguration](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[Test-AzureRmNetworkWatcherIPFlow](./Test-AzureRmNetworkWatcherIPFlow.md)

[Test-AzureRmNetworkWatcherConnectivity](./Test-AzureRmNetworkWatcherConnectivity.md)

[Stop-AzureRmNetworkWatcherConnectionMonitor](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[Set-AzureRmNetworkWatcherConnectionMonitor](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[Set-AzureRmNetworkWatcherConfigFlowLog](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[Get-AzureRMNetworkWatcherReachabilityReport](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[Get-AzureRmNetworkWatcherReachabilityProvidersList](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[Get-AzureRmNetworkWatcherFlowLogStatus](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor)
