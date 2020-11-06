---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/restore-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: 61fe76eba8d1f8faf0ab45d0a24f56a8dabf3641
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594332"
---
# <span data-ttu-id="bbe40-101">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="bbe40-101">Restore-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="bbe40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbe40-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe40-103">Azure SQL yönetilen örneği veritabanını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="bbe40-103">Restores an Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbe40-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bbe40-104">SYNTAX</span></span>

### <span data-ttu-id="bbe40-105">Pointintimesameınstancerestoreınstancedatabasefrominınputparameters (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bbe40-105">PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters (Default)</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbe40-106">Pointintimesameınstancerestoreınstancedatabasefrolaurestomanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="bbe40-106">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbe40-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="bbe40-107">PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbe40-108">Pointintimecrossınstancerestoreınstancedatabasefrominınputparameters</span><span class="sxs-lookup"><span data-stu-id="bbe40-108">PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-Name] <String> [-InstanceName] <String>
 [-ResourceGroupName] <String> -PointInTime <DateTime> -TargetInstanceDatabaseName <String>
 -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbe40-109">Pointintimecrossınstancerestoreınstancedatabasefrolaurestomanageddatabasemodelınstancedefinition</span><span class="sxs-lookup"><span data-stu-id="bbe40-109">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-InputObject] <AzureSqlManagedDatabaseModel>
 -PointInTime <DateTime> -TargetInstanceDatabaseName <String> -TargetInstanceName <String>
 -TargetResourceGroupName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbe40-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="bbe40-110">PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId</span></span>
