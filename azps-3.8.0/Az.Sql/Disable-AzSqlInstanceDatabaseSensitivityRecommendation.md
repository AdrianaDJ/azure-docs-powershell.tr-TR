---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098433"
---
# <span data-ttu-id="8164b-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="8164b-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="8164b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8164b-102">SYNOPSIS</span></span>
<span data-ttu-id="8164b-103">Azure SQL yönetilen örnek veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8164b-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="8164b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8164b-104">SYNTAX</span></span>

### <span data-ttu-id="8164b-105">Inputobjectparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8164b-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8164b-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8164b-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8164b-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="8164b-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8164b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8164b-108">DESCRIPTION</span></span>
<span data-ttu-id="8164b-109">Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet, Azure SQL yönetilen örnek veritabanındaki sütunlarda duyarlılık önerilerini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="8164b-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="8164b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8164b-110">EXAMPLES</span></span>

### <span data-ttu-id="8164b-111">Örnek 1: Azure SQL yönetilen örnek veritabanındaki belirli bir sütunda duyarlılık önerilerini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="8164b-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="8164b-112">Örnek 2: yöneltme ile Azure SQL yönetilen örnek veritabanında, duyarlılık önerilerini içeren sütunlarda duyarlılık önerilerini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="8164b-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="8164b-113">Örnek 3: yöneltme ile Azure SQL yönetilen örnek veritabanındaki belirli bir sütunda duyarlılık önerilerini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="8164b-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="8164b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8164b-114">PARAMETERS</span></span>

### <span data-ttu-id="8164b-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="8164b-115">-AsJob</span></span>
<span data-ttu-id="8164b-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8164b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8164b-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="8164b-117">-ColumnName</span></span>
<span data-ttu-id="8164b-118">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="8164b-118">Name of column.</span></span>

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

### <span data-ttu-id="8164b-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8164b-119">-DatabaseName</span></span>
<span data-ttu-id="8164b-120">Azure SQL yönetilen örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="8164b-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="8164b-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8164b-121">-DatabaseObject</span></span>
<span data-ttu-id="8164b-122">Azure SQL yönetilen örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8164b-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="8164b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8164b-123">-DefaultProfile</span></span>
<span data-ttu-id="8164b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8164b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8164b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8164b-125">-InputObject</span></span>
<span data-ttu-id="8164b-126">SQL yönetilen örnek veritabanı duyarlılığı sınıflandırmasını temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="8164b-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="8164b-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="8164b-127">-InstanceName</span></span>
<span data-ttu-id="8164b-128">Azure SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="8164b-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="8164b-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8164b-129">-PassThru</span></span>
<span data-ttu-id="8164b-130">Cmdlet 'in yürütülmesinin sonunda duyarlılık sınıflandırması modelinin çıkışını belirtir</span><span class="sxs-lookup"><span data-stu-id="8164b-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="8164b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8164b-131">-ResourceGroupName</span></span>
<span data-ttu-id="8164b-132">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="8164b-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="8164b-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="8164b-133">-SchemaName</span></span>
<span data-ttu-id="8164b-134">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="8164b-134">Name of schema.</span></span>

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

### <span data-ttu-id="8164b-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="8164b-135">-TableName</span></span>
<span data-ttu-id="8164b-136">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="8164b-136">Name of table.</span></span>

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

### <span data-ttu-id="8164b-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="8164b-137">-Confirm</span></span>
<span data-ttu-id="8164b-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8164b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8164b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8164b-139">-WhatIf</span></span>
<span data-ttu-id="8164b-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8164b-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8164b-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8164b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8164b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8164b-142">CommonParameters</span></span>
<span data-ttu-id="8164b-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8164b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8164b-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8164b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8164b-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8164b-145">INPUTS</span></span>

### <span data-ttu-id="8164b-146">Microsoft. Azure. Commands. Sql. DataClassification. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="8164b-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="8164b-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8164b-147">OUTPUTS</span></span>

### <span data-ttu-id="8164b-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8164b-148">System.Boolean</span></span>

## <span data-ttu-id="8164b-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8164b-149">NOTES</span></span>

## <span data-ttu-id="8164b-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8164b-150">RELATED LINKS</span></span>

[<span data-ttu-id="8164b-151">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="8164b-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)