---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105864"
---
# Set-AzureSqlDatabaseServer

## SYNOPSIS
Azure SQL veritabanı sunucusunun özelliklerini değiştirir.

## INDEKI

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-Azuressqldatabaseserver** cmdlet 'i, BELIRTILEN Azure SQL veritabanı sunucusu örneğinin özelliklerini değiştirir.
Geçerli sürümde, yalnızca sunucunun yönetici hesabı parolasını güncelleştirebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: sunucunun parolasını değiştirme
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

Bu komut, lpqd0zbr8y adlı Azure SQL veritabanı sunucusu için yönetici hesabı parolasını değiştirir.

## PARAMETRELERINE

### -AdminPassword
Azure SQL veritabanı sunucusu için yönetici hesabı parolasını belirtir.
Güçlü bir parola belirtmelisiniz.
Daha fazla bilgi [için bkz](https://go.microsoft.com/fwlink/p/?LinkId=154152) https://go.microsoft.com/fwlink/p/?LinkId=154152) .

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

### -ServerName
Bu cmdlet 'in değiştirdiği sunucunun adını belirtir.
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

### Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqldatabaseserver](./Get-AzureSqlDatabaseServer.md)

[New-Azuressqldatabaseserver](./New-AzureSqlDatabaseServer.md)

[Remove-Azuressqldatabaseserver](./Remove-AzureSqlDatabaseServer.md)


