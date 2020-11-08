---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107576"
---
# <span data-ttu-id="15c04-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="15c04-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="15c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15c04-102">SYNOPSIS</span></span>
<span data-ttu-id="15c04-103">Tüm sütunlarda duyarlılık önerilerini (tüm sütunlarda varsayılan olarak etkindir) Azure SQL yönetilen örnek veritabanında etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="15c04-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="15c04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15c04-104">SYNTAX</span></span>

### <span data-ttu-id="15c04-105">Inputobjectparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15c04-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c04-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c04-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15c04-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="15c04-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15c04-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="15c04-108">DESCRIPTION</span></span>
<span data-ttu-id="15c04-109">Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet 'i Azure SQL yönetilen örnek veritabanındaki sütunlarda duyarlılık önerilerini etkinleştirmektedir.</span><span class="sxs-lookup"><span data-stu-id="15c04-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="15c04-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15c04-110">EXAMPLES</span></span>

### <span data-ttu-id="15c04-111">Örnek 1: Azure SQL yönetilen örnek veritabanındaki belirli bir sütunda duyarlılık önerilerini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="15c04-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="15c04-112">Örnek 2: bir Azure SQL yönetilen örnek veritabanında, boruları ile duyarlılık önerilerini etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="15c04-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="15c04-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15c04-113">PARAMETERS</span></span>

### <span data-ttu-id="15c04-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="15c04-114">-AsJob</span></span>
<span data-ttu-id="15c04-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="15c04-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15c04-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="15c04-116">-ColumnName</span></span>
<span data-ttu-id="15c04-117">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="15c04-117">Name of column.</span></span>

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

### <span data-ttu-id="15c04-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="15c04-118">-DatabaseName</span></span>
<span data-ttu-id="15c04-119">Azure SQL yönetilen örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="15c04-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="15c04-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="15c04-120">-DatabaseObject</span></span>
<span data-ttu-id="15c04-121">Azure SQL yönetilen örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="15c04-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="15c04-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c04-122">-DefaultProfile</span></span>
<span data-ttu-id="15c04-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15c04-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c04-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15c04-124">-InputObject</span></span>
<span data-ttu-id="15c04-125">SQL yönetilen örnek veritabanı duyarlılığı sınıflandırmasını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="15c04-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15c04-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="15c04-126">-InstanceName</span></span>
<span data-ttu-id="15c04-127">Azure SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="15c04-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="15c04-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="15c04-128">-PassThru</span></span>
<span data-ttu-id="15c04-129">Cmdlet 'in yürütülmesinin sonunda duyarlılık sınıflandırması modelinin çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="15c04-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="15c04-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c04-130">-ResourceGroupName</span></span>
<span data-ttu-id="15c04-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="15c04-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="15c04-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="15c04-132">-SchemaName</span></span>
<span data-ttu-id="15c04-133">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="15c04-133">Name of schema.</span></span>

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

### <span data-ttu-id="15c04-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="15c04-134">-TableName</span></span>
<span data-ttu-id="15c04-135">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="15c04-135">Name of table.</span></span>

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

### <span data-ttu-id="15c04-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="15c04-136">-Confirm</span></span>
<span data-ttu-id="15c04-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15c04-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c04-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c04-138">-WhatIf</span></span>
<span data-ttu-id="15c04-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15c04-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15c04-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15c04-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c04-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c04-141">CommonParameters</span></span>
<span data-ttu-id="15c04-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15c04-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c04-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15c04-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c04-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15c04-144">INPUTS</span></span>

### <span data-ttu-id="15c04-145">Microsoft. Azure. Commands. Sql. DataClassification. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="15c04-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="15c04-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15c04-146">OUTPUTS</span></span>

### <span data-ttu-id="15c04-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15c04-147">System.Boolean</span></span>

## <span data-ttu-id="15c04-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15c04-148">NOTES</span></span>

## <span data-ttu-id="15c04-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15c04-149">RELATED LINKS</span></span>

[<span data-ttu-id="15c04-150">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="15c04-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)