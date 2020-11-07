---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: adf689396930b57b18c53d5ac6d98478ab6f952a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933649"
---
# Get-AzSqlDatabaseUpgradeHint

## SYNOPSIS
Bir veritabanı için fiyatlandırma katmanı ipuçlarını alır.

## INDEKI

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Get-AzSqlDatabaseUpgradeHint** cmdlet 'i, BIR Azure SQL veritabanını yükseltmek için fiyatlandırma katmanı ipuçlarını alır.
Hala Web ve Iş fiyatlandırması katmanlarındaki veritabanları, yeni temel, standart veya Premium fiyatlandırma katmanlarına yükseltme ipucunu alır.
Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.

## ÖRNEKLERDEN

### Örnek 1: sunucudaki tüm veritabanlarına yönelik öneriler alma
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

Bu komut, server01 adındaki sunucudaki tüm veritabanlarının yükseltme ipuçlarını döndürür.

### Örnek 2: belirli veritabanı için öneriler alma
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

Bu komut, belirli bir veritabanının yükseltme ipuçlarını döndürür.

### Örnek 3: elastik bir veritabanı havuzunda bulunmayan tüm veritabanları için öneri alma
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

Bu komut, elastik bir veritabanı havuzunda olmayan tüm veritabanlarının yükseltme ipuçlarını döndürür.

### Örnek 4: filtreleme kullanarak sunucudaki tüm veritabanlarına yönelik öneriler alma
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

Bu komut, server01 adlı sunucudaki "veritabanı" ile başlayan tüm veritabanlarının yükseltme ipuçlarını döndürür.

## PARAMETRELERINE

### -DatabaseName
Bu cmdlet 'in bir yükseltme ipucu aldığı SQL veritabanının adını belirtir.
Bir veritabanı belirtmezseniz, bu cmdlet mantıksal sunucudaki tüm veritabanlarının ipuçlarını alır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Excludeeladapooladaylar
Elastik veritabanı havuzlarındaki veritabanlarının döndürülen önerilerden dışlanıp dışlanmadığını gösterir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Veritabanının atandığı kaynak grubunun adını belirtir.

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
Bu cmdlet 'in yükseltme ipucu aldığı veritabanını barındıran sunucunun adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Boolean

## ÇıKıŞLAR

### Microsoft. Azure. Management. Sql. LegacySdk. modeller. RecommendedDatabaseProperties

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azsqldatabasegenişletilen](./Get-AzSqlDatabaseExpanded.md)

[Get-Azsqlelaunpooltavsiyeleri](./Get-AzSqlElasticPoolRecommendation.md)


