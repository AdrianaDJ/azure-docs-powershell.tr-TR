---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279443"
---
# <span data-ttu-id="c2030-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="c2030-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="c2030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2030-102">SYNOPSIS</span></span>
<span data-ttu-id="c2030-103">Azure SQL yönetilen örnek veritabanındaki sütunların önerilen bilgi türlerini ve duyarlılık etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c2030-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="c2030-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2030-104">SYNTAX</span></span>

### <span data-ttu-id="c2030-105">DatabaseObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2030-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2030-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2030-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2030-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2030-107">DESCRIPTION</span></span>
<span data-ttu-id="c2030-108">Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet 'i Azure SQL yönetilen örnek veritabanındaki sütunların önerilen bilgi türlerini ve duyarlılık etiketlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c2030-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="c2030-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2030-109">EXAMPLES</span></span>

### <span data-ttu-id="c2030-110">Örnek 1: Azure SQL yönetilen örnek veritabanının önerilen bilgi türlerini ve duyarlılık etiketlerini alma.</span><span class="sxs-lookup"><span data-stu-id="c2030-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="c2030-111">Örnek 2: yöneltme kullanarak Azure SQL yönetilen örnek veritabanının önerilen bilgi türlerini ve duyarlılık etiketlerini alma.</span><span class="sxs-lookup"><span data-stu-id="c2030-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="c2030-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2030-112">PARAMETERS</span></span>

### <span data-ttu-id="c2030-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="c2030-113">-AsJob</span></span>
<span data-ttu-id="c2030-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c2030-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2030-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c2030-115">-DatabaseName</span></span>
<span data-ttu-id="c2030-116">Azure SQL yönetilen örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c2030-116">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2030-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c2030-117">-DatabaseObject</span></span>
<span data-ttu-id="c2030-118">Azure SQL yönetilen örnek veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c2030-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2030-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2030-119">-DefaultProfile</span></span>
<span data-ttu-id="c2030-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2030-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2030-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2030-121">-InstanceName</span></span>
<span data-ttu-id="c2030-122">Azure SQL yönetilen örnek adı.</span><span class="sxs-lookup"><span data-stu-id="c2030-122">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2030-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2030-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2030-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c2030-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2030-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2030-125">CommonParameters</span></span>
<span data-ttu-id="c2030-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2030-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2030-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c2030-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2030-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2030-128">INPUTS</span></span>

### <span data-ttu-id="c2030-129">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="c2030-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="c2030-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2030-130">OUTPUTS</span></span>

### <span data-ttu-id="c2030-131">Microsoft. Azure. Commands. Sql. DataClassification. model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="c2030-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="c2030-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2030-132">NOTES</span></span>

## <span data-ttu-id="c2030-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2030-133">RELATED LINKS</span></span>

[<span data-ttu-id="c2030-134">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="c2030-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
