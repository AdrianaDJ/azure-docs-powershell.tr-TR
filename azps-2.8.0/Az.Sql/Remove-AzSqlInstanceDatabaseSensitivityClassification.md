---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: fa187bad03027f1c0dd3e1c38e8b05dfb9257f05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933800"
---
# <span data-ttu-id="4a8e7-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4a8e7-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="4a8e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="4a8e7-103">Azure SQL yönetilen örnek veritabanındaki sütunların bilgi türlerini ve duyarlılık etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="4a8e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a8e7-104">SYNTAX</span></span>

### <span data-ttu-id="4a8e7-105">ClassificationObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a8e7-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a8e7-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a8e7-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a8e7-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a8e7-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a8e7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a8e7-108">DESCRIPTION</span></span>
<span data-ttu-id="4a8e7-109">Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet 'i Azure SQL yönetilen örnek veritabanındaki sütunların bilgi türlerini ve duyarlılık etiketlerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="4a8e7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a8e7-110">EXAMPLES</span></span>

### <span data-ttu-id="4a8e7-111">Örnek 1: Azure SQL yönetilen örnek veritabanındaki bir sütunun bilgi türü ve duyarlılık etiketini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="4a8e7-112">Örnek 2: bir Azure SQL yönetilen örnek veritabanındaki sütunların geçerli bilgi türlerini ve duyarlılık etiketlerini boru ile kaldırın.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="4a8e7-113">Örnek 3: yöneltme ile Azure SQL yönetilen örnek veritabanındaki bir sütunun bilgi türü ve duyarlılık etiketini kaldırma.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="4a8e7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a8e7-114">PARAMETERS</span></span>

### <span data-ttu-id="4a8e7-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="4a8e7-115">-AsJob</span></span>
<span data-ttu-id="4a8e7-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4a8e7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a8e7-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="4a8e7-117">-ClassificationObject</span></span>
<span data-ttu-id="4a8e7-118">SQL yönetilen örnek veritabanı duyarlılığı sınıflandırmasını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8e7-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4a8e7-119">-ColumnName</span></span>
<span data-ttu-id="4a8e7-120">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-120">Name of column.</span></span>

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

### <span data-ttu-id="4a8e7-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a8e7-121">-DatabaseName</span></span>
<span data-ttu-id="4a8e7-122">Azure SQL yönetilen örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="4a8e7-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="4a8e7-123">-DatabaseObject</span></span>
<span data-ttu-id="4a8e7-124">Azure SQL yönetilen örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a8e7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a8e7-125">-DefaultProfile</span></span>
<span data-ttu-id="4a8e7-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a8e7-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4a8e7-127">-InstanceName</span></span>
<span data-ttu-id="4a8e7-128">Azure SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="4a8e7-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4a8e7-129">-PassThru</span></span>
<span data-ttu-id="4a8e7-130">Cmdlet 'in yürütülmesinin sonunda duyarlılık sınıflandırması modelinin çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="4a8e7-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="4a8e7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a8e7-131">-ResourceGroupName</span></span>
<span data-ttu-id="4a8e7-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a8e7-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4a8e7-133">-SchemaName</span></span>
<span data-ttu-id="4a8e7-134">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-134">Name of schema.</span></span>

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

### <span data-ttu-id="4a8e7-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="4a8e7-135">-TableName</span></span>
<span data-ttu-id="4a8e7-136">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-136">Name of table.</span></span>

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

### <span data-ttu-id="4a8e7-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a8e7-137">-Confirm</span></span>
<span data-ttu-id="4a8e7-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a8e7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a8e7-139">-WhatIf</span></span>
<span data-ttu-id="4a8e7-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a8e7-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a8e7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a8e7-142">CommonParameters</span></span>
<span data-ttu-id="4a8e7-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a8e7-144">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4a8e7-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a8e7-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a8e7-145">INPUTS</span></span>

### <span data-ttu-id="4a8e7-146">Microsoft. Azure. Commands. Sql. DataClassification. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="4a8e7-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="4a8e7-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a8e7-147">OUTPUTS</span></span>

### <span data-ttu-id="4a8e7-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4a8e7-148">System.Boolean</span></span>

## <span data-ttu-id="4a8e7-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a8e7-149">NOTES</span></span>

## <span data-ttu-id="4a8e7-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a8e7-150">RELATED LINKS</span></span>

[<span data-ttu-id="4a8e7-151">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="4a8e7-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)