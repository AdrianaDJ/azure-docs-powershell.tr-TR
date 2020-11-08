---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A0C674FC-A1D8-4068-8CAB-2EE0AECB8E68
online version: ''
schema: 2.0.0
ms.openlocfilehash: 069b96809c0659028135e8c9a28e7e3c0ab8b3ae
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105971"
---
# New-AzureSqlDatabaseServer

## SYNOPSIS
Azure SQL veritabanı sunucusu oluşturur.

## INDEKI

```
New-AzureSqlDatabaseServer -AdministratorLogin <String> -AdministratorLoginPassword <String> -Location <String>
 [-Version <Single>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-Azuressqldatabaseserver** cmdlet 'i geçerli ABONELIKTE Azure SQL veritabanı sunucusu örneği oluşturur.

## ÖRNEKLERDEN

### Örnek 1: sunucu oluşturma
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword"
```

Bu komut, bir sürüm 11 Azure SQL veritabanı sunucusu oluşturur.

### Örnek 2: sürüm 12 sunucusu oluşturma
```
PS C:\>New-AzureSqlDatabaseServer -Location "East US" -AdministratorLogin "AdminLogin" -AdministratorLoginPassword "AdminPassword" -Version "12.0"
```

Bu komut 12 sunucusu oluşturur.

## PARAMETRELERINE

### -\Administrators oturum açma
Yeni Azure SQL veritabanı sunucusu için yönetici hesap adını belirtir.

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

### -\Administrators
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

### -Konum
Bu cmdlet 'in sunucuyu oluşturduğu veri merkezinin konumunu belirtir.
Daha fazla bilgi için bkz: [Azure](https://azure.microsoft.com/regions/) https://azure.microsoft.com/regions/#services) Library.

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

### -Version
Yeni sunucunun sürümünü belirtir.
Geçerli değerler: 2,0 ve 12,0.

```yaml
Type: Single
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

### Microsoft. Windowsazve. Commands. SqlDatabase. model. SqlDatabaseServerContext

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Sunucu oluşturma](https://msdn.microsoft.com/en-us/library/azure/dn505699.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqldatabaseserver](./Get-AzureSqlDatabaseServer.md)

[Remove-Azuressqldatabaseserver](./Remove-AzureSqlDatabaseServer.md)

[Set-Azuressqldatabaseserver](./Set-AzureSqlDatabaseServer.md)


