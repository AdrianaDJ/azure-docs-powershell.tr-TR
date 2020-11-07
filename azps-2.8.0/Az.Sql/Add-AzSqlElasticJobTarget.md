---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: d1788abc6ac0546732fe2476cf2822210a1fa8da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932399"
---
# <span data-ttu-id="e53cd-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="e53cd-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="e53cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e53cd-102">SYNOPSIS</span></span>
<span data-ttu-id="e53cd-103">Hedef gruba hedef ekler</span><span class="sxs-lookup"><span data-stu-id="e53cd-103">Adds a target to a target group</span></span>

## <span data-ttu-id="e53cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e53cd-104">SYNTAX</span></span>

### <span data-ttu-id="e53cd-105">SqlDatabase (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e53cd-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53cd-106">Sqlserverorelaçıkartma</span><span class="sxs-lookup"><span data-stu-id="e53cd-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e53cd-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="e53cd-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53cd-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e53cd-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53cd-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e53cd-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53cd-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e53cd-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53cd-111">Sqldatabaseusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="e53cd-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53cd-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e53cd-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e53cd-113">Sqlshardmapusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="e53cd-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e53cd-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="e53cd-114">DESCRIPTION</span></span>
<span data-ttu-id="e53cd-115">Add-AzSqlElasticJobTarget cmdlet 'i hedef bir gruba hedef kaynak ekler</span><span class="sxs-lookup"><span data-stu-id="e53cd-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="e53cd-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e53cd-116">EXAMPLES</span></span>

### <span data-ttu-id="e53cd-117">Örnek 1-sunucu hedefi ekleme</span><span class="sxs-lookup"><span data-stu-id="e53cd-117">Example 1 - Add a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="e53cd-118">Örnek 2-veritabanı hedefi ekleme</span><span class="sxs-lookup"><span data-stu-id="e53cd-118">Example 2 - Add a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="e53cd-119">Örnek 3-elastik havuz hedefi ekleme</span><span class="sxs-lookup"><span data-stu-id="e53cd-119">Example 3 - Add an elastic pool target</span></span>
```
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="e53cd-120">Örnek 4-bir üst harita hedefi ekleme</span><span class="sxs-lookup"><span data-stu-id="e53cd-120">Example 4 - Add a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="e53cd-121">Hedef gruba hedef (sunucu, esnek havuz, veritabanı ve Shard Haritası) ekler</span><span class="sxs-lookup"><span data-stu-id="e53cd-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="e53cd-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e53cd-122">PARAMETERS</span></span>

### <span data-ttu-id="e53cd-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e53cd-123">-AgentName</span></span>
<span data-ttu-id="e53cd-124">Aracı adı.</span><span class="sxs-lookup"><span data-stu-id="e53cd-124">The agent name.</span></span>

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

### <span data-ttu-id="e53cd-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="e53cd-125">-AgentServerName</span></span>
<span data-ttu-id="e53cd-126">Sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="e53cd-126">The server name.</span></span>

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

### <span data-ttu-id="e53cd-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e53cd-127">-DatabaseName</span></span>
<span data-ttu-id="e53cd-128">Veritabanı hedef adı</span><span class="sxs-lookup"><span data-stu-id="e53cd-128">Database Target Name</span></span>

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

### <span data-ttu-id="e53cd-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e53cd-129">-DefaultProfile</span></span>
<span data-ttu-id="e53cd-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e53cd-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e53cd-131">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="e53cd-131">-ElasticPoolName</span></span>
<span data-ttu-id="e53cd-132">Elastik havuz hedef adı</span><span class="sxs-lookup"><span data-stu-id="e53cd-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="e53cd-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="e53cd-133">-Exclude</span></span>
<span data-ttu-id="e53cd-134">Hedefi dışlar.</span><span class="sxs-lookup"><span data-stu-id="e53cd-134">Excludes a target.</span></span>

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

### <span data-ttu-id="e53cd-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e53cd-135">-ParentObject</span></span>
<span data-ttu-id="e53cd-136">Hedef Grup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e53cd-136">The target group object.</span></span>

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

### <span data-ttu-id="e53cd-137">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="e53cd-137">-ParentResourceId</span></span>
<span data-ttu-id="e53cd-138">Hedef Grup kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e53cd-138">The target group resource id.</span></span>

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

### <span data-ttu-id="e53cd-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="e53cd-139">-RefreshCredentialName</span></span>
<span data-ttu-id="e53cd-140">Kimlik bilgileri yenileme</span><span class="sxs-lookup"><span data-stu-id="e53cd-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="e53cd-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e53cd-141">-ResourceGroupName</span></span>
<span data-ttu-id="e53cd-142">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e53cd-142">Resource Group Name</span></span>

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

### <span data-ttu-id="e53cd-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e53cd-143">-ServerName</span></span>
<span data-ttu-id="e53cd-144">Sunucu hedef adı</span><span class="sxs-lookup"><span data-stu-id="e53cd-144">Server Target Name</span></span>

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

### <span data-ttu-id="e53cd-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="e53cd-145">-ShardMapName</span></span>
<span data-ttu-id="e53cd-146">Shard harita hedef adı</span><span class="sxs-lookup"><span data-stu-id="e53cd-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="e53cd-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="e53cd-147">-TargetGroupName</span></span>
<span data-ttu-id="e53cd-148">Hedef grup adı.</span><span class="sxs-lookup"><span data-stu-id="e53cd-148">The target group name.</span></span>

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

### <span data-ttu-id="e53cd-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="e53cd-149">-Confirm</span></span>
<span data-ttu-id="e53cd-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e53cd-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e53cd-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e53cd-151">-WhatIf</span></span>
<span data-ttu-id="e53cd-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e53cd-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e53cd-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e53cd-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e53cd-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e53cd-154">CommonParameters</span></span>
<span data-ttu-id="e53cd-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e53cd-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e53cd-156">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e53cd-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e53cd-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e53cd-157">INPUTS</span></span>

### <span data-ttu-id="e53cd-158">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobtargetgroupmodel</span><span class="sxs-lookup"><span data-stu-id="e53cd-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="e53cd-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e53cd-159">OUTPUTS</span></span>

### <span data-ttu-id="e53cd-160">Microsoft. Azure. Management. Sql. modeller. JobTarget</span><span class="sxs-lookup"><span data-stu-id="e53cd-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="e53cd-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e53cd-161">NOTES</span></span>

## <span data-ttu-id="e53cd-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e53cd-162">RELATED LINKS</span></span>
