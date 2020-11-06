---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593777"
---
# Suspend-AzureRmSqlDatabase

## SYNOPSIS
SQL veri ambarı veritabanını askıya alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Askıya al-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veri ambarı veritabanını askıya alır.

## ÖRNEKLERDEN

### Örnek 1: Azure SQL veri ambarı veritabanını askıya alır
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Bu komut, etkin bir Azure SQL veri ambarı veritabanını askıya alır.

## PARAMETRELERINE

### -DatabaseName
Bu cmdlet 'in askıya aldığı veritabanının adını belirtir.

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
Veritabanını barındıran sunucunun adını belirtir.

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

### Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel

## NOTLARıNDA
* **Suspend-AzureRmSqlDatabase** cmdlet 'ı yalnızca Azure SQL veri ambarı veritabanlarında çalışır. Bu işlem, Azure SQL veritabanı temel, Standard ve Premium sürümlerinde desteklenmez.

## ILGILI BAĞLANTıLAR

[Get-AzureRmSqlDatabase](./Get-AzureRmSqlDatabase.md)

[Yeni-AzureRmSqlDatabase](./New-AzureRmSqlDatabase.md)

[Remove-AzureRmSqlDatabase](./Remove-AzureRmSqlDatabase.md)

[Özgeçmiş-AzureRmSqlDatabase](./Resume-AzureRmSqlDatabase.md)

[Set-AzureRmSqlDatabase](./Set-AzureRmSqlDatabase.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)


