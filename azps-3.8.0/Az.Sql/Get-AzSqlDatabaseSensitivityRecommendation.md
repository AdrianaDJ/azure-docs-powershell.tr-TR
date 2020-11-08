---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097099"
---
# <span data-ttu-id="2b6c4-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="2b6c4-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="2b6c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6c4-103">Veritabanındaki sütunların önerilen bilgi türlerini ve duyarlılık etiketlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="2b6c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b6c4-104">SYNTAX</span></span>

### <span data-ttu-id="2b6c4-105">DatabaseObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b6c4-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b6c4-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b6c4-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b6c4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b6c4-107">DESCRIPTION</span></span>
<span data-ttu-id="2b6c4-108">Get-AzSqlDatabaseSensitivityRecommendation cmdlet 'i veritabanındaki sütunların önerilen bilgi türlerini ve duyarlılık etiketlerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="2b6c4-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b6c4-109">EXAMPLES</span></span>

### <span data-ttu-id="2b6c4-110">Örnek 1: Azure SQL veritabanının önerilen bilgi türlerini ve duyarlılık etiketlerini alma.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
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

### <span data-ttu-id="2b6c4-111">Örnek 2: yöneltme kullanarak bir Azure SQL veritabanının önerilen bilgi türlerini ve duyarlılık etiketlerini alma.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
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

## <span data-ttu-id="2b6c4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b6c4-112">PARAMETERS</span></span>

### <span data-ttu-id="2b6c4-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="2b6c4-113">-AsJob</span></span>
<span data-ttu-id="2b6c4-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2b6c4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b6c4-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b6c4-115">-DatabaseName</span></span>
<span data-ttu-id="2b6c4-116">Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="2b6c4-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2b6c4-117">-DatabaseObject</span></span>
<span data-ttu-id="2b6c4-118">SQL veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6c4-119">-DefaultProfile</span></span>
<span data-ttu-id="2b6c4-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b6c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b6c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="2b6c4-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b6c4-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2b6c4-123">-ServerName</span></span>
<span data-ttu-id="2b6c4-124">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-124">SQL server name.</span></span>

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

### <span data-ttu-id="2b6c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6c4-125">CommonParameters</span></span>
<span data-ttu-id="2b6c4-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6c4-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2b6c4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6c4-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b6c4-128">INPUTS</span></span>

### <span data-ttu-id="2b6c4-129">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="2b6c4-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="2b6c4-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b6c4-130">OUTPUTS</span></span>

### <span data-ttu-id="2b6c4-131">Microsoft. Azure. Commands. Sql. DataClassification. model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="2b6c4-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="2b6c4-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b6c4-132">NOTES</span></span>

## <span data-ttu-id="2b6c4-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b6c4-133">RELATED LINKS</span></span>

[<span data-ttu-id="2b6c4-134">Azure SQL veritabanı veri bulma ve sınıflandırma hakkında daha fazla bilgi edinin</span><span class="sxs-lookup"><span data-stu-id="2b6c4-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)