---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: ad46883722f0c9d4c4d8bf5a5f5f568bb267bba5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764764"
---
# Get-AzureRmSqlDatabaseGeoBackup

## SYNOPSIS
Bir veritabanının coğrafi yedekli yedeklemesini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Get-AzureRMSqlDatabaseGeoBackup** cmdlet 'i, belirtilen bir sunucuda bir SQL veritabanının belirtilen coğrafi ve yedekli yedek yedeklemelerini alır.

Coğrafi olarak yedekli yedekleme, ayrı bir coğrafi konumdan veri dosyalarını kullanan geri yüklenebilen bir kaynaktır.
Veritabanınızı yeni bir bölgeye kurtarmak için bölgesel kesinti olayında coğrafi artıklık yedeği geri yüklemek için Geo-Restore kullanabilirsiniz.

Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.

## ÖRNEKLERDEN

### Örnek 1: sunucudaki tüm Coğrafi Yedekli yedekleri alma
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

Bu komut, belirli bir sunucudaki tüm coğrafi artıklık yedekli yedekleri alır.

### Örnek 2: belirtilen coğrafi
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

Bu komut, ContosoDatabase adlı veritabanı coğrafi artıklık yedeklemesini alır.

## PARAMETRELERINE

### -DatabaseName
Alınacak veritabanının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
SQL veritabanı sunucusunun atandığı kaynak grubunun adını belirtir.

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
Geri yüklenecek yedeklemeyi barındıran sunucunun adını belirtir.

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. Backup. model. Azuressqldatabasegeobackupmodel

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Genel Bakış: SQL veritabanıyla bulut iş devamlılık ve veritabanı olağanüstü durum kurtarması](https://go.microsoft.com/fwlink/?LinkId=746881)

[Azure SQL veritabanını kesinti 'den kurtarma](https://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)
