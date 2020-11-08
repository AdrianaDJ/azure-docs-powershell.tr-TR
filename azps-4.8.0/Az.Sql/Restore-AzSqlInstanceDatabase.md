---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: 4d8ece03cc5c1a96d73bcde79aef76c8f329b38a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108628"
---
# <span data-ttu-id="986ef-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="986ef-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="986ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986ef-102">SYNOPSIS</span></span>
<span data-ttu-id="986ef-103">Azure SQL yönetilen örneği veritabanını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="986ef-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="986ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="986ef-104">SYNTAX</span></span>

### <span data-ttu-id="986ef-105">Pointintimesameınstancerestoreınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="986ef-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="986ef-106">Pointintimesameınstancerestoreınstancedatabasefrolaurestomanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="986ef-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="986ef-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="986ef-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="986ef-108">Pointintimecrossınstancerestoreınstancedatabasefrominınputparameters</span><span class="sxs-lookup"><span data-stu-id="986ef-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="986ef-109">Pointintimecrossınstancerestoreınstancedatabasefrolaurestomanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="986ef-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="986ef-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="986ef-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="986ef-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span><span class="sxs-lookup"><span data-stu-id="986ef-111">PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="986ef-112">Pointintimedeleteddatabasescrossınstancerestoreınstancedatabasefrominınputparameters</span><span class="sxs-lookup"><span data-stu-id="986ef-112">PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-SubscriptionId <String>] [-ResourceGroupName] <String>
 [-InstanceName] <String> [-Name] <String> [-DeletionDate] <DateTime> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="986ef-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="986ef-113">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="986ef-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="986ef-114">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="986ef-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="986ef-115">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-Name] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="986ef-116">LongTermRetentionBackupRestoreParameter</span><span class="sxs-lookup"><span data-stu-id="986ef-116">LongTermRetentionBackupRestoreParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromLongTermRetentionBackup] [-SubscriptionId <String>] [-ResourceId] <String>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="986ef-117">Tanım</span><span class="sxs-lookup"><span data-stu-id="986ef-117">DESCRIPTION</span></span>
<span data-ttu-id="986ef-118">**Restore-Azsqlınstancedatabase** cmdlet 'i bir örnek veritabanını coğrafi olarak yedekli bir yedekten, canlı bir veritabanındaki bir noktadan veya uzun süreli bir bekletme yedeğinden geri yükler.</span><span class="sxs-lookup"><span data-stu-id="986ef-118">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup, a point in time in a live database, or a long term retention backup.</span></span>
<span data-ttu-id="986ef-119">Geri yüklenen veritabanı yeni bir örnek veritabanı olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="986ef-119">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="986ef-120">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="986ef-120">EXAMPLES</span></span>

