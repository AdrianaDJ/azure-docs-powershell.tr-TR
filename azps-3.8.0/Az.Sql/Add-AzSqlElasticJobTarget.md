---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: 6ade592fde11c3bd614f602070fba87b60cdcda3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096749"
---
# <span data-ttu-id="7c583-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="7c583-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="7c583-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c583-102">SYNOPSIS</span></span>
<span data-ttu-id="7c583-103">Hedef gruba hedef ekler</span><span class="sxs-lookup"><span data-stu-id="7c583-103">Adds a target to a target group</span></span>

## <span data-ttu-id="7c583-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c583-104">SYNTAX</span></span>

### <span data-ttu-id="7c583-105">SqlDatabase (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7c583-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c583-106">Sqlserverorelaçıkartma</span><span class="sxs-lookup"><span data-stu-id="7c583-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c583-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="7c583-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c583-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7c583-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c583-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7c583-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c583-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7c583-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c583-111">Sqldatabaseusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7c583-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c583-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7c583-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c583-113">Sqlshardmapusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7c583-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c583-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c583-114">DESCRIPTION</span></span>
<span data-ttu-id="7c583-115">Add-AzSqlElasticJobTarget cmdlet 'i hedef bir gruba hedef kaynak ekler</span><span class="sxs-lookup"><span data-stu-id="7c583-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="7c583-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c583-116">EXAMPLES</span></span>

### <span data-ttu-id="7c583-117">Örnek 1-sunucu hedefi ekleme</span><span class="sxs-lookup"><span data-stu-id="7c583-117">Example 1 - Add a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="7c583-118">Örnek 2-veritabanı hedefi ekleme</span><span class="sxs-lookup"><span data-stu-id="7c583-118">Example 2 - Add a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="7c583-119">Örnek 3-elastik havuz hedefi ekleme</span><span class="sxs-lookup"><span data-stu-id="7c583-119">Example 3 - Add an elastic pool target</span></span>
```
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="7c583-120">Örnek 4-bir üst harita hedefi ekleme</span><span class="sxs-lookup"><span data-stu-id="7c583-120">Example 4 - Add a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="7c583-121">Hedef gruba hedef (sunucu, esnek havuz, veritabanı ve Shard Haritası) ekler</span><span class="sxs-lookup"><span data-stu-id="7c583-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="7c583-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c583-122">PARAMETERS</span></span>

### <span data-ttu-id="7c583-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7c583-123">-AgentName</span></span>
<span data-ttu-id="7c583-124">Aracı adı.</span><span class="sxs-lookup"><span data-stu-id="7c583-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="7c583-125">-AgentServerName</span></span>
<span data-ttu-id="7c583-126">Sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="7c583-126">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7c583-127">-DatabaseName</span></span>
<span data-ttu-id="7c583-128">Veritabanı hedef adı</span><span class="sxs-lookup"><span data-stu-id="7c583-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c583-129">-DefaultProfile</span></span>
<span data-ttu-id="7c583-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c583-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c583-131">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="7c583-131">-ElasticPoolName</span></span>
<span data-ttu-id="7c583-132">Elastik havuz hedef adı</span><span class="sxs-lookup"><span data-stu-id="7c583-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="7c583-133">-Exclude</span></span>
<span data-ttu-id="7c583-134">Hedefi dışlar.</span><span class="sxs-lookup"><span data-stu-id="7c583-134">Excludes a target.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7c583-135">-ParentObject</span></span>
<span data-ttu-id="7c583-136">Hedef Grup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7c583-136">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-137">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7c583-137">-ParentResourceId</span></span>
<span data-ttu-id="7c583-138">Hedef Grup kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="7c583-138">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="7c583-139">-RefreshCredentialName</span></span>
<span data-ttu-id="7c583-140">Kimlik bilgileri yenileme</span><span class="sxs-lookup"><span data-stu-id="7c583-140">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c583-141">-ResourceGroupName</span></span>
<span data-ttu-id="7c583-142">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7c583-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7c583-143">-ServerName</span></span>
<span data-ttu-id="7c583-144">Sunucu hedef adı</span><span class="sxs-lookup"><span data-stu-id="7c583-144">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="7c583-145">-ShardMapName</span></span>
<span data-ttu-id="7c583-146">Shard harita hedef adı</span><span class="sxs-lookup"><span data-stu-id="7c583-146">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="7c583-147">-TargetGroupName</span></span>
<span data-ttu-id="7c583-148">Hedef grup adı.</span><span class="sxs-lookup"><span data-stu-id="7c583-148">The target group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="7c583-149">-Confirm</span></span>
<span data-ttu-id="7c583-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7c583-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c583-151">-WhatIf</span></span>
<span data-ttu-id="7c583-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c583-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c583-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7c583-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c583-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c583-154">CommonParameters</span></span>
<span data-ttu-id="7c583-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c583-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c583-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7c583-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c583-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c583-157">INPUTS</span></span>

### <span data-ttu-id="7c583-158">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobtargetgroupmodel</span><span class="sxs-lookup"><span data-stu-id="7c583-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="7c583-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c583-159">OUTPUTS</span></span>

### <span data-ttu-id="7c583-160">Microsoft. Azure. Management. Sql. modeller. JobTarget</span><span class="sxs-lookup"><span data-stu-id="7c583-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="7c583-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c583-161">NOTES</span></span>

## <span data-ttu-id="7c583-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c583-162">RELATED LINKS</span></span>
