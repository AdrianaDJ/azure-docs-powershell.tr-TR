---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/restore-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Restore-AzSqlInstanceDatabase.md
ms.openlocfilehash: d513c186f621329510582c9cd69a64461f9e068f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758812"
---
# <span data-ttu-id="44054-101">Restore-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="44054-101">Restore-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="44054-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44054-102">SYNOPSIS</span></span>
<span data-ttu-id="44054-103">Azure SQL yönetilen örneği veritabanını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="44054-103">Restores an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="44054-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="44054-104">SYNTAX</span></span>

### <span data-ttu-id="44054-105">Pointintimesameınstancerestoreınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="44054-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44054-106">Pointintimesameınstancerestoreınstancedatabasefrolaurestomanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="44054-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44054-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="44054-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44054-108">Pointintimecrossınstancerestoreınstancedatabasefrominınputparameters</span><span class="sxs-lookup"><span data-stu-id="44054-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44054-109">Pointintimecrossınstancerestoreınstancedatabasefrolaurestomanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="44054-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44054-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="44054-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44054-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span><span class="sxs-lookup"><span data-stu-id="44054-111">GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-GeoBackupObject] <AzureSqlRecoverableManagedDatabaseModel>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44054-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="44054-112">GeoRestoreFromGeoBackupSetNameFromResourceIdParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-ResourceId] <String> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44054-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="44054-113">GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter</span></span>
```
Restore-AzSqlInstanceDatabase [-FromGeoBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44054-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="44054-114">DESCRIPTION</span></span>
<span data-ttu-id="44054-115">**Restore-Azsqlınstancedatabase** cmdlet 'i bir örnek veritabanını coğrafi olarak yedekli bir yedekten veya Live veritabanından gelen bir noktadan geri yükler.</span><span class="sxs-lookup"><span data-stu-id="44054-115">The **Restore-AzSqlInstanceDatabase** cmdlet restores an instance database from a geo-redundant backup or a point in time in a live database.</span></span>
<span data-ttu-id="44054-116">Geri yüklenen veritabanı yeni bir örnek veritabanı olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="44054-116">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="44054-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="44054-117">EXAMPLES</span></span>

### <span data-ttu-id="44054-118">Örnek 1: örnek veritabanını zaman noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="44054-118">Example 1: Restore an instance database from a point in time</span></span>
```
PS C:\> Restore-AzSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="44054-119">Bu komut, Database01 adlı örnek veritabanı, belirtilen zaman içinde, Database01_restored adlı örnek veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="44054-119">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="44054-120">Örnek 2: bir örnek veritabanını farklı bir kaynak grubundaki başka bir örneğe geri yükleme</span><span class="sxs-lookup"><span data-stu-id="44054-120">Example 2: Restore an instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="44054-121">Bu komut, kaynak grubu ResourceGroup02 managedInstance1 örneğindeki örneğindeki Database01_restored örnek veritabanına ResourceGroup01 kaynak grubu örnek veritabanı Database01 'i geri yükler.</span><span class="sxs-lookup"><span data-stu-id="44054-121">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

