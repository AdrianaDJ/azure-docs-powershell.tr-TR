---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: d60eff325b0240591fc3360276447861560860ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933817"
---
# <span data-ttu-id="d50b1-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="d50b1-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="d50b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d50b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d50b1-103">Veritabanındaki sütunların bilgi türlerini ve duyarlılık etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d50b1-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="d50b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d50b1-104">SYNTAX</span></span>

### <span data-ttu-id="d50b1-105">ClassificationObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d50b1-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d50b1-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d50b1-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d50b1-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="d50b1-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d50b1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d50b1-108">DESCRIPTION</span></span>
<span data-ttu-id="d50b1-109">Remove-AzSqlDatabaseSensitivityClassification cmdlet 'i veritabanındaki sütunların bilgi türlerini ve duyarlılık etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d50b1-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="d50b1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d50b1-110">EXAMPLES</span></span>

### <span data-ttu-id="d50b1-111">Örnek 1: Azure SQL veritabanındaki bir sütunun bilgi türü ve duyarlılık etiketini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="d50b1-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="d50b1-112">Örnek 2: yöneltme kullanarak Azure SQL veritabanındaki sütunların geçerli bilgi türlerini ve duyarlılık etiketlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="d50b1-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="d50b1-113">Örnek 3: yöneltme kullanarak Azure SQL veritabanındaki bir sütunun bilgi türü ve duyarlılık etiketini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="d50b1-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="d50b1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d50b1-114">PARAMETERS</span></span>

### <span data-ttu-id="d50b1-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="d50b1-115">-AsJob</span></span>
<span data-ttu-id="d50b1-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d50b1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d50b1-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="d50b1-117">-ClassificationObject</span></span>
<span data-ttu-id="d50b1-118">SQL veritabanı duyarlılığı sınıflandırmasını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="d50b1-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d50b1-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="d50b1-119">-ColumnName</span></span>
<span data-ttu-id="d50b1-120">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="d50b1-120">Name of column.</span></span>

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

### <span data-ttu-id="d50b1-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d50b1-121">-DatabaseName</span></span>
<span data-ttu-id="d50b1-122">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="d50b1-122">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50b1-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d50b1-123">-DatabaseObject</span></span>
<span data-ttu-id="d50b1-124">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d50b1-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d50b1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d50b1-125">-DefaultProfile</span></span>
<span data-ttu-id="d50b1-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d50b1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d50b1-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d50b1-127">-PassThru</span></span>
<span data-ttu-id="d50b1-128">Cmdlet 'in yürütülmesinin sonunda duyarlılık sınıflandırması modelinin çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="d50b1-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="d50b1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d50b1-129">-ResourceGroupName</span></span>
<span data-ttu-id="d50b1-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d50b1-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50b1-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="d50b1-131">-SchemaName</span></span>
<span data-ttu-id="d50b1-132">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="d50b1-132">Name of schema.</span></span>

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

### <span data-ttu-id="d50b1-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d50b1-133">-ServerName</span></span>
<span data-ttu-id="d50b1-134">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="d50b1-134">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d50b1-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="d50b1-135">-TableName</span></span>
<span data-ttu-id="d50b1-136">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="d50b1-136">Name of table.</span></span>

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

### <span data-ttu-id="d50b1-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="d50b1-137">-Confirm</span></span>
<span data-ttu-id="d50b1-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d50b1-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50b1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d50b1-139">-WhatIf</span></span>
<span data-ttu-id="d50b1-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d50b1-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d50b1-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d50b1-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d50b1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d50b1-142">CommonParameters</span></span>
<span data-ttu-id="d50b1-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d50b1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d50b1-144">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d50b1-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d50b1-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d50b1-145">INPUTS</span></span>

### <span data-ttu-id="d50b1-146">Microsoft. Azure. Commands. Sql. DataClassification. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="d50b1-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="d50b1-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d50b1-147">OUTPUTS</span></span>

### <span data-ttu-id="d50b1-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d50b1-148">System.Boolean</span></span>

## <span data-ttu-id="d50b1-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d50b1-149">NOTES</span></span>

## <span data-ttu-id="d50b1-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d50b1-150">RELATED LINKS</span></span>

[<span data-ttu-id="d50b1-151">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="d50b1-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
