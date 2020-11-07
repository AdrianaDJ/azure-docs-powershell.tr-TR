---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9273c4cf6d23825b931dda696e1a2ef8513aa68d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917896"
---
# Set-AzNetworkInterface

## SYNOPSIS
Ağ arabirimini güncelleştirir.

## INDEKI

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Set-Azağinterface** bir ağ arabirimini güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: ağ arabirimini yapılandırma
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

Bu örnek, ağ arabirimini yapılandırır.
İlk komut NetworkInterface1 adındaki bir ağ arabirimini kaynak grubunda ResourceGroup1 alır.
İkinci komut, IP yapılandırmasının özel IP adresini ayarlar.
Üçüncü komut özel IP ayırma yöntemini statik olarak ayarlar.
Dördüncü komut ağ arabiriminde bir etiket ayarlar.
Beşinci komut, ağ arabirimini ayarlamak için $Nic değişkeninde depolanan bilgileri kullanır.

### Örnek 2: ağ arabirimindeki DNS ayarlarını değiştirme
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

İlk komut NetworkInterface1 adlı bir ağ arabirimini kaynak grubu ResourceGroup1 içinde var. İkinci komut bu arabirime DNS sunucusu 192.168.1.100 ekler. Üçüncü komut, bu değişiklikleri ağ arabiriminde uygular. DNS sunucusunu kaldırmak için yukarıda listelenen, ancak yerine konan komutları izleyin. "With" ekleyin. Remove "komutu

### Örnek 3: ağ arabiriminde IP iletmeyi etkinleştirme
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

İlk komut NetworkInterface1 adındaki mevcut bir ağ arabirimini alır ve $nic değişkeninde depolar. İkinci komut, IP iletme değerini doğru olarak değiştirir. Son olarak, üçüncü komut değişiklikleri ağ arabiriminde uygular. Ağ arabiriminde IP iletmeyi devre dışı bırakmak için örnek örneği izleyin, ancak ikinci komutu "$nic olarak değiştirdiğinizden emin olun. Enableipiletme = 0 ".

### Örnek 4: ağ arabiriminin alt ağını değiştirme
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

İlk komut NetworkInterface1 ağ arabirimini alır ve $nic değişkeninde depolar. İkinci komut, ağ arabiriminin ilişkilendirildiği alt ağla ilişkilendirilmiş sanal ağı alır. İkinci komut, alt ağı alır ve $subnet 2 değişkeninde depolar. Yeni alt ağla ağ arabiriminin birincil özel IP adresini içeren üçüncü komut. Son komut, bu değişiklikleri ağ arabiriminde uyguladı.
>[!NOTE] 
>Alt ağı değiştirebilmeniz için IP yapılandırmalarının dinamik olması gerekir. Statik IP yapılandırmalarınız varsa, devam etmeden önce dinamik olarak değiştirin. 
>[!NOTE]
>Ağ arabiriminin birden çok IP yapılandırması varsa, son Set-AzNetworkInterface komutu yürütülmeden önce ileri komutu tüm bu IP yapılandırmalarında tamamlanmalıdır. Bu, ileri komutunda olduğu gibi, "0" değerini uygun sayıyla değiştirerek yapılabilir. Ağ arabiriminde N IP yapılandırması varsa, bu komutların N-1 olması gerekir.

### Örnek 5: ağ güvenlik grubunu ağ arabirimiyle Ilişkilendirme/Ilişkilendirme
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

İlk komut NetworkInterface1 adındaki mevcut bir ağ arabirimini alır ve $nic değişkeninde depolar. İkinci komut MyNSG adlı varolan bir ağ güvenlik grubunu alır ve $nsg değişkeninde depolar. Üçüncü komut $nsg $nic atar. Son olarak, ileri komutu, değişiklikleri ağ arabiriminde uygular. Ağ güvenliği gruplarının ağ arabiriminden ilişkisini kaldırmak için, üçüncü komutta $null $nsg basit değiştirme 'yi.

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

### -NetworkInterface
Ağ arabiriminin ayarlanması gereken durumu temsil eden bir ağ arabirimi nesnesi belirtir.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[Get-AzNetworkInterface](./Get-AzNetworkInterface.md)

[New-AzNetworkInterface](./New-AzNetworkInterface.md)

[Remove-AzNetworkInterface](./Remove-AzNetworkInterface.md)
