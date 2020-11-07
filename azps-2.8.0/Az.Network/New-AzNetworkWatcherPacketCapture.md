---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b67d393f0ab24fff15da14b9ce6f6fb1b567d0b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918223"
---
# New-AzNetworkWatcherPacketCapture

## SYNOPSIS
Yeni bir paket yakalama kaynağı oluşturur ve bir VM 'de paket yakalama oturumu başlatır.

## INDEKI

### SetByResource (varsayılan)
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByLocation
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
New-AzNetworkWatcherPacketCapture cmdlet 'i yeni bir paket yakalama kaynağı oluşturur ve bir VM 'de paket yakalama oturumu başlatır.
Paket yakalama oturumlarının uzunluğu, bir zaman kısıtlaması veya boyut kısıtlaması aracılığıyla yapılandırılabilir. Her paket için yakalanan verilerin miktarı da yapılandırılabilir.
Filtreler belirli bir paket yakalama oturumuna uygulanabilir ve bu da yakalanan paketlerin türünü özelleştirmenize olanak tanır. Süzgeçler, yerel ve uzak IP adresleri & adres aralıkları, yerel ve uzak bağlantı noktaları & bağlantı noktası aralıklarını ve oturum düzeyi iletişim kuralını da kısıtlayabilir. Filtreler birleştirilebilir ve size birden çok filtre uygulamak için çok sayıda filtre uygulayabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: birden çok filtre içeren bir paket yakalama oluşturma
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

Bu örnekte, birden çok filtre ve zaman sınırı içeren "PacketCaptureTest" adlı bir paket yakalama oluşturalım. Oturum tamamlandığında, belirtilen depolama hesabına kaydedilir. Not: paket yakalamaları oluşturmak için hedef sanal makinede Azure ağ Izleyicisi uzantısı yüklü olmalıdır.

## PARAMETRELERINE

### -Iş
Arka planda cmdlet 'i çalıştırın

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BytesToCapturePerPacket
Paket başına yakalanacak baytlar.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filtre
Paket yakalama oturumu için filtreler.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalFilePath
Yerel dosya yolu.

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

### -Konum
Ağ İzleyicisi 'nin konumu.

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Networkizleyicisi
Ağ İzleyicisi kaynağı.

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

### -NetworkWatcherName
Ağ İzleyicisi 'nin adı.

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

### -PacketCaptureName
Paket yakalama adı.

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

### -ResourceGroupName
Ağ İzleyicisi kaynak grubunun adı.

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

### -Storageaccountıd
Depolama hesabı kimliği.

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

### -StoragePath
Depolama yolu.

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

### -Targetvirtualmachineıd
Hedef sanal makine KIMLIĞI.

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

### -Timelimitınseconds
Saniye cinsinden zaman sınırı.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TotalBytesPerSession
Oturum başına toplam bayt sayısı.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

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

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. model. Psnetworkizleyicisi

### System. String

### System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSPacketCaptureResult

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, ağ, ağ, Ağ İzleyicisi, paket, yakalama, trafik 

## ILGILI BAĞLANTıLAR

[Yeni-Azağ Izleyicisi](./New-AzNetworkWatcher.md)

[Get-Azağizleyicisi](./Get-AzNetworkWatcher.md)

[Remove-Aznetworkizleyicisi](./Remove-AzNetworkWatcher.md)

[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)

[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)

[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)

[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)

[Yeni-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)

[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)

[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)

[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)

[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)

[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)

[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)

[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)

[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)

[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)

[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)

[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)

[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)

[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)

[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)

[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)

[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport)

[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor)


