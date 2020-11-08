---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 89190f171ec9634e13eaa56499f6eca87e75ccf5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933613"
---
# <span data-ttu-id="91e4a-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="91e4a-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="91e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="91e4a-103">Azure SQL yönetilen örnek veritabanındaki sütunların geçerli bilgi türlerini ve duyarlılık etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="91e4a-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="91e4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91e4a-104">SYNTAX</span></span>

### <span data-ttu-id="91e4a-105">DatabaseObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91e4a-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91e4a-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="91e4a-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91e4a-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="91e4a-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91e4a-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="91e4a-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91e4a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="91e4a-109">DESCRIPTION</span></span>
<span data-ttu-id="91e4a-110">Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet 'i Azure SQL yönetilen örnek veritabanındaki sütunların geçerli bilgi türlerini ve duyarlılık etiketlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="91e4a-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="91e4a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91e4a-111">EXAMPLES</span></span>

### <span data-ttu-id="91e4a-112">Örnek 1: Azure SQL yönetilen örnek veritabanının geçerli bilgi türlerini ve duyarlılık etiketlerini alma.</span><span class="sxs-lookup"><span data-stu-id="91e4a-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="91e4a-113">Örnek 2: yöneltme ile Azure SQL yönetilen örnek veritabanının güncel bilgi türlerini ve duyarlılık etiketlerini alma.</span><span class="sxs-lookup"><span data-stu-id="91e4a-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="91e4a-114">Örnek 3: Azure SQL yönetilen örnek veritabanının belirli bir sütununun geçerli bilgi türü ve duyarlılık etiketini alma.</span><span class="sxs-lookup"><span data-stu-id="91e4a-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="91e4a-115">Örnek 4: yöneltme kullanarak Azure SQL yönetilen örnek veritabanının belirli bir sütununun geçerli bilgi türü ve duyarlılık etiketini alma.</span><span class="sxs-lookup"><span data-stu-id="91e4a-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="91e4a-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91e4a-116">PARAMETERS</span></span>

### <span data-ttu-id="91e4a-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="91e4a-117">-AsJob</span></span>
<span data-ttu-id="91e4a-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="91e4a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91e4a-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="91e4a-119">-ColumnName</span></span>
<span data-ttu-id="91e4a-120">Sütun adı.</span><span class="sxs-lookup"><span data-stu-id="91e4a-120">Name of column.</span></span>

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

### <span data-ttu-id="91e4a-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="91e4a-121">-DatabaseName</span></span>
<span data-ttu-id="91e4a-122">Azure SQL yönetilen örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="91e4a-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="91e4a-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="91e4a-123">-DatabaseObject</span></span>
<span data-ttu-id="91e4a-124">Azure SQL yönetilen örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="91e4a-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91e4a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91e4a-125">-DefaultProfile</span></span>
<span data-ttu-id="91e4a-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91e4a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91e4a-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="91e4a-127">-InstanceName</span></span>
<span data-ttu-id="91e4a-128">Azure SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="91e4a-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="91e4a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91e4a-129">-ResourceGroupName</span></span>
<span data-ttu-id="91e4a-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="91e4a-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="91e4a-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="91e4a-131">-SchemaName</span></span>
<span data-ttu-id="91e4a-132">Şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="91e4a-132">Name of schema.</span></span>

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

### <span data-ttu-id="91e4a-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="91e4a-133">-TableName</span></span>
<span data-ttu-id="91e4a-134">Tablo adı.</span><span class="sxs-lookup"><span data-stu-id="91e4a-134">Name of table.</span></span>

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

### <span data-ttu-id="91e4a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91e4a-135">CommonParameters</span></span>
<span data-ttu-id="91e4a-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91e4a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91e4a-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="91e4a-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91e4a-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91e4a-138">INPUTS</span></span>

### <span data-ttu-id="91e4a-139">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="91e4a-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="91e4a-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91e4a-140">OUTPUTS</span></span>

### <span data-ttu-id="91e4a-141">Microsoft. Azure. Commands. Sql. DataClassification. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="91e4a-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="91e4a-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91e4a-142">NOTES</span></span>

## <span data-ttu-id="91e4a-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91e4a-143">RELATED LINKS</span></span>

[<span data-ttu-id="91e4a-144">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="91e4a-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)