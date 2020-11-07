---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938109"
---
# <span data-ttu-id="9c08a-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="9c08a-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="9c08a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c08a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c08a-103">Sütunlardaki duyarlılık önerilerini etkinleştir (tüm sütunlarda öneri varsayılan olarak etkindir).</span><span class="sxs-lookup"><span data-stu-id="9c08a-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="9c08a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c08a-104">SYNTAX</span></span>

### <span data-ttu-id="9c08a-105">Inputobjectparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9c08a-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c08a-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c08a-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c08a-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c08a-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c08a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c08a-108">DESCRIPTION</span></span>
<span data-ttu-id="9c08a-109">Enable-AzSqlDatabaseSensitivityRecommendation cmdlet, veritabanındaki sütunlarda duyarlılık önerilerini etkin kılar.</span><span class="sxs-lookup"><span data-stu-id="9c08a-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="9c08a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c08a-110">EXAMPLES</span></span>

### <span data-ttu-id="9c08a-111">Örnek 1: Azure SQL veritabanındaki belirli bir sütunda duyarlılık önerilerini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="9c08a-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="9c08a-112">Örnek 2: boru kullanarak belirli bir sütunda Azure SQL veritabanında duyarlılık önerilerini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="9c08a-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="9c08a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c08a-113">PARAMETERS</span></span>

### <span data-ttu-id="9c08a-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="9c08a-114">-AsJob</span></span>
<span data-ttu-id="9c08a-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9c08a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c08a-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9c08a-116">-ColumnName</span></span>
<span data-ttu-id="9c08a-117">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="9c08a-117">Name of column.</span></span>

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

### <span data-ttu-id="9c08a-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c08a-118">-DatabaseName</span></span>
<span data-ttu-id="9c08a-119">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="9c08a-119">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="9c08a-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9c08a-120">-DatabaseObject</span></span>
<span data-ttu-id="9c08a-121">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9c08a-121">The SQL database object.</span></span>

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

### <span data-ttu-id="9c08a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c08a-122">-DefaultProfile</span></span>
<span data-ttu-id="9c08a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c08a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c08a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c08a-124">-InputObject</span></span>
<span data-ttu-id="9c08a-125">SQL veritabanı duyarlılığı sınıflandırmasını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="9c08a-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9c08a-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9c08a-126">-PassThru</span></span>
<span data-ttu-id="9c08a-127">Cmdlet 'in yürütülmesinin sonunda duyarlılık sınıflandırması modelinin çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="9c08a-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="9c08a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c08a-128">-ResourceGroupName</span></span>
<span data-ttu-id="9c08a-129">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9c08a-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="9c08a-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9c08a-130">-SchemaName</span></span>
<span data-ttu-id="9c08a-131">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="9c08a-131">Name of schema.</span></span>

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

### <span data-ttu-id="9c08a-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9c08a-132">-ServerName</span></span>
<span data-ttu-id="9c08a-133">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="9c08a-133">SQL server name.</span></span>

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

### <span data-ttu-id="9c08a-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="9c08a-134">-TableName</span></span>
<span data-ttu-id="9c08a-135">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="9c08a-135">Name of table.</span></span>

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

### <span data-ttu-id="9c08a-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c08a-136">-Confirm</span></span>
<span data-ttu-id="9c08a-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c08a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c08a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c08a-138">-WhatIf</span></span>
<span data-ttu-id="9c08a-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c08a-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c08a-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c08a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c08a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c08a-141">CommonParameters</span></span>
<span data-ttu-id="9c08a-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c08a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c08a-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9c08a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c08a-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c08a-144">INPUTS</span></span>

### <span data-ttu-id="9c08a-145">Microsoft. Azure. Commands. Sql. DataClassification. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9c08a-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9c08a-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c08a-146">OUTPUTS</span></span>

### <span data-ttu-id="9c08a-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9c08a-147">System.Boolean</span></span>

## <span data-ttu-id="9c08a-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c08a-148">NOTES</span></span>

## <span data-ttu-id="9c08a-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c08a-149">RELATED LINKS</span></span>

[<span data-ttu-id="9c08a-150">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="9c08a-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)