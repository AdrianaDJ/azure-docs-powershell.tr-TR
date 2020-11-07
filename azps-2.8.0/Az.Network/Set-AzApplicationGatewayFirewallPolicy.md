---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917960"
---
# Set-AzApplicationGatewayFirewallPolicy

## SYNOPSIS
Uygulama ağ geçidi güvenlik ilkesini güncelleştirir.

## INDEKI

### ByFactoryObject (varsayılan)
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFactoryName
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Byresourceıd
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Set-AzApplicationGatewayFirewallPolicy** cmdlet 'i, bir Azure uygulama ağ geçidi güvenlik duvarı ilkesini güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

Bu komut, uygulama ağ geçidi güvenlik ilkesini $AppGwFirewallPolicy değişkeninde ayarlarla güncelleştirir ve güncelleştirilmiş ağ geçidini $UpdatedAppGwFirewallPolicy değişkeninde depolar.

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

### -CustomRule
CustomRules listesi

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
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

### -InputObject
ApplicationGatewayFirewallPolicy

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Güvenlik Duvarı Ilke adı.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Azure Resource ID.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayWebApplicationFirewallPolicy

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
