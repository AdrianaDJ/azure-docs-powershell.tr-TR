---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274674"
---
# <span data-ttu-id="e5088-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e5088-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="e5088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5088-102">SYNOPSIS</span></span>
<span data-ttu-id="e5088-103">SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5088-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e5088-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5088-104">SYNTAX</span></span>

### <span data-ttu-id="e5088-105">CreateByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e5088-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5088-106">Createfrombackupıdbynameparameterset</span><span class="sxs-lookup"><span data-stu-id="e5088-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5088-107">Createfrombackupıdbyparentobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="e5088-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5088-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5088-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5088-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5088-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5088-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5088-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5088-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e5088-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5088-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5088-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5088-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5088-117">DESCRIPTION</span></span>
<span data-ttu-id="e5088-118">**New-AzSynapseSqlPool** cmdlet 'ı bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5088-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="e5088-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5088-119">EXAMPLES</span></span>

### <span data-ttu-id="e5088-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e5088-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="e5088-121">Bu komut, bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5088-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="e5088-122">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e5088-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="e5088-123">Bu komut, Bu abonelikteki herhangi bir SQL havuzunun en son yedeklemesinden geri yükleyerek bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5088-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="e5088-124">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e5088-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="e5088-125">Bu komut, Bu abonelikteki herhangi bir SQL havuzundan geri yükleme noktası göndererek önceki bir durumdan kurtarmak veya kopyalamak için bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5088-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="e5088-126">Örnek 4</span><span class="sxs-lookup"><span data-stu-id="e5088-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="e5088-127">Bu komut, Bu abonelikteki herhangi bir SQL havuzunun en son yedeklemesinden kaynak KIMLIĞIYLE geri yükleyerek bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5088-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="e5088-128">Örnek 5</span><span class="sxs-lookup"><span data-stu-id="e5088-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="e5088-129">Bu komut, Bu abonelikteki herhangi bir SQL havuzundan geri yükleme noktası kullanarak, kaynak KIMLIĞIYLE önceki bir durumdan kurtarmak veya kopyalamak için bir Azure SYNAPSE Analytics SQL havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5088-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="e5088-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5088-130">PARAMETERS</span></span>

### <span data-ttu-id="e5088-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="e5088-131">-AsJob</span></span>
<span data-ttu-id="e5088-132">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e5088-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5088-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5088-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="e5088-134">Oluşturulacak fırfinsql havuz nesnesinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-135">-Backupresourceıd</span><span class="sxs-lookup"><span data-stu-id="e5088-135">-BackupResourceId</span></span>
<span data-ttu-id="e5088-136">Geri yüklenecek yedekleme SQL havuz nesnesinin kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e5088-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e5088-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="e5088-138">Oluşturulacak ilk SQL havuz nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e5088-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="e5088-140">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e5088-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-141">-Yedeklemeçalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e5088-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="e5088-142">Oluşturulacak ilk SQL havuz nesnesinin SYNAPSE çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-143">-Harmanlama</span><span class="sxs-lookup"><span data-stu-id="e5088-143">-Collation</span></span>
<span data-ttu-id="e5088-144">Harmanlama, verileri sıralayan ve karşılaştıran kuralları tanımlar ve SQL havuzu oluşturulduktan sonra değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="e5088-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="e5088-145">Varsayılan alfabe düzeni SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="e5088-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5088-146">-DefaultProfile</span></span>
<span data-ttu-id="e5088-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e5088-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5088-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="e5088-148">-FromBackup</span></span>
<span data-ttu-id="e5088-149">Bu abonelikteki herhangi bir SQL havuzunun en son yedeklemesinden geri yüklemeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5088-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e5088-150">-FromRestorePoint</span></span>
<span data-ttu-id="e5088-151">Bu abonelikteki herhangi bir SQL havuzundan, önceki bir durumdan kurtarmak veya kopyalamak için bir geri yükleme noktasının kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5088-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-152">-Ad</span><span class="sxs-lookup"><span data-stu-id="e5088-152">-Name</span></span>
<span data-ttu-id="e5088-153">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="e5088-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="e5088-154">-PerformanceLevel</span></span>
<span data-ttu-id="e5088-155">SQL havuzuna atanacak SQL hizmet katmanı ve performans düzeyi.</span><span class="sxs-lookup"><span data-stu-id="e5088-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="e5088-156">Örneğin, DW2000c.</span><span class="sxs-lookup"><span data-stu-id="e5088-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5088-157">-ResourceGroupName</span></span>
<span data-ttu-id="e5088-158">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="e5088-159">-RestorePoint</span></span>
<span data-ttu-id="e5088-160">Geri yüklenecek anlık görüntü süresi.</span><span class="sxs-lookup"><span data-stu-id="e5088-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5088-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="e5088-162">Oluşturulacak kaynak SQL havuzu nesnesinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-163">-Sourceresourceıd</span><span class="sxs-lookup"><span data-stu-id="e5088-163">-SourceResourceId</span></span>
<span data-ttu-id="e5088-164">Oluşturulacak kaynak SQL havuzu nesnesinin kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e5088-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-165">-Sourcessqlpoolname</span><span class="sxs-lookup"><span data-stu-id="e5088-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="e5088-166">Oluşturulacak kaynak SQL havuzu nesnesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-167">-Sourcessqlpoolobject</span><span class="sxs-lookup"><span data-stu-id="e5088-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="e5088-168">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e5088-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-169">-Sourceçalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e5088-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="e5088-170">Oluşturulacak kaynak SQL havuzu nesnesinin SYNAPSE çalışma alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-171">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e5088-171">-Tag</span></span>
<span data-ttu-id="e5088-172">Kaynakla ilişkili etiketlerin dize sözlüğü.</span><span class="sxs-lookup"><span data-stu-id="e5088-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="e5088-173">-Version</span><span class="sxs-lookup"><span data-stu-id="e5088-173">-Version</span></span>
<span data-ttu-id="e5088-174">SYNAPSE SQL havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="e5088-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="e5088-175">Örneğin, 2 veya 3.</span><span class="sxs-lookup"><span data-stu-id="e5088-175">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-176">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="e5088-176">-WorkspaceName</span></span>
<span data-ttu-id="e5088-177">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="e5088-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-178">-</span><span class="sxs-lookup"><span data-stu-id="e5088-178">-WorkspaceObject</span></span>
<span data-ttu-id="e5088-179">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="e5088-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5088-180">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5088-180">-Confirm</span></span>
<span data-ttu-id="e5088-181">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5088-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5088-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5088-182">-WhatIf</span></span>
<span data-ttu-id="e5088-183">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5088-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5088-184">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5088-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5088-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5088-185">CommonParameters</span></span>
<span data-ttu-id="e5088-186">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5088-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5088-187">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e5088-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5088-188">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5088-188">INPUTS</span></span>

### <span data-ttu-id="e5088-189">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e5088-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e5088-190">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5088-190">OUTPUTS</span></span>

### <span data-ttu-id="e5088-191">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e5088-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e5088-192">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5088-192">NOTES</span></span>

## <span data-ttu-id="e5088-193">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5088-193">RELATED LINKS</span></span>
