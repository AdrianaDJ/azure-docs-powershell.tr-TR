---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764619"
---
# Get-AzureRmFirewall

## SYNOPSIS
Bir Azure Güvenlik Duvarı alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureRmFirewall** cmdlet 'i bir kaynak grubunda bir veya daha fazla güvenlik duvarını alır.

## ÖRNEKLERDEN

### 1: kaynak grubundaki tüm güvenlik duvarlarını alma
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

Bu örnekte, "rgName" kaynak grubundaki tüm güvenlik duvarları alınır.

### 2: ada göre bir güvenlik duvarı alma
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

Bu örnekte, "rgName" kaynak grubunda "azFw" adlı güvenlik duvarı alınır.

### 3: güvenlik duvarı alın ve güvenlik duvarına uygulama kuralı koleksiyonu ekleyin
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

Bu örnek bir güvenlik duvarı alır ve güvenlik duvarına bir uygulama kuralı koleksiyonu ekleyerek AddApplicationRuleCollection metodunu çağırarak.

### 4: güvenlik duvarı alın ve güvenlik duvarına bir ağ kuralı koleksiyonu ekleyin
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

Bu örnek bir güvenlik duvarı alır ve ardından AddNetworkRuleCollection metodunu çağırarak güvenlik duvarına bir ağ kuralı koleksiyonu ekler.

### 5: güvenlik duvarı alın ve güvenlik duvarından ada göre uygulama kuralı koleksiyonunu geri alın
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

Bu örnekte, bir güvenlik duvarı alınır ve ardından, güvenlik duvarı nesnesinde GetApplicationRuleCollectionByName metodunu çağıran bir kural koleksiyonunu ada göre alır. GetApplicationRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.

### 6: güvenlik duvarı alın ve güvenlik duvarından bir ağ kuralı koleksiyonunu ada göre geri alın
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

Bu örnekte bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre alır GetNetworkRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.

### 7: güvenlik duvarını alın ve güvenlik duvarından bir uygulama kuralı koleksiyonunu ada göre kaldırın
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

Bu örnekte bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre kaldırır RemoveApplicationRuleCollectionByName metodunun kural koleksiyonu adı büyük/küçük harf duyarlı değildir.

### 8: güvenlik duvarı alın ve güvenlik duvarından ada göre bir ağ kuralı koleksiyonunu kaldırın
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

Bu örnekte, bir güvenlik duvarı ve ardından bir kural koleksiyonunu ada göre kaldırır Yöntem RemoveNetworkRuleCollectionByName için kural koleksiyonu adı büyük/küçük harf duyarlı değildir.

### 9: güvenlik duvarını alın ve güvenlik duvarını ayırın
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

Bu örnekte, güvenlik duvarındaki güvenlik duvarı ve çağrı çağrıları, güvenlik duvarıyla ilişkili yapılandırmayı (uygulama ve ağ kuralı koleksiyonlarını) kullanarak güvenlik duvarı hizmetini başlatacak şekilde alınır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Ad
Bu cmdlet 'in aldığı güvenlik duvarının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Güvenlik duvarının ait olduğu kaynak grubunun adını belirtir.

```yaml
Type: String
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSAzureFirewall

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
