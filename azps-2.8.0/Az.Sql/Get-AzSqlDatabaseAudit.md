---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAudit.md
ms.openlocfilehash: 24cc7df97e5942b966d1857052ce647150ccd817
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933900"
---
# <span data-ttu-id="841c8-101">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="841c8-101">Get-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="841c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="841c8-102">SYNOPSIS</span></span>
<span data-ttu-id="841c8-103">Bir Azure SQL veritabanının denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="841c8-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="841c8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="841c8-104">SYNTAX</span></span>

### <span data-ttu-id="841c8-105">DatabaseParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="841c8-105">DatabaseParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAudit [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="841c8-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="841c8-106">DatabaseObjectParameterSet</span></span>
```
Get-AzSqlDatabaseAudit -DatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="841c8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="841c8-107">DESCRIPTION</span></span>
<span data-ttu-id="841c8-108">**Get-AzSqlDatabaseAudit** cmdlet 'ı BIR Azure SQL veritabanının denetleme ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="841c8-108">The **Get-AzSqlDatabaseAudit** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="841c8-109">Cmdlet 'i kullanmak için, *Resourcegroupname* , *ServerName* ve *DatabaseName* parametrelerini kullanarak veritabanını belirleyin.</span><span class="sxs-lookup"><span data-stu-id="841c8-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>

## <span data-ttu-id="841c8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="841c8-110">EXAMPLES</span></span>

### <span data-ttu-id="841c8-111">Örnek 1: Azure SQL veritabanının denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="841c8-111">Example 1: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="841c8-112">Örnek 2: Azure SQL veritabanının denetim ayarlarını ardışık düzen ile edinme</span><span class="sxs-lookup"><span data-stu-id="841c8-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAudit
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="841c8-113">Örnek 3: Azure SQL veritabanının denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="841c8-113">Example 3: Get the auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Disabled
WorkspaceResourceId                 :
```

## <span data-ttu-id="841c8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="841c8-114">PARAMETERS</span></span>

### <span data-ttu-id="841c8-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="841c8-115">-DatabaseName</span></span>
<span data-ttu-id="841c8-116">SQL veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="841c8-116">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="841c8-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="841c8-117">-DatabaseObject</span></span>
<span data-ttu-id="841c8-118">Denetim ilkesini yönetmek için veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="841c8-118">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="841c8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841c8-119">-DefaultProfile</span></span>
<span data-ttu-id="841c8-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="841c8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="841c8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="841c8-121">-ResourceGroupName</span></span>
<span data-ttu-id="841c8-122">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="841c8-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="841c8-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="841c8-123">-ServerName</span></span>
<span data-ttu-id="841c8-124">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="841c8-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="841c8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841c8-125">CommonParameters</span></span>
<span data-ttu-id="841c8-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="841c8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841c8-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="841c8-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841c8-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="841c8-128">INPUTS</span></span>

### <span data-ttu-id="841c8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="841c8-129">System.String</span></span>

### <span data-ttu-id="841c8-130">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="841c8-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="841c8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="841c8-131">OUTPUTS</span></span>

### <span data-ttu-id="841c8-132">Microsoft. Azure. Commands. Sql. Auditing. model. DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="841c8-132">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="841c8-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="841c8-133">NOTES</span></span>

## <span data-ttu-id="841c8-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="841c8-134">RELATED LINKS</span></span>
