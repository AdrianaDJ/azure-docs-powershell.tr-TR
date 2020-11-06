---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/get-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Get-AzureRmDataMigrationProject.md
ms.openlocfilehash: ea6406d83004d9a7d21a2f47aba0c39a10caf59a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593505"
---
# Get-AzureRmDataMigrationProject

## SYNOPSIS
Azure veritabanı geçiş projesi özelliklerini getirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ComponentNameParameterSet (varsayılan)
```
Get-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### Bileşen Entobjectparameterparameteri
```
Get-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### Resourceıdparameterset
```
Get-AzureRmDataMigrationProject [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

## Tanım
Get-AzureRmDataMigrationProject cmdlet 'i, Azure veritabanı geçiş projesi özelliklerini alır.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Get-AzureRmDataMigrationProject -ServiceName testService -Name testProject -ResourceGroup testResourceGroup
```

Yukarıdaki örnek testresourcegroup adındaki ve testhizmeti adlı hizmet 'in altındaki test

### Örnek 2
```
PS C:\> Get-AzureRmDataMigrationProject -InputObject $myService
```

Yukarıdaki örnek, gelen PSProject nesne giriş parametresine dayalı olarak Azure veritabanı geçiş projesini alır. 


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

### -InputObject
PSDataMigrationService nesnesi.

```yaml
Type: PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Projenin adı.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProjectName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adı.

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
DataMigrationService kaynak kimliği.

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -HizmetAdı
Veri geçişi hizmeti adı.

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## GÖLGELENDIRICI

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
System. String


## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. DataMigration. modeller. PSProject, Microsoft. Azure. Commands. DataMigration, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]


## NOTLARıNDA

## ILGILI BAĞLANTıLAR

