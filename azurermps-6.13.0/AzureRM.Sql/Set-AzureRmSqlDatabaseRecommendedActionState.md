---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: c926078b46fbfb27947e53121e159aafe092da3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593623"
---
# Set-AzureRmSqlDatabaseRecommendedActionState

## SYNOPSIS
Bir Azure SQL veritabanı önerilen eyleminin durumunu güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Set-AzureRmSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureRmSqlDatabaseRecommendedActionState** cmdlet 'i, BIR Azure SQL veritabanı önerilen eyleminin durumunu güncelleştirir.
Bu, önerilen bir eylemin yeni duruma göre uygulanmasını, geri döndürüldüğünü veya atılmasına olanak tanır.

## ÖRNEKLERDEN

### Örnek 1: beklemede olan önerilen bir eylem durumunu uygulama
```
PS C:\>Set-AzureRmSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

Bu komut, \[ \] \[ \] wirunner adlı veritabanına ait olan IR_ test_schema _ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893 adlı önerilen eylemin durumunu güncelleştirir.

## PARAMETRELERINE

### -Danışmanlar veya ad
Bu önerilen eylemin ait olduğu danışman adını belirtir.

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

### -DatabaseName
Bu cmdlet 'in önerilen eylem durumunu ayarladığı veritabanının adını belirtir.

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -RecommendedActionName
Durumu güncelleştirilen önerilen eylemin adını belirtir.

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
Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.

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
Veritabanının bulunduğu sunucunun adını belirtir.

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

### Durumlu
Bu cmdlet 'in önerilen eylem durumunu güncelleştirdiği yeni değeri belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Etkin
- Bekley
- Pendinggeri döndür
- Yankı Iptal edildi
- Edildi
- Lemezse

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. Sql. RecommendedAction. cmdlet. RecommendedActionState

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. RecommendedAction. model. AzureSqlDatabaseRecommendedActionModel

## NOTLARıNDA
* Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, Manager, SQL, veritabanı, MSSQL, danışman, recommendedaction

## ILGILI BAĞLANTıLAR

[Get-AzureRmSqlServerAdvisor](./Get-AzureRmSqlServerAdvisor.md)

[Get-AzureRmSqlElasticPoolAdvisor](./Get-AzureRmSqlElasticPoolAdvisor.md)

[Get-AzureRmSqlServerRecommendedAction](./Get-AzureRmSqlServerRecommendedAction.md)

[Get-AzureRmSqlElasticPoolRecommendedAction](./Get-AzureRmSqlElasticPoolRecommendedAction.md)

[Set-AzureRmSqlElasticPoolRecommendedActionState](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[Set-AzureRmSqlElasticPoolRecommendedActionState](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[Set-AzureRmSqlServerRecommendedActionState](./Set-AzureRmSqlServerRecommendedActionState.md)

[Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus](./Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus.md)

[Set-Azurermsqlserverdanışmanlar Orautoexecutestatus](./Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)
