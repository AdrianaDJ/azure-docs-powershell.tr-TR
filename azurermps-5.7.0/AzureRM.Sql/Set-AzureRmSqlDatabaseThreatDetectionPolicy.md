---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: aa70b94614f8a0826a5d1563439afa8cb9ef6d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593362"
---
# Set-AzureRmSqlDatabaseThreatDetectionPolicy

## SYNOPSIS
Veritabanında tehdit algılama ilkesini ayarlar.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet 'ı BIR Azure SQL veritabanında tehdit algılama ilkesini ayarlar.
Veritabanında tehdit algılamasını etkinleştirmek için bu veritabanında denetim ilkesi etkinleştirilmelidir.

Bu cmdlet 'i kullanmak için, veritabanını tanımlayacak *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini belirtin.

Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.

## ÖRNEKLERDEN

### Örnek 1: veritabanı için tehdit algılama ilkesini ayarlama
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

Bu komut, server01 adındaki sunucuda Database01 adlı bir veritabanı için tehdit algılama ilkesini ayarlar.

## PARAMETRELERINE

### -DatabaseName
İlkenin ayarlandığı veritabanının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Eda
Tehdit algılama ilkesinin e-posta kullanarak yöneticilere mı ait olduğunu belirtir.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExcludedDetectionType
İlkeden dışlanacak algılama türleri dizisini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Sql_Injection 
- Sql_Injection_Vulnerability 
- Access_Anomaly 
- Yabilirsiniz

```yaml
Type: DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Notificationrecipientşeması ILS
İlkenin uyarıları gönderdiği e-posta adreslerinin noktalı virgülle ayrılmış listesini belirtir.

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

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

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

### -ResourceGroupName
Sunucunun atandığı kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Denetim günlükleri için bekletme günü sayısı

```yaml
Type: UInt32
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

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Kullanılacak depolama hesabının adını belirtir. Joker karakterlere izin verilmez. Bu parametre gerekli değildir. Bu parametre sağlanmadıysa cmdlet, veritabanının tehdit algılama ilkesinin bir parçası olarak daha önce tanımlanan depolama hesabını kullanır. Bir veritabanı tehdit algılama ilkesi ilk kez tanımlandıysa ve bu parametre sağlanmadıysa cmdlet başarısız olur.

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

###  
Bu cmdlet 'e giriş kanalı oluşturamazsınız.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. ThreatDetection. model. DatabaseThreatDetectionPolicyModel
Bu cmdlet, bir **model. DatabaseThreatDetectionPolicyModel** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmSqlDatabaseThreatDetectionPolicy](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[Remove-AzureRmSqlDatabaseThreatDetectionPolicy](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)


