---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAudit.md
ms.openlocfilehash: eda8123b9ff309f4834f6e954e5e0b1e01b3f1e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933595"
---
# <span data-ttu-id="a27d6-101">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="a27d6-101">Get-AzSqlServerAudit</span></span>

## <span data-ttu-id="a27d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a27d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a27d6-103">Bir Azure SQL Server 'ın denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a27d6-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="a27d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a27d6-104">SYNTAX</span></span>

### <span data-ttu-id="a27d6-105">Sunucuparametrekümesi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a27d6-105">ServerParameterSet (Default)</span></span>
```
Get-AzSqlServerAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a27d6-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a27d6-106">ServerObjectParameterSet</span></span>
```
Get-AzSqlServerAudit -ServerObject <AzureSqlServerModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a27d6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a27d6-107">DESCRIPTION</span></span>
<span data-ttu-id="a27d6-108">**Get-AzSqlServerAudit** cmdlet 'i, BIR Azure SQL Server 'ın denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a27d6-108">The **Get-AzSqlServerAudit** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="a27d6-109">Sunucuyu tanımlayan *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a27d6-109">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="a27d6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a27d6-110">EXAMPLES</span></span>

### <span data-ttu-id="a27d6-111">Örnek 1: Azure SQL Server 'ın denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="a27d6-111">Example 1: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

### <span data-ttu-id="a27d6-112">Örnek 2: Azure SQL Server 'ın denetim ayarlarını ardışık düzen ile edinme</span><span class="sxs-lookup"><span data-stu-id="a27d6-112">Example 2: Get, through pipeline, the auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAudit
ServerName                          : server01
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

### <span data-ttu-id="a27d6-113">Örnek 3: Azure SQL Server 'ın denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="a27d6-113">Example 3: Get the auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
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

## <span data-ttu-id="a27d6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a27d6-114">PARAMETERS</span></span>

### <span data-ttu-id="a27d6-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="a27d6-115">-AsJob</span></span>
<span data-ttu-id="a27d6-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a27d6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a27d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a27d6-117">-DefaultProfile</span></span>
<span data-ttu-id="a27d6-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a27d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a27d6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a27d6-119">-ResourceGroupName</span></span>
<span data-ttu-id="a27d6-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a27d6-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a27d6-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a27d6-121">-ServerName</span></span>
<span data-ttu-id="a27d6-122">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="a27d6-122">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a27d6-123">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="a27d6-123">-ServerObject</span></span>
<span data-ttu-id="a27d6-124">Denetim ilkesini yönetmek için sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a27d6-124">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a27d6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a27d6-125">CommonParameters</span></span>
<span data-ttu-id="a27d6-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a27d6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a27d6-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a27d6-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a27d6-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a27d6-128">INPUTS</span></span>

### <span data-ttu-id="a27d6-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a27d6-129">System.String</span></span>

### <span data-ttu-id="a27d6-130">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="a27d6-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="a27d6-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a27d6-131">OUTPUTS</span></span>

### <span data-ttu-id="a27d6-132">Microsoft. Azure. Commands. Sql. Auditing. model. ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="a27d6-132">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="a27d6-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a27d6-133">NOTES</span></span>

## <span data-ttu-id="a27d6-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a27d6-134">RELATED LINKS</span></span>
