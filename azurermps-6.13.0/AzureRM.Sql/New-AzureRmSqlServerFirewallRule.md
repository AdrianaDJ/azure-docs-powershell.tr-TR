---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e5d835d0dbe31728a0b524c95b4473a94bb42a20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587137"
---
# New-AzureRmSqlServerFirewallRule

## SYNOPSIS
SQL veritabanı sunucusu için bir güvenlik duvarı kuralı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Kullanıcı Belirtilmediruleset
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AzureIpRuleSet
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmSqlServerFirewallRule** cmdlet 'ı BELIRTILEN Azure SQL veritabanı sunucusu için bir güvenlik duvarı kuralı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: güvenlik duvarı kuralı oluşturma
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

Bu komut, server01 adlı sunucuda Rule01 adlı bir güvenlik duvarı kuralı oluşturur.
Kural, belirtilen başlangıç ve bitiş IP adreslerini içerir.

### Örnek 2: tüm Azure IP adreslerinin sunucuya erişmesine izin veren bir güvenlik duvarı kuralı oluşturma
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

Bu komut, ResourceGroup01 adındaki kaynak grubuna ait server01 adındaki sunucuda bir güvenlik duvarı kuralı oluşturur.
*AllowAllAzureIPs* parametresi kullanıldığından, güvenlik duvarı kuralı tüm Azure IP adreslerinin sunucuya erişmesini sağlar.

## PARAMETRELERINE

### -AllowAllAzureIPs
Bu güvenlik duvarı kuralının tüm Azure IP adreslerinin sunucuya erişmesine izin verdiğini gösterir.
*Firewallrulename* , *Startıpaddress* ve *endıda adres* parametrelerini kullanmayı düşünüyorsanız bu parametreyi kullanamazsınız.
Azure IP 'Lerin sunucuya erişmesine izin vermek istiyorsanız, bu parametre *Firewallrulename* , *Startıpaddress* ve *endıveraddress* parametrelerini kullanmayan ayrı bir cmdlet çağrısında kullanılmalıdır.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Endıadaddress
Bu kuralın IP adresi aralığının bitiş değerini belirtir.

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallRuleName
Yeni güvenlik duvarı kuralının adını belirtir.

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Sunucunun atandığı kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Sunucunun adını belirtir.
Tam DNS adını değil, sunucu adını belirtin.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Startıpaddress
Güvenlik duvarı kuralının IP adresi aralığının başlangıç değerini belirtir.

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
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

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. FirewallRule. model. Azuressqlserverfirewallrulemodel

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmSqlServerFirewallRule](./Get-AzureRmSqlServerFirewallRule.md)

[Remove-AzureRmSqlServerFirewallRule](./Remove-AzureRmSqlServerFirewallRule.md)

[Set-AzureRmSqlServerFirewallRule](./Set-AzureRmSqlServerFirewallRule.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)


