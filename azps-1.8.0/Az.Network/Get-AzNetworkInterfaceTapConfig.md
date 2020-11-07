---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: d8e9eda6c6507974376dc35e80a30669bd940153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760541"
---
# Get-AzNetworkInterfaceTapConfig

## SYNOPSIS
Bir dokunuş yapılandırma kaynağını alır.

## INDEKI

### GetByNameParameterSet (varsayılan)
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Getbyresourceıdparameterset
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Get-Aznetworkınterfacetapconfig** cmdlet 'i, belirli bir kaynak grubu Için bir Azure dokunma yapılandırması alır, bir kaynak grubunda ve ağ arabiriminde, yapılandırma adına veya dokunun yapılandırmasına dokunun.

## ÖRNEKLERDEN

### Örnek 1: belirli bir ağ arabiriminin tüm dokunma yapılandırmalarını alma
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

Bu komut, verilen ağ arabirimine eklenecek yapılandırmalara dokunun.

### Örnek 2: belirli bir dokunma yapılandırmasını alma
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

Bu komut, belirli bir ağ arabirimine belirli dokunuş yapılandırmasını getirir.

### Örnek 3: belirli bir dokunma yapılandırmasını alma
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

Bu komut, verilen ağ arabirimine "tapconfig" ile başlayan ad ile birlikte verilen yapılandırmalara dokunun.

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

### -Ad
Belirli dokunun yapılandırması adı.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Networkınterfacename
Ağ arabirim adı.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
TapConfiguration kaynağının RESOURCEID

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. model. Psnetworkınterfacetapconfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Aznetworkınterfacetapconfig](./Add-AzNetworkInterfaceTapConfig.md)

[Remove-Aznetworkınterfacetapconfig](./Remove-AzNetworkInterfaceTapConfig.md)

[Set-Aznetworkınterfacetapconfig](./Set-AzNetworkInterfaceTapConfig.md)
