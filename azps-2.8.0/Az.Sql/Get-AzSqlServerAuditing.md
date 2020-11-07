---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: cf9bea67027e7a2c5e3928755f6d88b1dc124489
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933880"
---
# <span data-ttu-id="5711e-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="5711e-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="5711e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5711e-102">SYNOPSIS</span></span>
<span data-ttu-id="5711e-103">**Önemli: Bu cmdlet kullanım dışıdır, [Get-AzSqlServerAudit yerini alır](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) .**</span><span class="sxs-lookup"><span data-stu-id="5711e-103">**Important: This cmdlet is deprecated, [Get-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="5711e-104">Bir Azure SQL Server 'ın denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5711e-104">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="5711e-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5711e-105">SYNTAX</span></span>

### <span data-ttu-id="5711e-106">DefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5711e-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5711e-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="5711e-107">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5711e-108">Günlük çözümlemesi</span><span class="sxs-lookup"><span data-stu-id="5711e-108">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5711e-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="5711e-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5711e-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="5711e-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5711e-111">Loganalyzer Ticsbyparentresourceset</span><span class="sxs-lookup"><span data-stu-id="5711e-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5711e-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="5711e-112">DESCRIPTION</span></span>
<span data-ttu-id="5711e-113">**Get-AzSqlServerAuditing** cmdlet 'i, BIR Azure SQL Server 'ın denetim ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5711e-113">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="5711e-114">Sunucuyu tanımlayan *Resourcegroupname* ve *ServerName* parametrelerini belirtin.</span><span class="sxs-lookup"><span data-stu-id="5711e-114">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="5711e-115">Denetim günlükleri hedefi, aşağıdaki Switch parametrelerinden biri belirtilerek belirlenir: BlobStorage, LogAnalytics veya EventHub (hiçbiri belirtilmemişse, varsayılan BlobStorage olur).</span><span class="sxs-lookup"><span data-stu-id="5711e-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="5711e-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5711e-116">EXAMPLES</span></span>

### <span data-ttu-id="5711e-117">Örnek 1: Azure SQL Server 'ın BLOB depolama denetimi ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="5711e-117">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="5711e-118">Örnek 2: Azure SQL Server 'ın BLOB depolama denetimi ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="5711e-118">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="5711e-119">Örnek 3: Azure SQL Server 'ın BLOB depolama denetimi ayarları</span><span class="sxs-lookup"><span data-stu-id="5711e-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="5711e-120">Örnek 4: Azure SQL Server 'ın Olay Hub denetimini alma</span><span class="sxs-lookup"><span data-stu-id="5711e-120">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="5711e-121">Örnek 5: bir Azure SQL Server 'ın Olay Hub denetimini gözden geçirme</span><span class="sxs-lookup"><span data-stu-id="5711e-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="5711e-122">Örnek 6: Azure SQL Server 'ın Log Analytics denetim ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="5711e-122">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="5711e-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5711e-123">PARAMETERS</span></span>

### <span data-ttu-id="5711e-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="5711e-124">-BlobStorage</span></span>
<span data-ttu-id="5711e-125">Denetim günlükleri hedefinin blob depolaması olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="5711e-125">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5711e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5711e-126">-DefaultProfile</span></span>
<span data-ttu-id="5711e-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5711e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5711e-128">-EventHub</span><span class="sxs-lookup"><span data-stu-id="5711e-128">-EventHub</span></span>
<span data-ttu-id="5711e-129">Denetim günlükleri hedefinin Olay Hub olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="5711e-129">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5711e-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5711e-130">-InputObject</span></span>
<span data-ttu-id="5711e-131">Denetim ilkesini yönetmek için sunucu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5711e-131">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5711e-132">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="5711e-132">-LogAnalytics</span></span>
<span data-ttu-id="5711e-133">Denetim günlükleri hedefinin Günlük Analizi olduğunu belirtir</span><span class="sxs-lookup"><span data-stu-id="5711e-133">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5711e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5711e-134">-ResourceGroupName</span></span>
<span data-ttu-id="5711e-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5711e-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5711e-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5711e-136">-ServerName</span></span>
<span data-ttu-id="5711e-137">SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="5711e-137">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5711e-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="5711e-138">-Confirm</span></span>
<span data-ttu-id="5711e-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5711e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5711e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5711e-140">-WhatIf</span></span>
<span data-ttu-id="5711e-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5711e-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5711e-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5711e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5711e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5711e-143">CommonParameters</span></span>
<span data-ttu-id="5711e-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5711e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5711e-145">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5711e-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5711e-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5711e-146">INPUTS</span></span>

### <span data-ttu-id="5711e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="5711e-147">System.String</span></span>

### <span data-ttu-id="5711e-148">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="5711e-148">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="5711e-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5711e-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5711e-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5711e-150">OUTPUTS</span></span>

### <span data-ttu-id="5711e-151">Microsoft. Azure. Commands. Sql. Auditing. model. Serverblobobauditingsettingsmodel</span><span class="sxs-lookup"><span data-stu-id="5711e-151">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="5711e-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5711e-152">NOTES</span></span>

## <span data-ttu-id="5711e-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5711e-153">RELATED LINKS</span></span>
