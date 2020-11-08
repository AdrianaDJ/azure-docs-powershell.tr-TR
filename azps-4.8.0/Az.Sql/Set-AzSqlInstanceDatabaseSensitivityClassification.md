---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: f524c8b30f609cb2fef3fb3f59550078b26b11b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108614"
---
# <span data-ttu-id="cf1d7-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="cf1d7-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="cf1d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf1d7-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1d7-103">Azure SQL yönetilen örnek veritabanındaki sütunların bilgi türlerini ve duyarlılık etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="cf1d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf1d7-104">SYNTAX</span></span>

### <span data-ttu-id="cf1d7-105">ClassificationObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf1d7-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf1d7-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf1d7-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf1d7-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf1d7-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf1d7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf1d7-108">DESCRIPTION</span></span>
<span data-ttu-id="cf1d7-109">Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet 'i Azure SQL yönetilen örnek veritabanındaki sütunların bilgi türlerini ve duyarlılık etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="cf1d7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf1d7-110">EXAMPLES</span></span>

### <span data-ttu-id="cf1d7-111">Örnek 1: Azure SQL yönetilen örnek veritabanındaki bir sütunun bilgi türü ve duyarlılık etiketini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="cf1d7-112">Örnek 2: Azure SQL yönetilen örnek veritabanındaki sütunların önerilen bilgi türlerini ve duyarlılık etiketlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="cf1d7-113">Örnek 3: yöneltme kullanarak Azure SQL yönetilen örnek veritabanındaki bir sütunun bilgi türü ve duyarlılık etiketini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="cf1d7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf1d7-114">PARAMETERS</span></span>

### <span data-ttu-id="cf1d7-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="cf1d7-115">-AsJob</span></span>
<span data-ttu-id="cf1d7-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cf1d7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf1d7-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="cf1d7-117">-ClassificationObject</span></span>
<span data-ttu-id="cf1d7-118">SQL yönetilen örnek veritabanı duyarlılığı sınıflandırmasını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="cf1d7-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="cf1d7-119">-ColumnName</span></span>
<span data-ttu-id="cf1d7-120">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-120">Name of column.</span></span>

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

### <span data-ttu-id="cf1d7-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cf1d7-121">-DatabaseName</span></span>
<span data-ttu-id="cf1d7-122">Azure SQL yönetilen örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="cf1d7-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="cf1d7-123">-DatabaseObject</span></span>
<span data-ttu-id="cf1d7-124">Azure SQL yönetilen örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="cf1d7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf1d7-125">-DefaultProfile</span></span>
<span data-ttu-id="cf1d7-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf1d7-127">-Informationtype</span><span class="sxs-lookup"><span data-stu-id="cf1d7-127">-InformationType</span></span>
<span data-ttu-id="cf1d7-128">Sütunda depolanan verilerin bilgi türünü açıklayan ad.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="cf1d7-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="cf1d7-129">-InstanceName</span></span>
<span data-ttu-id="cf1d7-130">Azure SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="cf1d7-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cf1d7-131">-PassThru</span></span>
<span data-ttu-id="cf1d7-132">Cmdlet 'in yürütülmesinin sonunda duyarlılık sınıflandırması modelinin çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="cf1d7-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="cf1d7-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf1d7-133">-ResourceGroupName</span></span>
<span data-ttu-id="cf1d7-134">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="cf1d7-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cf1d7-135">-SchemaName</span></span>
<span data-ttu-id="cf1d7-136">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-136">Name of schema.</span></span>

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

### <span data-ttu-id="cf1d7-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="cf1d7-137">-SensitivityLabel</span></span>
<span data-ttu-id="cf1d7-138">Sütunda depolanan verilerin duyarlılığını açıklayan ad.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="cf1d7-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="cf1d7-139">-TableName</span></span>
<span data-ttu-id="cf1d7-140">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-140">Name of table.</span></span>

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

### <span data-ttu-id="cf1d7-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="cf1d7-141">-Confirm</span></span>
<span data-ttu-id="cf1d7-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf1d7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf1d7-143">-WhatIf</span></span>
<span data-ttu-id="cf1d7-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf1d7-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf1d7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1d7-146">CommonParameters</span></span>
<span data-ttu-id="cf1d7-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1d7-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cf1d7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1d7-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf1d7-149">INPUTS</span></span>

### <span data-ttu-id="cf1d7-150">Microsoft. Azure. Commands. Sql. DataClassification. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="cf1d7-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="cf1d7-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf1d7-151">OUTPUTS</span></span>

### <span data-ttu-id="cf1d7-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf1d7-152">System.Boolean</span></span>

## <span data-ttu-id="cf1d7-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf1d7-153">NOTES</span></span>

## <span data-ttu-id="cf1d7-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf1d7-154">RELATED LINKS</span></span>

[<span data-ttu-id="cf1d7-155">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="cf1d7-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
