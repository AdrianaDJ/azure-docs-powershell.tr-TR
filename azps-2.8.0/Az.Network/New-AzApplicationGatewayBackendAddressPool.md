---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 1165d7abccdbf21dc94e4f39b8b2dad953fdba07
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918364"
---
# New-AzApplicationGatewayBackendAddressPool

## SYNOPSIS
Uygulama ağ geçidi için arka uç adres havuzu oluşturur.

## INDEKI

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Yeni-AzApplicationGatewayBackendAddressPool** cmdlet 'ı bir Azure uygulama ağ geçidi için arka uç adres havuzu oluşturur.
Arka uç adresi, IP adresi, tam nitelikli etki alanı adı (FQDN) veya IP yapılandırma KIMLIĞI olarak belirtilebilir.

## ÖRNEKLERDEN

### Örnek 1: arka uç sunucusunun FQDN 'sini kullanarak arka uç adres havuzu oluşturma
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

Bu komut, arka uç sunucuların FQDN 'lerini kullanarak Pool01 adlı bir arka uç adres havuzu oluşturur ve $Pool değişkeninde depolar.

### Örnek 2: arka uç sunucusunun IP adresini kullanarak arka uç adres havuzu oluşturma
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

Bu komut, arka uç sunucuların IP adreslerini kullanarak Pool02 adlı bir arka uç adres havuzu oluşturur ve $Pool değişkeninde depolar.

## PARAMETRELERINE

### -Backendfqdn 'leri
Bu cmdlet 'in arka uç sunucu havuzuyla ilişki kurduğu arka uç FQDN 'lerin listesini belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Backentüm adresler
Bu cmdlet 'in arka uç sunucu havuzuyla ilişki kurduğu arka uç IP adresleri listesini belirtir.

```yaml
Type: System.String[]
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

### -Ad
Bu cmdlet 'in oluşturduğu arka uç sunucu havuzunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendAddressPool

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzApplicationGatewayBackendAddressPool](./Add-AzApplicationGatewayBackendAddressPool.md)

[Get-AzApplicationGatewayBackendAddressPool](./Get-AzApplicationGatewayBackendAddressPool.md)

[Remove-AzApplicationGatewayBackendAddressPool](./Remove-AzApplicationGatewayBackendAddressPool.md)

[Set-AzApplicationGatewayBackendAddressPool](./Set-AzApplicationGatewayBackendAddressPool.md)