### <span data-ttu-id="986ef-121">Örnek 1: örnek veritabanını zaman noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="986ef-121">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="986ef-122">Bu komut, Database01 adlı örnek veritabanı, belirtilen zaman içinde, Database01_restored adlı örnek veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="986ef-122">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="986ef-123">Örnek 2: bir örnek veritabanını farklı bir kaynak grubundaki başka bir örneğe geri yükleme</span><span class="sxs-lookup"><span data-stu-id="986ef-123">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="986ef-124">Bu komut, kaynak grubu ResourceGroup02 managedInstance1 örneğindeki örneğindeki Database01_restored örnek veritabanına ResourceGroup01 kaynak grubu örnek veritabanı Database01 'i geri yükler.</span><span class="sxs-lookup"><span data-stu-id="986ef-124">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="986ef-125">Örnek 3: örnek veritabanını Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="986ef-125">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="986ef-126">İlk komut, Database01 adlı veritabanının coğrafi yedekli yedeklemesini alır ve $GeoBackup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="986ef-126">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="986ef-127">İkinci komut $GeoBackup yedeği Database01_restored adlı örnek veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="986ef-127">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="986ef-128">Örnek 4: silinmiş bir örnek veritabanını zaman noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="986ef-128">Example 4: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -Name $deletedDatabase.Name -InstanceName $deletedDatabase.ManagedInstanceName -ResourceGroupName $deletedDatabase.ResourceGroupName -DeletionDate $deletedDatabase.DeletionDate -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="986ef-129">İlk komut, ' managedInstance1 ' örneğindeki ' DB1 ' adındaki silinmiş örnek veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="986ef-129">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="986ef-130">İkinci komut, getirilen veritabanını belirtilen zaman noktasından, Database01_restored adlı örnek veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="986ef-130">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="986ef-131">Örnek 5: silinmiş bir örnek veritabanını zaman noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="986ef-131">Example 5: Restore a deleted instance database from a point in time</span></span>
```
PS C:\> $deletedDatabase = Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -DatabaseName "DB1"
PS C:\> Restore-AzSqlinstanceDatabase -InputObject $deletedDatabase[0] -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="986ef-132">İlk komut, ' managedInstance1 ' örneğindeki ' DB1 ' adındaki silinmiş örnek veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="986ef-132">The first command gets the deleted instance databases named 'DB1' on Instance 'managedInstance1'.</span></span>
<span data-ttu-id="986ef-133">İkinci komut, getirilen veritabanını, giriş nesnesini kullanarak belirtilen zaman içinde, belirtilen nokta yedeklemesinden örnek Database01_restored veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="986ef-133">The second command restores the the fetched database, from the specified point-in-time backup to the instance database named Database01_restored using input object.</span></span>

### <span data-ttu-id="986ef-134">Örnek 6: bir veritabanını LTR yedekten geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="986ef-134">Example 6: Restore a database from LTR backup.</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -FromLongTermRetentionBackup -ResourceId /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManagedInstances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000 -TargetInstanceDatabaseName restoreTarget -TargetInstanceName testInstance -TargetResourceGroupName testResourceGroup


Location                          : southeastasia
Tags                              :
Collation                         : SQL_Latin1_General_CP1_CI_AS
Status                            : Online
RestorePointInTime                :
DefaultSecondaryLocation          : northeurope
CatalogCollation                  :
CreateMode                        :
StorageContainerUri               :
StorageContainerSasToken          :
SourceDatabaseId                  :
FailoverGroupId                   :
RecoverableDatabaseId             :
RestorableDroppedDatabaseId       :
LongTermRetentionBackupResourceId :
ResourceGroupName                 : testResourceGroup
ManagedInstanceName               : testInstance
Name                              : restoreTarget
CreationDate                      : 3/4/2020 8:12:56 AM
EarliestRestorePoint              : 3/4/2020 8:14:29 AM
Id                                : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/managedInstances/testInstance/databases/restoreTarget
```

