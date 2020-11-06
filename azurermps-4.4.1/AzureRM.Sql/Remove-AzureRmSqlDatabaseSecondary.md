---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 54E01B3B-FFA5-4E3C-BA5A-A281FF5C9F8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 843a3bd4cd3d43239cfb850edc3cd3b4fb3461ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594994"
---
# Remove-AzureRmSqlDatabaseSecondary

## SYNOPSIS
SQL veritabanıyla belirtilen ikincil veritabanı arasında veri çoğaltmayı sonlandırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmSqlDatabaseSecondary** cmdlet 'i coğrafi çoğaltma bağlantısını sonlandırmaya zorlar.
Bu cmdlet Stop-AzureSqlDatabaseCopy cmdlet 'ini değiştirir.
İşten çıkmadan önce çoğaltma eşitlemesi yapılmaz.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -DatabaseName
Bu cmdlet 'in kaldırıldığı çoğaltma bağlantısının bulunduğu birincil Azure SQL veritabanının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartnerResourceGroupName
İş ortağı kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartnerServerName
İş ortağı SQL Server 'ın adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaldırılacak olan çoğaltma bağlantısıyla ilişkilendirilmiş olan kaynak grubunun adını belirtir.

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
Kaldırılacak çoğaltma bağlantısının bulunduğu SQL sunucusunun adını belirtir.

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

###  
Birincil veya ikincil veritabanı için **veritabanı** nesnesinin örneklerini bu cmdlet 'e boru edebilirsiniz.

## ÇıKıŞLAR

###  
Bu cmdlet hiçbir çıkış üretmez.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzureRmSqlDatabaseSecondary](./New-AzureRmSqlDatabaseSecondary.md)

[Set-AzureRmSqlDatabaseSecondary](./Set-AzureRmSqlDatabaseSecondary.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)
