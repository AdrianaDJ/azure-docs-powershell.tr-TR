---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfig.md
ms.openlocfilehash: 11051c8030fb9a57b84f738ff487b00d6652749c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278555"
---
# New-AzContainerNicConfig

## SYNOPSIS
Yeni bir kapsayıcı ağ arabirimi yapılandırma nesnesi oluşturur.

## INDEKI

```
New-AzContainerNicConfig [-Name <String>] [-IpConfiguration <PSIPConfigurationProfile[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Yeni-AzContainerNicConfig** cmdlet 'i yeni bir kapsayıcı ağ arabirimi yapılandırma nesnesi oluşturur. Bu nesne, üst ağ profiline başvuruda bulunan kapsayıcı ağ arabiriminin özelliklerini belirler.

## ÖRNEKLERDEN

### Örnek 1
```powershell
$containerNicConfig = New-AzContainerNicConfig -Name cnicConfig1

$networkProfile = New-AzNetworkProfile -Name np1 -ResourceGroupName rg1 -Location westus -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

İlk komut boş bir konteyner ağı arabirim yapılandırması oluşturur. İkincisi, önceden oluşturulmuş kapsayıcı ağı arabirim yapılandırmasını bağımsız değişken olarak New-NetworkProfile cmdlet 'ine geçirerek yeni bir ağ profili oluşturur.

### Örnek 2

Yeni bir kapsayıcı ağ arabirimi yapılandırma nesnesi oluşturur. oluşturulmuş

<!-- Aladdin Generated Example -->
```powershell
New-AzContainerNicConfig -IpConfiguration <PSIPConfigurationProfile[]> -Name cnic
```

## PARAMETRELERINE

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

### -IP yapılandırması
Bu kapsayıcıdaki bir kapsayıcı NIC örneği oluşturulduğunda hangi IP yapılandırmalarının oluşturulduğunu belirleyen IP yapılandırma profilleri koleksiyonu

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIPConfigurationProfile[]
Parameter Sets: (All)
Aliases: IpConfig

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Kapsayıcı ağ arabirimi yapılandırmasının adı.

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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. model. PSIPConfigurationProfile []

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Pscontainernetworkınterfaceconfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azcontainernicconfigıconfig](./New-AzContainerNicConfigIpConfig.md)
