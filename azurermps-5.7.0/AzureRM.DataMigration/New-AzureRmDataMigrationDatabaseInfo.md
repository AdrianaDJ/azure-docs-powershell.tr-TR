---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764459"
---
# New-AzureRmDataMigrationDatabaseInfo

## SYNOPSIS
Geçiş için veritabanı kaynağını belirten Azure veritabanı geçiş hizmeti için Databaseınfo nesnesini oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## Tanım
New-AzureRmDataMigrationDatabaseInfo cmdlet, geçirilecek kaynak veritabanı örneğini belirten Databaseınfo nesnesini oluşturur. Veritabanı adı giriş parametresi olarak alınır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

Önceki örnek, kaynak veritabanı **AdventureWorks2016** için yeni bir databaseınfo nesnesi oluşturur.

Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır. Get-AzureSubscription cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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
### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
Kaynak veritabanı adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### Yabilirsiniz


## ÇıKıŞLAR

### Microsoft. Azure. Management. DataMigration. modeller. Databaseınfo


## NOTLARıNDA

## ILGILI BAĞLANTıLAR


