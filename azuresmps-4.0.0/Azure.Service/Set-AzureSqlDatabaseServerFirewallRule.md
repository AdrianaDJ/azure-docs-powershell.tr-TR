---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F311A7A9-5FE9-4E81-8FF1-8E3A02F2BF4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce9d384a5dd7f57fb4444fb173864ec5859b3a81
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105863"
---
# Set-AzureSqlDatabaseServerFirewallRule

## SYNOPSIS
Azure SQL veritabanı sunucusunda varolan bir güvenlik duvarı kuralını değiştirir.

## INDEKI

```
Set-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-azures, Databaseserverfirewallrule** cmdlet 'i, BELIRTILEN Azure SQL veritabanı sunucusu örneğindeki varolan güvenlik DUVARıNıN başlangıç IP adresini ve bitiş IP adresi değerlerini değiştirir.

## ÖRNEKLERDEN

### Örnek 1: güvenlik duvarı kuralını değiştirme
```
PS C:\> Set-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.2 -EndIpAddress 10.1.1.4
```

Bu komut, lpqd0zbr8y adlı Azure SQL veritabanı sunucusunda FirewallRule24 adındaki güvenlik duvarı kuralının başlangıç IP adresini ve bitiş IP adresini değiştirir.

## PARAMETRELERINE

### -Endıadaddress
Bu kuralın IP adresi aralığının bitiş değerini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleName
Bu cmdlet 'in değiştirdiği güvenlik duvarı kuralının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Sunucunun adını belirtir.
Bu cmdlet, bu cmdlet 'in belirttiği sunucuda bir güvenlik duvarı kuralı oluşturur.
Tam DNS adını değil, sunucu adını belirtin.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Startıpaddress
Güvenlik duvarı kuralının IP adresi aralığının başlangıç değerini belirtir.

```yaml
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
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

### Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerFirewallRuleContext

## ÇıKıŞLAR

### Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerFirewallRuleContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Güvenlik duvarı kuralı ayarlama](https://msdn.microsoft.com/en-us/library/azure/dn505707.aspx)

[Get-Azuressqldatabaseserverfirewallrule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[New-Azuressqldatabaseserverfirewallrule](./New-AzureSqlDatabaseServerFirewallRule.md)

[Remove-Azuressqldatabaseserverfirewallrule](./Remove-AzureSqlDatabaseServerFirewallRule.md)