### <span data-ttu-id="44054-122">Örnek 3: örnek veritabanını Geo-Restore</span><span class="sxs-lookup"><span data-stu-id="44054-122">Example 3: Geo-Restore an instance database</span></span>
```
PS C:\>$GeoBackup = Get-AzSqlInstanceDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -InstanceName "managedInstance1" -Name "Database01"
PS C:\> $GeoBackup | Restore-AzSqlInstanceDatabase -FromGeoBackup -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance2" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="44054-123">İlk komut, Database01 adlı veritabanının coğrafi yedekli yedeklemesini alır ve $GeoBackup değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="44054-123">The first command gets the geo-redundant backup for the database named Database01, and then stores it in the $GeoBackup variable.</span></span>
<span data-ttu-id="44054-124">İkinci komut $GeoBackup yedeği Database01_restored adlı örnek veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="44054-124">The second command restores the backup in $GeoBackup to the instance database named Database01_restored.</span></span>

## <span data-ttu-id="44054-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="44054-125">PARAMETERS</span></span>

### <span data-ttu-id="44054-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="44054-126">-AsJob</span></span>
<span data-ttu-id="44054-127">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="44054-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44054-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44054-128">-DefaultProfile</span></span>
<span data-ttu-id="44054-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="44054-129">The credentials, account, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="44054-130">-FromGeoBackup</span><span class="sxs-lookup"><span data-stu-id="44054-130">-FromGeoBackup</span></span>
<span data-ttu-id="44054-131">Coğrafi bir yedekten geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="44054-131">Restore from a geo backup.</span></span>

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

### <span data-ttu-id="44054-132">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="44054-132">-FromPointInTimeBackup</span></span>
<span data-ttu-id="44054-133">Bir noktadan noktaya geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="44054-133">Restore from a point-in-time backup.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44054-134">-GeoBackupObject</span><span class="sxs-lookup"><span data-stu-id="44054-134">-GeoBackupObject</span></span>
<span data-ttu-id="44054-135">Geri yüklenecek kurtarılabilir örnek veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="44054-135">The recoverable instance database object to restore</span></span>

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

### <span data-ttu-id="44054-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44054-136">-InputObject</span></span>
<span data-ttu-id="44054-137">Geri yüklenecek örnek veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="44054-137">The Instance Database object to restore</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44054-138">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="44054-138">-InstanceName</span></span>
<span data-ttu-id="44054-139">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="44054-139">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44054-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="44054-140">-Name</span></span>
<span data-ttu-id="44054-141">Geri yüklenecek örnek veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="44054-141">The instance database name to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44054-142">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="44054-142">-PointInTime</span></span>
<span data-ttu-id="44054-143">Veritabanını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="44054-143">The point in time to restore the database to.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44054-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44054-144">-ResourceGroupName</span></span>
<span data-ttu-id="44054-145">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="44054-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44054-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="44054-146">-ResourceId</span></span>
<span data-ttu-id="44054-147">Geri yüklenecek örnek veritabanı nesnesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="44054-147">The resource id of Instance Database object to restore</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
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

### <span data-ttu-id="44054-148">-Targetınstancedatabasename</span><span class="sxs-lookup"><span data-stu-id="44054-148">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="44054-149">Geri yüklenecek hedef örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="44054-149">The name of the target instance database to restore to.</span></span>

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

### <span data-ttu-id="44054-150">-Targetınstancename</span><span class="sxs-lookup"><span data-stu-id="44054-150">-TargetInstanceName</span></span>
<span data-ttu-id="44054-151">Geri yüklenecek hedef örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="44054-151">The name of the target instance to restore to.</span></span>
<span data-ttu-id="44054-152">Belirtilmemişse, hedef örnek kaynak örnekle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="44054-152">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44054-153">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44054-153">-TargetResourceGroupName</span></span>
<span data-ttu-id="44054-154">Geri yüklenecek hedef kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="44054-154">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="44054-155">Belirtilmemişse, hedef kaynak grubu kaynak kaynak grubuyla aynıdır.</span><span class="sxs-lookup"><span data-stu-id="44054-155">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId, GeoRestoreFromGeoBackupSetNameFromGeoBackupObjectParameter, GeoRestoreFromGeoBackupSetNameFromResourceIdParameter, GeoRestoreFromGeoBackupSetNameFromNameAndResourceGroupParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44054-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="44054-156">-Confirm</span></span>
<span data-ttu-id="44054-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="44054-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44054-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44054-158">-WhatIf</span></span>
<span data-ttu-id="44054-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="44054-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44054-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="44054-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44054-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44054-161">CommonParameters</span></span>
<span data-ttu-id="44054-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="44054-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44054-163">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="44054-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44054-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="44054-164">INPUTS</span></span>

### <span data-ttu-id="44054-165">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="44054-165">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="44054-166">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlrecoverablemanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="44054-166">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlRecoverableManagedDatabaseModel</span></span>

### <span data-ttu-id="44054-167">System. String</span><span class="sxs-lookup"><span data-stu-id="44054-167">System.String</span></span>

## <span data-ttu-id="44054-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="44054-168">OUTPUTS</span></span>

### <span data-ttu-id="44054-169">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="44054-169">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="44054-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="44054-170">NOTES</span></span>

## <span data-ttu-id="44054-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="44054-171">RELATED LINKS</span></span>
