---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266790"
---
# <span data-ttu-id="6e5e1-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="6e5e1-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="6e5e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5e1-103">Hedef gruptan hedefi kaldırır</span><span class="sxs-lookup"><span data-stu-id="6e5e1-103">Removes the target from the target group</span></span>

## <span data-ttu-id="6e5e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e5e1-104">SYNTAX</span></span>

### <span data-ttu-id="6e5e1-105">SqlDatabase (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e5e1-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e5e1-106">Sqlserverorelaçıkartma</span><span class="sxs-lookup"><span data-stu-id="6e5e1-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e5e1-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="6e5e1-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e5e1-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6e5e1-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e5e1-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6e5e1-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e5e1-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="6e5e1-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e5e1-111">Sqldatabaseusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="6e5e1-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e5e1-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6e5e1-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e5e1-113">Sqlshardmapusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="6e5e1-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e5e1-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e5e1-114">DESCRIPTION</span></span>
<span data-ttu-id="6e5e1-115">Remove-AzSqlElasticJobTarget cmdlet 'i hedef bir kaynağı hedef gruba çıkarır</span><span class="sxs-lookup"><span data-stu-id="6e5e1-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="6e5e1-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e5e1-116">EXAMPLES</span></span>

### <span data-ttu-id="6e5e1-117">Örnek 1: sunucu hedefini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e5e1-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="6e5e1-118">Örnek 2: veritabanı hedefini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e5e1-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="6e5e1-119">Örnek 3: elastik havuz hedefini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e5e1-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="6e5e1-120">Örnek 4: Shard harita hedefini kaldırma</span><span class="sxs-lookup"><span data-stu-id="6e5e1-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="6e5e1-121">Hedef gruptan hedef (sunucu, esnek havuz, veritabanı ve Shard Haritası) kaldırır</span><span class="sxs-lookup"><span data-stu-id="6e5e1-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="6e5e1-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e5e1-122">PARAMETERS</span></span>

### <span data-ttu-id="6e5e1-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-123">-AgentName</span></span>
<span data-ttu-id="6e5e1-124">SQL veritabanı Aracısı adı.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="6e5e1-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-125">-AgentServerName</span></span>
<span data-ttu-id="6e5e1-126">SQL veritabanı Aracısı sunucusu adı.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="6e5e1-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-127">-DatabaseName</span></span>
<span data-ttu-id="6e5e1-128">Veritabanı hedef adı</span><span class="sxs-lookup"><span data-stu-id="6e5e1-128">Database Target Name</span></span>

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

### <span data-ttu-id="6e5e1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5e1-129">-DefaultProfile</span></span>
<span data-ttu-id="6e5e1-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e5e1-131">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-131">-ElasticPoolName</span></span>
<span data-ttu-id="6e5e1-132">Elastik havuz hedef adı</span><span class="sxs-lookup"><span data-stu-id="6e5e1-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="6e5e1-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6e5e1-133">-ParentObject</span></span>
<span data-ttu-id="6e5e1-134">Hedef Grup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-134">The target group object.</span></span>

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

### <span data-ttu-id="6e5e1-135">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="6e5e1-135">-ParentResourceId</span></span>
<span data-ttu-id="6e5e1-136">Hedef Grup kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-136">The target group resource id.</span></span>

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

### <span data-ttu-id="6e5e1-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-137">-RefreshCredentialName</span></span>
<span data-ttu-id="6e5e1-138">Kimlik bilgileri yenileme</span><span class="sxs-lookup"><span data-stu-id="6e5e1-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="6e5e1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-139">-ResourceGroupName</span></span>
<span data-ttu-id="6e5e1-140">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6e5e1-140">Resource Group Name</span></span>

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

### <span data-ttu-id="6e5e1-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-141">-ServerName</span></span>
<span data-ttu-id="6e5e1-142">Sunucu hedef adı</span><span class="sxs-lookup"><span data-stu-id="6e5e1-142">Server Target Name</span></span>

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

### <span data-ttu-id="6e5e1-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-143">-ShardMapName</span></span>
<span data-ttu-id="6e5e1-144">Shard harita hedef adı</span><span class="sxs-lookup"><span data-stu-id="6e5e1-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="6e5e1-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="6e5e1-145">-TargetGroupName</span></span>
<span data-ttu-id="6e5e1-146">SQL veritabanı Aracısı adı.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="6e5e1-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="6e5e1-147">-Confirm</span></span>
<span data-ttu-id="6e5e1-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e5e1-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e5e1-149">-WhatIf</span></span>
<span data-ttu-id="6e5e1-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e5e1-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e5e1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e5e1-152">CommonParameters</span></span>
<span data-ttu-id="6e5e1-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e5e1-154">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e5e1-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e5e1-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e5e1-155">INPUTS</span></span>

### <span data-ttu-id="6e5e1-156">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobtargetgroupmodel</span><span class="sxs-lookup"><span data-stu-id="6e5e1-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="6e5e1-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e5e1-157">OUTPUTS</span></span>

### <span data-ttu-id="6e5e1-158">Microsoft. Azure. Management. Sql. modeller. JobTarget</span><span class="sxs-lookup"><span data-stu-id="6e5e1-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="6e5e1-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e5e1-159">NOTES</span></span>

## <span data-ttu-id="6e5e1-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e5e1-160">RELATED LINKS</span></span>
