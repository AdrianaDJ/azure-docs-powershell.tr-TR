---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmssipconfig
schema: 2.0.0
ms.openlocfilehash: 82c27b6f8f926d273948bdfcb519a10ee1e0a3c7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939776"
---
# New-AzureRmVmssIpConfig

## SYNOPSIS
Bir VMSS ağ arabirimi için bir IP yapılandırması oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-AzureRmVmssIpConfig** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) ağ arabirimi IÇIN bir IP yapılandırması nesnesi oluşturur.
Bu cmdlet 'teki yapılandırmayı Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet 'inin *IP* yapılandırması parametresi olarak belirtin.

## ÖRNEKLERDEN

### Örnek 1: bir VMSS arabirimi için IP yapılandırma nesnesi oluşturma
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

Bu komut, ContosoVmssInterface02 adlı bir IP yapılandırma nesnesi oluşturur.
Komut, $SubnetId depolanan önceden tanımlanmış bir alt ağ KIMLIĞINI kullanır.
Komut $IPConfiguration değişkeninde, daha sonra **Add-Azurermvmssnetworkınterfaceconfiguration** ile kullanmak için yapılandırma ayarlarını depolar.

### Örnek 2: NAT havuz ayarlarını içeren bir IP yapılandırma nesnesi oluşturma
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

Bu komut ContosoVmssInterface03 adlı bir IP yapılandırma nesnesi oluşturur ve daha sonra kullanmak üzere $IPConfiguration değişkeninde depolar.
Komut, $SubnetId depolanan önceden tanımlanmış bir alt ağ KIMLIĞINI kullanır.
Komut, $IPConfiguration değişkeninde yapılandırma ayarlarını daha sonra kullanmak üzere depolar.
Komut, *Loadbalancerınboundnatpoolsid* ve *Loadbalancerbackendaddresspoolsid* parametrelerinin değerlerini belirtir.

## PARAMETRELERINE

### -ApplicationGatewayBackendAddressPoolsId
Yük dengeleyicilerde arka uç adres havuzlarına başvurular dizisi belirtir.
Ölçek kümesi, genel ve bir iç yük dengeleyicinin arka uç adres havuzlarına başvurabilir.
Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -DnsSetting
Publicıp adreslerine uygulanacak DNS ayarları.
Publicıp adreslerine uygulanacak DNS ayarlarının etki alanı adı etiketi.
Etki alanı adı etiketi ve VM dizinini birleştirme, oluşturulacak genel IP adresi kaynaklarının etki alanı adı etiketlerdir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Bir KIMLIK belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LoadBalancerBackendAddressPoolsId
Yük dengeleyicileri gelen ağ adresi çevirisi (NAT) havuzlarına başvurular dizisini belirtir.
Ölçek kümesi, genel ve bir iç yük dengeleyicinin gelen NAT havuzlarına başvurabilir.
Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Loadbalancerınboundnatpoolsid
Yük dengeleyicilerde gelen NAT havuzlarına başvuru dizisini belirtir.
Ölçek kümesi, genel ve bir iç yük dengeleyicinin gelen NAT havuzlarına başvurabilir.
Birden çok ölçek kümesi aynı yük dengeleyiciyi kullanamaz.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
IP yapılandırmasının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Birincil
Ağ arabiriminin birden fazla IP yapılandırması olması durumunda birincil IP yapılandırmasını belirtir.

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

### -PrivateIPAddressVersion
IP yapılandırmasını IPv4 veya IPv6 olarak belirtin. Varsayılan olarak IPv4 alınır.  Olası değerler: ' IPv4 ' ve ' IPv6 '.

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

### -Publicipadresconfigurationıdintimeout ınminutes
Genel IP adresinin Boşta durma zaman aşımı.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publicıpaddressconfigurationname
Publicıp adresi yapılandırma adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetId
Yapılandırmanın, VMSS ağ arabirimini oluşturduğu alt ağ KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIPConfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermvmssnetworkınterfaceconfiguration](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


