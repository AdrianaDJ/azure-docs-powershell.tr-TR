---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105572"
---
# Get-AzureSqlDatabaseServerFirewallRule

## SYNOPSIS
Azure SQL veritabanı sunucusu için güvenlik duvarı kurallarını alır.

## INDEKI

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-azures, Databaseserverfirewallrule** cmdlet 'i, BIR Azure SQL veritabanı sunucusu örneği için güvenlik duvarı kurallarını alır.
Bir güvenlik duvarı kuralı adı belirtirseniz, bu cmdlet bu güvenlik duvarı kuralı hakkındaki bilgileri döndürür.
Aksi halde cmdlet, belirtilen Azure SQL veritabanı sunucusundaki tüm güvenlik duvarı kuralları hakkında bilgi döndürür.

## ÖRNEKLERDEN

### Örnek 1: sunucudaki tüm güvenlik duvarı kurallarını alma
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

Bu komut, lpqd0zbr8y adındaki Azure SQL veritabanı sunucusunda tüm güvenlik duvarı kurallarını alır.

### Örnek 2: adını kullanarak bir güvenlik duvarı kuralı alma
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

Bu komut, lpqd0zbr8y adındaki sunucudaki FirewallRule24 adındaki güvenlik duvarı kuralını alır.

## PARAMETRELERINE

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
Bu cmdlet 'in aldığı güvenlik duvarının adını belirtir.

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

### -ServerName
Sunucunun adını belirtir.
Bu cmdlet, bu parametrenin belirttiği sunucudan güvenlik duvarı kurallarını alır.
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerFirewallRuleContext

## ÇıKıŞLAR

### 'A\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Güvenlik duvarı kurallarını Listele](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[New-Azuressqldatabaseserverfirewallrule](./New-AzureSqlDatabaseServerFirewallRule.md)

[Remove-Azuressqldatabaseserverfirewallrule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-Azuressqldatabaseserverfirewallrule](./Set-AzureSqlDatabaseServerFirewallRule.md)


