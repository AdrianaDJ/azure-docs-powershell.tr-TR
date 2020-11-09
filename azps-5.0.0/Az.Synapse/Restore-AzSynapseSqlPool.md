---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 2dae942470dba8a36258ffb8c813e08c664f2e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323533"
---
# <span data-ttu-id="96e20-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="96e20-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="96e20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96e20-102">SYNOPSIS</span></span>
<span data-ttu-id="96e20-103">SYNAPSE Analytics SQL havuzunu geri yükler.</span><span class="sxs-lookup"><span data-stu-id="96e20-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="96e20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96e20-104">SYNTAX</span></span>

### <span data-ttu-id="96e20-105">Restorefrombackupıdbynameparameterset</span><span class="sxs-lookup"><span data-stu-id="96e20-105">RestoreFromBackupIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96e20-106">Restorefrombackupıdbyparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="96e20-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96e20-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e20-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96e20-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e20-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96e20-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e20-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96e20-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e20-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96e20-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e20-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96e20-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e20-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96e20-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e20-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96e20-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="96e20-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96e20-115">Tanım</span><span class="sxs-lookup"><span data-stu-id="96e20-115">DESCRIPTION</span></span>
<span data-ttu-id="96e20-116">**Restore-AzSynapseSqlPool** cmdlet 'i bir yedekten veya HERHANGI bir SQL havuzunun geri yükleme noktasından bir Azure SYNAPSE Analytics SQL havuzunu geri yükler.</span><span class="sxs-lookup"><span data-stu-id="96e20-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="96e20-117">Geri yüklenen SQL havuzu yeni bir SQL havuzu olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="96e20-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="96e20-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96e20-118">EXAMPLES</span></span>

### <span data-ttu-id="96e20-119">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="96e20-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="96e20-120">Bu komut, Bu abonelikteki herhangi bir SQL havuzunun en son yedeklemesinden geri yükleyerek bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96e20-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="96e20-121">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="96e20-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="96e20-122">Bu komut, Bu abonelikteki herhangi bir SQL havuzundan geri yükleme noktası göndererek önceki bir durumdan kurtarmak veya kopyalamak için bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96e20-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="96e20-123">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="96e20-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="96e20-124">Bu komut, Bu abonelikteki herhangi bir SQL havuzunun en son yedeklemesinden kaynak KIMLIĞIYLE geri yükleyerek bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96e20-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="96e20-125">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="96e20-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="96e20-126">Bu komut, Bu abonelikteki herhangi bir SQL havuzundan geri yükleme noktası kullanarak, kaynak KIMLIĞIYLE önceki bir durumdan kurtarmak veya kopyalamak için bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="96e20-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="96e20-127">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96e20-127">PARAMETERS</span></span>

### <span data-ttu-id="96e20-128">-Iş</span><span class="sxs-lookup"><span data-stu-id="96e20-128">-AsJob</span></span>
<span data-ttu-id="96e20-129">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="96e20-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96e20-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e20-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="96e20-131">Oluşturulacak fırfinsql havuz nesnesinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-132">-Backupresourceıd</span><span class="sxs-lookup"><span data-stu-id="96e20-132">-BackupResourceId</span></span>
<span data-ttu-id="96e20-133">Geri yüklenecek yedekleme SQL havuz nesnesinin kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="96e20-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="96e20-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="96e20-135">Oluşturulacak ilk SQL havuz nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="96e20-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="96e20-137">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="96e20-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-138">-Yedeklemeçalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="96e20-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="96e20-139">Oluşturulacak ilk SQL havuz nesnesinin SYNAPSE çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e20-140">-DefaultProfile</span></span>
<span data-ttu-id="96e20-141">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96e20-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96e20-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="96e20-142">-FromBackup</span></span>
<span data-ttu-id="96e20-143">Bu abonelikteki herhangi bir SQL havuzunun en son yedeklemesinden geri yüklemeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="96e20-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="96e20-144">-FromRestorePoint</span></span>
<span data-ttu-id="96e20-145">Bu abonelikteki herhangi bir SQL havuzundan, önceki bir durumdan kurtarmak veya kopyalamak için bir geri yükleme noktasının kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96e20-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-146">-Ad</span><span class="sxs-lookup"><span data-stu-id="96e20-146">-Name</span></span>
<span data-ttu-id="96e20-147">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-147">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="96e20-148">-PerformanceLevel</span></span>
<span data-ttu-id="96e20-149">SQL havuzuna atanacak SQL hizmet katmanı ve performans düzeyi.</span><span class="sxs-lookup"><span data-stu-id="96e20-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="96e20-150">Örneğin, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="96e20-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e20-151">-ResourceGroupName</span></span>
<span data-ttu-id="96e20-152">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="96e20-153">-RestorePoint</span></span>
<span data-ttu-id="96e20-154">Geri yüklenecek anlık görüntü süresi.</span><span class="sxs-lookup"><span data-stu-id="96e20-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e20-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="96e20-156">Oluşturulacak kaynak SQL havuzu nesnesinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-157">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="96e20-157">-SourceResourceId</span></span>
<span data-ttu-id="96e20-158">Oluşturulacak kaynak SQL havuzu nesnesinin kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="96e20-158">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-159">-Sourcessqlpoolname</span><span class="sxs-lookup"><span data-stu-id="96e20-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="96e20-160">Oluşturulacak kaynak SQL havuzu nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-161">-Sourcessqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="96e20-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="96e20-162">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="96e20-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-163">-Sourceçalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="96e20-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="96e20-164">Oluşturulacak kaynak SQL havuzu nesnesinin SYNAPSE çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-165">Etiketli</span><span class="sxs-lookup"><span data-stu-id="96e20-165">-Tag</span></span>
<span data-ttu-id="96e20-166">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="96e20-166">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-167">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="96e20-167">-WorkspaceName</span></span>
<span data-ttu-id="96e20-168">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="96e20-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-169">-</span><span class="sxs-lookup"><span data-stu-id="96e20-169">-WorkspaceObject</span></span>
<span data-ttu-id="96e20-170">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="96e20-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96e20-171">-Onay</span><span class="sxs-lookup"><span data-stu-id="96e20-171">-Confirm</span></span>
<span data-ttu-id="96e20-172">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96e20-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e20-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e20-173">-WhatIf</span></span>
<span data-ttu-id="96e20-174">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96e20-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96e20-175">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96e20-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e20-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e20-176">CommonParameters</span></span>
<span data-ttu-id="96e20-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96e20-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e20-178">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="96e20-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e20-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96e20-179">INPUTS</span></span>

### <span data-ttu-id="96e20-180">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="96e20-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="96e20-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96e20-181">OUTPUTS</span></span>

### <span data-ttu-id="96e20-182">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="96e20-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="96e20-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96e20-183">NOTES</span></span>

## <span data-ttu-id="96e20-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96e20-184">RELATED LINKS</span></span>
