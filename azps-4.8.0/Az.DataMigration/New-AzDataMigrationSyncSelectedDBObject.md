---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274573"
---
# New-AzDataMigrationSyncSelectedDBObject

## SYNOPSIS
Geçiş görevi için kullanılacak eşitleme senaryosuna özgü bir veritabanı bilgileri nesnesi oluşturur.

## INDEKI

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım

New-AzDataMigrationSyncSelectedDB cmdlet 'i, kaynak ve hedef veritabanları hakkında bilgi içeren eşitleme senaryosuna özgü bir veritabanı bilgileri nesnesi oluşturur.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

Bu örnek, veritabanı $DatabaseName $DatabaseName geçiş ayarlarını açıklayan bir veritabanı meta veri nesnesi oluşturur.  

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -MigrationSetting
Geçiş davranışını ayarlamaya yönelik geçiş ayarları

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchemaName
Geçirilecek şema adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Kaynak veritabanının adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceSetting
Kaynak uç noktası geçiş davranışını ayarlamak için kaynak ayarlar

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TableMap
Kaynak hedef tablolarla eşleme

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
Hedef veritabanının adı

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetSetting
Hedef uç nokta geçiş davranışını ayarlamak için hedef ayarlar

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbsynctaskınput

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
