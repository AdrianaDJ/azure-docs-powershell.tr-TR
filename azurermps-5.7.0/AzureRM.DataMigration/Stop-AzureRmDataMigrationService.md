---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/stop-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Stop-AzureRmDataMigrationService.md
ms.openlocfilehash: 9a3028e019d3873105df079b67652f2157137ce2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594963"
---
# Stop-AzureRmDataMigrationService

## SYNOPSIS
Çalışan bir durumda olan Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ComponentNameParameterSet (varsayılan)
```
Stop-AzureRmDataMigrationService -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### Bileşen Entobjectparameterparameteri
```
Stop-AzureRmDataMigrationService [-InputObject] <PSDataMigrationService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### Resourceıdparameterset
```
Stop-AzureRmDataMigrationService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## Tanım
Stop-AzureRmDataMigrationService cmdlet 'i, çalışan bir durumda olan Azure veritabanı geçiş hizmeti 'nin bir örneğini durdurur.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Stop-AzureRmDataMigrationService -ResourceGroupName MyResourceGroup –ServiceName TestService

```
Yukarıdaki örnek, giriş parametresi olarak geçirilen hizmet adına dayanan TestService adındaki bir Azure veritabanı geçiş hizmeti örneğini durdurur

### Örnek 2
```
PS C:\> Stop-AzureRmDataMigrationService -InputObject $TestService

```
Yukarıdaki örnek, giriş parametresi olarak geçirilen PSDataMigrationService nesnesini temel alan Azure veritabanı geçiş hizmeti örneğini durdurur.



## PARAMETRELERINE

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
Veri geçişi hizmeti adı.

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Bir doğru/yanlış döndürür.
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

### Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
System. String


## ÇıKıŞLAR

### System. Boolean


## NOTLARıNDA

## ILGILI BAĞLANTıLAR

