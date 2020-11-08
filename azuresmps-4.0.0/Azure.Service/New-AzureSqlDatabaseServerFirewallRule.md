---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105969"
---
# New-AzureSqlDatabaseServerFirewallRule

## SYNOPSIS
Azure SQL veritabanı sunucusunda bir güvenlik duvarı kuralı oluşturur.

## INDEKI

### IpRange (varsayılan)
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AllowAllAzureServices
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-Azuressqldatabaseserverfirewallrule** cmdlet 'i, geçerli abonelikte BELIRTILEN Azure SQL veritabanı sunucusu örneğinde bir güvenlik duvarı kuralı oluşturur.

Bu kuralın Azure SQL veritabanı sunucusuna bağlanmasına izin verdiği IP adresi aralığını belirtmek için *Startıpaddress* ve *endıadaddress* parametrelerini kullanın.

Sunucuya Azure bağlantılarının izin verdiği bir kural oluşturmak için *AllowAllAzureServices* parametresini belirtin.
Kural, 0.0.0.0 olan IP adresi değerlerini başlatıyor ve bitiyor.
Bir güvenlik duvarı kuralı adı belirtmezseniz, bu cmdlet varsayılan ad AllowAllAzureServices.

## ÖRNEKLERDEN

### Örnek 1: güvenlik duvarı kuralı oluşturma
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

Bu komut, lpqd0zbr8y adlı Azure SQL veritabanı sunucusunda bir güvenlik duvarı kuralı FirewallRule24 oluşturur.
Komut bir IP adresi aralığı belirtir.

### Örnek 2: tüm Azure hizmetlerinin bulunduğu bir kural oluşturma
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

Bu komut, Azure bağlantılarına izin veren lpqd0zbr8y adındaki sunucuda AzureConnections adlı bir güvenlik duvarı kuralı oluşturur.

### Örnek 3: varsayılan adı kullanan tüm Azure hizmetlerinin, varsayılan adı kullanan tüm Azure hizmetlerinin
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

Bu komut, Azure bağlantılarına izin veren lpqd0zbr8y adlı belirtilen sunucuda bir güvenlik duvarı kuralı oluşturur.
Komut AllowAllAzureServices varsayılan kural adını atar.

## PARAMETRELERINE

### -AllowAllAzureServices
Bu güvenlik duvarı kuralının tüm Azure IP adreslerinin sunucuya erişmesini etkinleştirdiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endıadaddress
Bu kuralın IP adresi aralığının bitiş değerini belirtir.

```yaml
Type: String
Parameter Sets: IpRange
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
Yeni güvenlik duvarı kuralının adını belirtir.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Parameter Sets: IpRange
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

## ÇıKıŞLAR

### Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerFirewallRuleContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Güvenlik duvarı kuralı oluşturma](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqldatabaseserverfirewallrule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[Remove-Azuressqldatabaseserverfirewallrule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-Azuressqldatabaseserverfirewallrule](./Set-AzureSqlDatabaseServerFirewallRule.md)