<span data-ttu-id="986ef-135">Verilen kaynak KIMLIĞIYLE (Get-AzSqlInstanceDatabaseLongTermRetentionBackup ' i çalıştırarak bulunabilir) LTR yedeklemesini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="986ef-135">Restores LTR backup with the given resource ID (which can be found by running Get-AzSqlInstanceDatabaseLongTermRetentionBackup).</span></span>

## <span data-ttu-id="986ef-136">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="986ef-136">PARAMETERS</span></span>

### <span data-ttu-id="986ef-137">-Iş</span><span class="sxs-lookup"><span data-stu-id="986ef-137">-AsJob</span></span>
<span data-ttu-id="986ef-138">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="986ef-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="986ef-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986ef-139">-DefaultProfile</span></span>
<span data-ttu-id="986ef-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="986ef-140">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="986ef-141">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="986ef-141">-DeletionDate</span></span>
<span data-ttu-id="986ef-142">Silinen veritabanının silme tarihi.</span><span class="sxs-lookup"><span data-stu-id="986ef-142">The deletion date of deleted database.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-143">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="986ef-143">-FromGeoBackup</span></span>
<span data-ttu-id="986ef-144">Coğrafi bir yedekten geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="986ef-144">Restore from a geo backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-145">-FromLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="986ef-145">-FromLongTermRetentionBackup</span></span>
<span data-ttu-id="986ef-146">Uzun süreli bekletme yedeklemesinden geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="986ef-146">Restore from a Long Term Retention backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-147">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="986ef-147">-FromPointInTimeBackup</span></span>
<span data-ttu-id="986ef-148">Bir noktadan noktaya geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="986ef-148">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-149">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="986ef-149">-GeoBackupObject</span></span>
<span data-ttu-id="986ef-150">Geri yüklenecek kurtarılabilir örnek veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="986ef-150">The recoverable instance database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter
Aliases: RecoverableInstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-151">-InputObject</span><span class="sxs-lookup"><span data-stu-id="986ef-151">-InputObject</span></span>
<span data-ttu-id="986ef-152">Geri yüklenecek örnek veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="986ef-152">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-153">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="986ef-153">-InstanceName</span></span>
<span data-ttu-id="986ef-154">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="986ef-154">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-155">-Ad</span><span class="sxs-lookup"><span data-stu-id="986ef-155">-Name</span></span>
<span data-ttu-id="986ef-156">Geri yüklenecek örnek veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="986ef-156">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName, SourceInstanceDatabaseName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-157">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="986ef-157">-PointInTime</span></span>
<span data-ttu-id="986ef-158">Veritabanını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="986ef-158">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="986ef-159">-ResourceGroupName</span></span>
<span data-ttu-id="986ef-160">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="986ef-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: SourceResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-161">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="986ef-161">-ResourceId</span></span>
<span data-ttu-id="986ef-162">Geri yüklenecek örnek veritabanı nesnesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="986ef-162">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GeoRestoreFromGeoBackupSetNameFromResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-163">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="986ef-163">-SubscriptionId</span></span>
<span data-ttu-id="986ef-164">Kaynak abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="986ef-164">Source subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, LongTermRetentionBackupRestoreParameter
Aliases: SourceSubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-165">-Targetınstancedatabasename</span><span class="sxs-lookup"><span data-stu-id="986ef-165">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="986ef-166">Geri yüklenecek hedef örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="986ef-166">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="986ef-167">-Targetınstancename</span><span class="sxs-lookup"><span data-stu-id="986ef-167">-TargetInstanceName</span></span>
<span data-ttu-id="986ef-168">Geri yüklenecek hedef örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="986ef-168">The name of the target instance to restore to.</span></span>
<span data-ttu-id="986ef-169">Belirtilmemişse, hedef örnek kaynak örnekle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="986ef-169">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-170">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="986ef-170">-TargetResourceGroupName</span></span>
<span data-ttu-id="986ef-171">Geri yüklenecek hedef kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="986ef-171">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="986ef-172">Belirtilmemişse, hedef kaynak grubu kaynak kaynak grubuyla aynıdır.</span><span class="sxs-lookup"><span data-stu-id="986ef-172">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeDeletedDatabasesCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter, LongTermRetentionBackupRestoreParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="986ef-173">-Onay</span><span class="sxs-lookup"><span data-stu-id="986ef-173">-Confirm</span></span>
<span data-ttu-id="986ef-174">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="986ef-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="986ef-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="986ef-175">-WhatIf</span></span>
<span data-ttu-id="986ef-176">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="986ef-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="986ef-177">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="986ef-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="986ef-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986ef-178">CommonParameters</span></span>
<span data-ttu-id="986ef-179">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="986ef-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986ef-180">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="986ef-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986ef-181">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="986ef-181">INPUTS</span></span>

### <span data-ttu-id="986ef-182">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="986ef-182">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="986ef-183">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlrecoverablemanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="986ef-183">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="986ef-184">System. String</span><span class="sxs-lookup"><span data-stu-id="986ef-184">System.String</span></span>

## <span data-ttu-id="986ef-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="986ef-185">OUTPUTS</span></span>

### <span data-ttu-id="986ef-186">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="986ef-186">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="986ef-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="986ef-187">NOTES</span></span>

## <span data-ttu-id="986ef-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="986ef-188">RELATED LINKS</span></span>
