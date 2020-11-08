---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106108"
---
# Remove-AzureSqlDatabase

## SYNOPSIS
Azure SQL veritabanını siler.

## INDEKI

### ByNameWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-Azurestabanı** cmdlet 'i, BIR Azure SQL veritabanını sunucu bağlantısı bağlamı veya sunucu adı ile siler.
**New-Azuressqldatabaseservercontext** cmdlet 'Ini kullanarak Azure SQL veritabanı sunucusu bağlantı bağlamını oluşturabilir ve bu cmdlet ile kullanabilirsiniz.

Bir Azure SQL veritabanı sunucusu adı belirterek bir veritabanını sildiğinizde, **Remove-Azuresurdatabase** cmdlet 'i, işlemi gerçekleştirmek için adı ve geçerli Azure aboneliği bilgilerini kullanır.

## ÖRNEKLERDEN

### Örnek 1: veritabanını kaldırma
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

Bu komut, Database01 adlı veritabanını Azure SQL veritabanı sunucusu bağlantı bağlamı $Context kaldırır.

### Örnek 2: sunucu adı kullanarak veritabanını kaldırma
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

Bu komut, Database01 adlı Azure SQL veritabanı sunucusundan gelen veritabanını kaldırır.

### Örnek 3: ardışık düzeni kullanarak veritabanını kaldırma
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

Bu örnek, ardışık düzen aracılığıyla veritabanı nesnesini geçirmenin alternatif yöntemini gösterir.

## PARAMETRELERINE

### -ConnectionContext
Bu cmdlet 'in veritabanından kaldırıldığı sunucunun bağlantı bağlamını belirtir.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Veritabanı
Bu cmdlet 'in kaldırdığı veritabanını temsil eden bir nesne belirtir.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
Bu cmdlet 'in kaldırdığı veritabanının adını belirtir.

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Eylemin kullanıcıya onay istemeden yapılmasına izin verir.

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
Bu cmdlet 'in veritabanını sildiği sunucunun adını belirtir.

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
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

### Microsoft. Windowsazme. Commands. SqlDatabase. Services. Server. Database

## ÇıKıŞLAR

## NOTLARıNDA
* İşlemin önem derecesi nedeniyle, bu cmdlet varsayılan olarak sizden onay ister. Onayı atlamak için *Force* parametresini belirtin.

## ILGILI BAĞLANTıLAR

[Azure SQL veritabanı](https://azure.microsoft.com/en-us/services/sql-database/)

[Veritabanını sil](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[Azure SQL veritabanları için işlemler](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-Azuressqldatabase](./Get-AzureSqlDatabase.md)

[Yeni-Azuressqldatabase](./New-AzureSqlDatabase.md)

[New-Azuressqldatabaseservercontext](./New-AzureSqlDatabaseServerContext.md)

[Set-Azuressqldatabase](./Set-AzureSqlDatabase.md)