```
Restore-AzureRmSqlInstanceDatabase [-FromPointInTimeBackup] [-ResourceId] <String> -PointInTime <DateTime>
 -TargetInstanceDatabaseName <String> -TargetInstanceName <String> -TargetResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbe40-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="bbe40-111">DESCRIPTION</span></span>
<span data-ttu-id="bbe40-112">**Restore-Azurermsqlınstancedatabase** cmdlet 'i, bir örnek veritabanını Live veritabanında bir noktadan geri yükler.</span><span class="sxs-lookup"><span data-stu-id="bbe40-112">The **Restore-AzureRmSqlInstanceDatabase** cmdlet restores an instance database from a point in time in a live database.</span></span>
<span data-ttu-id="bbe40-113">Geri yüklenen veritabanı yeni bir örnek veritabanı olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="bbe40-113">The restored database is created as a new instance database.</span></span>

## <span data-ttu-id="bbe40-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bbe40-114">EXAMPLES</span></span>

### <span data-ttu-id="bbe40-115">Örnek 1: örnek veritabanını zaman noktasından geri yükleme</span><span class="sxs-lookup"><span data-stu-id="bbe40-115">Example 1: Restore a instance database from a point in time</span></span>
```
PS C:\> Restore-AzureRmSqlinstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored"
```

<span data-ttu-id="bbe40-116">Bu komut, Database01 adlı örnek veritabanı, belirtilen zaman içinde, Database01_restored adlı örnek veritabanına geri yükler.</span><span class="sxs-lookup"><span data-stu-id="bbe40-116">The command restores the instance database Database01 from the specified point-in-time backup to the instance database named Database01_restored.</span></span>

### <span data-ttu-id="bbe40-117">Örnek 2: bir örnek veritabanını farklı bir kaynak grubundaki başka bir örneğe geri yükleme</span><span class="sxs-lookup"><span data-stu-id="bbe40-117">Example 2: Restore a instance database from a point in time to another instance on different resource group</span></span>
```
PS C:\> Restore-AzureRmSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01" -PointInTime UTCDateTime -TargetInstanceDatabaseName "Database01_restored" -TargetInstanceName "managedInstance1" -TargetResourceGroupName "ResourceGroup02"
```

<span data-ttu-id="bbe40-118">Bu komut, kaynak grubu ResourceGroup02 managedInstance1 örneğindeki örneğindeki Database01_restored örnek veritabanına ResourceGroup01 kaynak grubu örnek veritabanı Database01 'i geri yükler.</span><span class="sxs-lookup"><span data-stu-id="bbe40-118">The command restores the instance database Database01 on instance managedInstance1 on resource group ResourceGroup01 from the specified point-in-time backup to the instance database named Database01_restored on instance managedInstance2 on resource group ResourceGroup02.</span></span>

## <span data-ttu-id="bbe40-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bbe40-119">PARAMETERS</span></span>

### <span data-ttu-id="bbe40-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="bbe40-120">-AsJob</span></span>
<span data-ttu-id="bbe40-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="bbe40-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe40-122">-DefaultProfile</span></span>
<span data-ttu-id="bbe40-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bbe40-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-124">-FromPointInTimeBackup</span><span class="sxs-lookup"><span data-stu-id="bbe40-124">-FromPointInTimeBackup</span></span>
<span data-ttu-id="bbe40-125">Bir noktadan noktaya geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="bbe40-125">Restore from a point-in-time backup.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbe40-126">-InputObject</span></span>
<span data-ttu-id="bbe40-127">Geri yüklenecek örnek veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="bbe40-127">The Instance Database object to restore</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition
Aliases: InstanceDatabase

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="bbe40-128">-InstanceName</span></span>
<span data-ttu-id="bbe40-129">Örnek adı.</span><span class="sxs-lookup"><span data-stu-id="bbe40-129">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="bbe40-130">-Name</span></span>
<span data-ttu-id="bbe40-131">Geri yüklenecek örnek veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="bbe40-131">The instance database name to restore.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-132">-Pointıntime</span><span class="sxs-lookup"><span data-stu-id="bbe40-132">-PointInTime</span></span>
<span data-ttu-id="bbe40-133">Veritabanını geri yükleme</span><span class="sxs-lookup"><span data-stu-id="bbe40-133">The point in time to restore the database to.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe40-134">-ResourceGroupName</span></span>
<span data-ttu-id="bbe40-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbe40-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bbe40-136">-ResourceId</span></span>
<span data-ttu-id="bbe40-137">Geri yüklenecek örnek veritabanı nesnesinin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="bbe40-137">The resource id of Instance Database object to restore</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeSameInstanceRestoreInstanceDatabaseFromAzureResourceId, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-138">-Targetınstancedatabasename</span><span class="sxs-lookup"><span data-stu-id="bbe40-138">-TargetInstanceDatabaseName</span></span>
<span data-ttu-id="bbe40-139">Geri yüklenecek hedef örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="bbe40-139">The name of the target instance database to restore to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-140">-Targetınstancename</span><span class="sxs-lookup"><span data-stu-id="bbe40-140">-TargetInstanceName</span></span>
<span data-ttu-id="bbe40-141">Geri yüklenecek hedef örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="bbe40-141">The name of the target instance to restore to.</span></span>
<span data-ttu-id="bbe40-142">Belirtilmemişse, hedef örnek kaynak örnekle aynıdır.</span><span class="sxs-lookup"><span data-stu-id="bbe40-142">If not specified, the target instance is the same as the source instance.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-143">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe40-143">-TargetResourceGroupName</span></span>
<span data-ttu-id="bbe40-144">Geri yüklenecek hedef kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="bbe40-144">The name of the target resource group to restore to.</span></span>
<span data-ttu-id="bbe40-145">Belirtilmemişse, hedef kaynak grubu kaynak kaynak grubuyla aynıdır.</span><span class="sxs-lookup"><span data-stu-id="bbe40-145">If not specified, the target resource group is the same as the source resource group.</span></span>

```yaml
Type: String
Parameter Sets: PointInTimeCrossInstanceRestoreInstanceDatabaseFromInputParameters, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureSqlManagedDatabaseModelInstanceDefinition, PointInTimeCrossInstanceRestoreInstanceDatabaseFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="bbe40-146">-Confirm</span></span>
<span data-ttu-id="bbe40-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bbe40-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbe40-148">-WhatIf</span></span>
<span data-ttu-id="bbe40-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bbe40-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbe40-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bbe40-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbe40-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe40-151">CommonParameters</span></span>
<span data-ttu-id="bbe40-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bbe40-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe40-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe40-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe40-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bbe40-154">INPUTS</span></span>

### <span data-ttu-id="bbe40-155">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="bbe40-155">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>
<span data-ttu-id="bbe40-156">System. String</span><span class="sxs-lookup"><span data-stu-id="bbe40-156">System.String</span></span>

## <span data-ttu-id="bbe40-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bbe40-157">OUTPUTS</span></span>

### <span data-ttu-id="bbe40-158">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="bbe40-158">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="bbe40-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bbe40-159">NOTES</span></span>

## <span data-ttu-id="bbe40-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bbe40-160">RELATED LINKS</span></span>
