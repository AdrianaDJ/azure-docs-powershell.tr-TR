---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266776"
---
# <span data-ttu-id="4fe61-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4fe61-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="4fe61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fe61-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe61-103">Veritabanındaki sütunların bilgi türlerini ve duyarlılık etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4fe61-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="4fe61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4fe61-104">SYNTAX</span></span>

### <span data-ttu-id="4fe61-105">ClassificationObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4fe61-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe61-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fe61-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fe61-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fe61-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fe61-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4fe61-108">DESCRIPTION</span></span>
<span data-ttu-id="4fe61-109">Set-AzSqlDatabaseSensitivityClassification cmdlet 'i veritabanındaki sütunların bilgi türlerini ve duyarlılık etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4fe61-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="4fe61-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4fe61-110">EXAMPLES</span></span>

### <span data-ttu-id="4fe61-111">Örnek 1: Azure SQL veritabanındaki bir sütunun bilgi türü ve duyarlılık etiketini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4fe61-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="4fe61-112">Örnek 2: bir Azure SQL veritabanındaki sütunların önerilen bilgi türlerini ve duyarlılık etiketlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4fe61-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="4fe61-113">Örnek 3: yöneltme kullanarak Azure SQL veritabanındaki bir sütunun bilgi türü ve duyarlılık etiketini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4fe61-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="4fe61-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4fe61-114">PARAMETERS</span></span>

### <span data-ttu-id="4fe61-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="4fe61-115">-AsJob</span></span>
<span data-ttu-id="4fe61-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4fe61-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4fe61-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="4fe61-117">-ClassificationObject</span></span>
<span data-ttu-id="4fe61-118">SQL veritabanı duyarlılığı sınıflandırmasını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="4fe61-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="4fe61-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4fe61-119">-ColumnName</span></span>
<span data-ttu-id="4fe61-120">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="4fe61-120">Name of column.</span></span>

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

### <span data-ttu-id="4fe61-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4fe61-121">-DatabaseName</span></span>
<span data-ttu-id="4fe61-122">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4fe61-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="4fe61-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4fe61-123">-DatabaseObject</span></span>
<span data-ttu-id="4fe61-124">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4fe61-124">The SQL database object.</span></span>

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

### <span data-ttu-id="4fe61-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe61-125">-DefaultProfile</span></span>
<span data-ttu-id="4fe61-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4fe61-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fe61-127">-Informationtype</span><span class="sxs-lookup"><span data-stu-id="4fe61-127">-InformationType</span></span>
<span data-ttu-id="4fe61-128">Sütunda depolanan verilerin bilgi türünü açıklayan ad.</span><span class="sxs-lookup"><span data-stu-id="4fe61-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe61-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4fe61-129">-PassThru</span></span>
<span data-ttu-id="4fe61-130">Cmdlet 'in yürütülmesinin sonunda duyarlılık sınıflandırması modelinin çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="4fe61-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="4fe61-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe61-131">-ResourceGroupName</span></span>
<span data-ttu-id="4fe61-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4fe61-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="4fe61-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4fe61-133">-SchemaName</span></span>
<span data-ttu-id="4fe61-134">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="4fe61-134">Name of schema.</span></span>

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

### <span data-ttu-id="4fe61-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="4fe61-135">-SensitivityLabel</span></span>
<span data-ttu-id="4fe61-136">Sütunda depolanan verilerin duyarlılığını açıklayan ad.</span><span class="sxs-lookup"><span data-stu-id="4fe61-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fe61-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4fe61-137">-ServerName</span></span>
<span data-ttu-id="4fe61-138">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="4fe61-138">SQL server name.</span></span>

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

### <span data-ttu-id="4fe61-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="4fe61-139">-TableName</span></span>
<span data-ttu-id="4fe61-140">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="4fe61-140">Name of table.</span></span>

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

### <span data-ttu-id="4fe61-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="4fe61-141">-Confirm</span></span>
<span data-ttu-id="4fe61-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4fe61-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fe61-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe61-143">-WhatIf</span></span>
<span data-ttu-id="4fe61-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4fe61-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fe61-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4fe61-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fe61-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe61-146">CommonParameters</span></span>
<span data-ttu-id="4fe61-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4fe61-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe61-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4fe61-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe61-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4fe61-149">INPUTS</span></span>

### <span data-ttu-id="4fe61-150">Microsoft. Azure. Commands. Sql. DataClassification. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="4fe61-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="4fe61-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4fe61-151">OUTPUTS</span></span>

### <span data-ttu-id="4fe61-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fe61-152">System.Boolean</span></span>

## <span data-ttu-id="4fe61-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4fe61-153">NOTES</span></span>

## <span data-ttu-id="4fe61-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4fe61-154">RELATED LINKS</span></span>

[<span data-ttu-id="4fe61-155">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="4fe61-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
