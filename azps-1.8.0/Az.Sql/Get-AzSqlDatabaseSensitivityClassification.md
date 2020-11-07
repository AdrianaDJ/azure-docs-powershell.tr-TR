---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 50bd23f0c0be638683dae4acb5b43165a8c5b4f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759017"
---
# <span data-ttu-id="9e812-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="9e812-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="9e812-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e812-102">SYNOPSIS</span></span>
<span data-ttu-id="9e812-103">Veritabanındaki sütunların geçerli bilgi türlerini ve duyarlılık etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="9e812-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="9e812-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e812-104">SYNTAX</span></span>

### <span data-ttu-id="9e812-105">DatabaseObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9e812-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e812-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e812-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e812-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e812-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e812-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e812-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e812-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e812-109">DESCRIPTION</span></span>
<span data-ttu-id="9e812-110">Get-AzSqlDatabaseSensitivityClassification cmdlet 'i Azure SQL veritabanındaki sütunların geçerli bilgi türlerini ve duyarlılık etiketlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e812-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="9e812-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e812-111">EXAMPLES</span></span>

### <span data-ttu-id="9e812-112">Örnek 1: Azure SQL veritabanının geçerli bilgi türlerini ve duyarlılık etiketlerini alma.</span><span class="sxs-lookup"><span data-stu-id="9e812-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="9e812-113">Örnek 2: yöneltme içeren bir Azure SQL veritabanının geçerli bilgi türlerini ve duyarlılık etiketlerini alma.</span><span class="sxs-lookup"><span data-stu-id="9e812-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="9e812-114">Örnek 3: Azure SQL veritabanının belirli bir sütununun geçerli bilgi türü ve duyarlılık etiketini alma.</span><span class="sxs-lookup"><span data-stu-id="9e812-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="9e812-115">Örnek 4: yöneltme kullanarak Azure SQL veritabanının belirli bir sütununun geçerli bilgi türü ve duyarlılık etiketini alma.</span><span class="sxs-lookup"><span data-stu-id="9e812-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="9e812-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e812-116">PARAMETERS</span></span>

### <span data-ttu-id="9e812-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="9e812-117">-AsJob</span></span>
<span data-ttu-id="9e812-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9e812-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e812-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9e812-119">-ColumnName</span></span>
<span data-ttu-id="9e812-120">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="9e812-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e812-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9e812-121">-DatabaseName</span></span>
<span data-ttu-id="9e812-122">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="9e812-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e812-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9e812-123">-DatabaseObject</span></span>
<span data-ttu-id="9e812-124">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9e812-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e812-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e812-125">-DefaultProfile</span></span>
<span data-ttu-id="9e812-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e812-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e812-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e812-127">-ResourceGroupName</span></span>
<span data-ttu-id="9e812-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9e812-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e812-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9e812-129">-SchemaName</span></span>
<span data-ttu-id="9e812-130">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="9e812-130">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e812-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e812-131">-ServerName</span></span>
<span data-ttu-id="9e812-132">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="9e812-132">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e812-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="9e812-133">-TableName</span></span>
<span data-ttu-id="9e812-134">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="9e812-134">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e812-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e812-135">CommonParameters</span></span>
<span data-ttu-id="9e812-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e812-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e812-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9e812-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e812-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e812-138">INPUTS</span></span>

### <span data-ttu-id="9e812-139">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="9e812-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9e812-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e812-140">OUTPUTS</span></span>

### <span data-ttu-id="9e812-141">Microsoft. Azure. Commands. Sql. DataClassification. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9e812-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9e812-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e812-142">NOTES</span></span>

## <span data-ttu-id="9e812-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e812-143">RELATED LINKS</span></span>

[<span data-ttu-id="9e812-144">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="9e812-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)