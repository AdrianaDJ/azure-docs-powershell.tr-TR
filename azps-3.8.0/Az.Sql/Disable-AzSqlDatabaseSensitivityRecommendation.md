---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938045"
---
# <span data-ttu-id="34ce2-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="34ce2-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="34ce2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34ce2-102">SYNOPSIS</span></span>
<span data-ttu-id="34ce2-103">Veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="34ce2-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="34ce2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34ce2-104">SYNTAX</span></span>

### <span data-ttu-id="34ce2-105">Inputobjectparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34ce2-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ce2-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="34ce2-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34ce2-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="34ce2-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34ce2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34ce2-108">DESCRIPTION</span></span>
<span data-ttu-id="34ce2-109">Disable-AzSqlDatabaseSensitivityRecommendation cmdlet, veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="34ce2-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="34ce2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34ce2-110">EXAMPLES</span></span>

### <span data-ttu-id="34ce2-111">Örnek 1: Azure SQL veritabanındaki belirli bir sütunda duyarlılık önerilerini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="34ce2-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="34ce2-112">Örnek 2: yöneltme kullanan bir Azure SQL veritabanında duyarlık önerilerine sahip sütunlarda duyarlılık önerilerini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="34ce2-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="34ce2-113">Örnek 3: boru kullanarak Azure SQL veritabanında belirtilen sütunda duyarlılık önerilerini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="34ce2-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="34ce2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34ce2-114">PARAMETERS</span></span>

### <span data-ttu-id="34ce2-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="34ce2-115">-AsJob</span></span>
<span data-ttu-id="34ce2-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="34ce2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34ce2-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="34ce2-117">-ColumnName</span></span>
<span data-ttu-id="34ce2-118">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="34ce2-118">Name of column.</span></span>

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

### <span data-ttu-id="34ce2-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34ce2-119">-DatabaseName</span></span>
<span data-ttu-id="34ce2-120">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="34ce2-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="34ce2-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="34ce2-121">-DatabaseObject</span></span>
<span data-ttu-id="34ce2-122">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="34ce2-122">The SQL database object.</span></span>

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

### <span data-ttu-id="34ce2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ce2-123">-DefaultProfile</span></span>
<span data-ttu-id="34ce2-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34ce2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ce2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34ce2-125">-InputObject</span></span>
<span data-ttu-id="34ce2-126">SQL veritabanı duyarlılığı sınıflandırmasını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="34ce2-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="34ce2-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34ce2-127">-PassThru</span></span>
<span data-ttu-id="34ce2-128">Cmdlet 'in yürütülmesinin sonunda duyarlılık sınıflandırması modelinin çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="34ce2-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="34ce2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34ce2-129">-ResourceGroupName</span></span>
<span data-ttu-id="34ce2-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34ce2-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="34ce2-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="34ce2-131">-SchemaName</span></span>
<span data-ttu-id="34ce2-132">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="34ce2-132">Name of schema.</span></span>

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

### <span data-ttu-id="34ce2-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="34ce2-133">-ServerName</span></span>
<span data-ttu-id="34ce2-134">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="34ce2-134">SQL server name.</span></span>

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

### <span data-ttu-id="34ce2-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="34ce2-135">-TableName</span></span>
<span data-ttu-id="34ce2-136">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="34ce2-136">Name of table.</span></span>

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

### <span data-ttu-id="34ce2-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="34ce2-137">-Confirm</span></span>
<span data-ttu-id="34ce2-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34ce2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ce2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ce2-139">-WhatIf</span></span>
<span data-ttu-id="34ce2-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34ce2-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34ce2-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34ce2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ce2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ce2-142">CommonParameters</span></span>
<span data-ttu-id="34ce2-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34ce2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ce2-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34ce2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ce2-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34ce2-145">INPUTS</span></span>

### <span data-ttu-id="34ce2-146">Microsoft. Azure. Commands. Sql. DataClassification. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="34ce2-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="34ce2-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34ce2-147">OUTPUTS</span></span>

### <span data-ttu-id="34ce2-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34ce2-148">System.Boolean</span></span>

## <span data-ttu-id="34ce2-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34ce2-149">NOTES</span></span>

## <span data-ttu-id="34ce2-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34ce2-150">RELATED LINKS</span></span>

[<span data-ttu-id="34ce2-151">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="34ce2-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)