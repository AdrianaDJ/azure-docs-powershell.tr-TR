---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 6ec4e3163d1bcd388ef0b4b8813ece89a41bfd23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933758"
---
# <span data-ttu-id="34eeb-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="34eeb-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="34eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="34eeb-103">Yedekleme kısa süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34eeb-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="34eeb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34eeb-104">SYNTAX</span></span>

### <span data-ttu-id="34eeb-105">Policybyresourceınstancedatabaseset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34eeb-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34eeb-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="34eeb-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34eeb-107">Policybyresourceıdset</span><span class="sxs-lookup"><span data-stu-id="34eeb-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34eeb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="34eeb-108">DESCRIPTION</span></span>
<span data-ttu-id="34eeb-109">**Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="34eeb-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="34eeb-110">İlke, bir defalık geri yükleme yedekleri için gün cinsinden bekletme dönemidir.</span><span class="sxs-lookup"><span data-stu-id="34eeb-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="34eeb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34eeb-111">EXAMPLES</span></span>

### <span data-ttu-id="34eeb-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34eeb-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="34eeb-113">Bu komut, database01 için kısa süreli bekletme ilkesini 35 güne ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34eeb-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="34eeb-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="34eeb-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="34eeb-115">Bu komut, database01 için kısa süreli bekletme ilkesini bir veritabanı nesnesinin boruları aracılığıyla 35 gün içinde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34eeb-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="34eeb-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="34eeb-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="34eeb-117">Bu komut, silinmiş bir veritabanı nesnesinde DB1 adındaki tüm silinmiş veritabanları için kısa süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34eeb-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="34eeb-118">Not yalnızca silinen veritabanlarında bekletme süresini azaltabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34eeb-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="34eeb-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34eeb-119">PARAMETERS</span></span>

### <span data-ttu-id="34eeb-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="34eeb-120">-DatabaseName</span></span>
<span data-ttu-id="34eeb-121">Yedekleri alacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="34eeb-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34eeb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34eeb-122">-DefaultProfile</span></span>
<span data-ttu-id="34eeb-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34eeb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34eeb-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="34eeb-124">-DeletionDate</span></span>
<span data-ttu-id="34eeb-125">Milisaniye duyarlılığı (örneğin 2016-02-23T00:21:22.847 Z) ile yedeklemelerin alınacağı Azure SQL örnek veritabanının silme tarihi</span><span class="sxs-lookup"><span data-stu-id="34eeb-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34eeb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34eeb-126">-InputObject</span></span>
<span data-ttu-id="34eeb-127">İlkesi alınacak/ayarlanacak olan Live veya Deleted veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="34eeb-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34eeb-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="34eeb-128">-InstanceName</span></span>
<span data-ttu-id="34eeb-129">Veritabanının bulunduğu Azure SQL yönetilen örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="34eeb-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34eeb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34eeb-130">-ResourceGroupName</span></span>
<span data-ttu-id="34eeb-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="34eeb-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34eeb-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="34eeb-132">-ResourceId</span></span>
<span data-ttu-id="34eeb-133">Kısa süreli bekletme ilkesi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="34eeb-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34eeb-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="34eeb-134">-RetentionDays</span></span>
<span data-ttu-id="34eeb-135">Günlük yedekleme</span><span class="sxs-lookup"><span data-stu-id="34eeb-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34eeb-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="34eeb-136">-Confirm</span></span>
<span data-ttu-id="34eeb-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34eeb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34eeb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34eeb-138">-WhatIf</span></span>
<span data-ttu-id="34eeb-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34eeb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34eeb-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34eeb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34eeb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34eeb-141">CommonParameters</span></span>
<span data-ttu-id="34eeb-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34eeb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34eeb-143">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34eeb-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34eeb-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34eeb-144">INPUTS</span></span>

### <span data-ttu-id="34eeb-145">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasebasemodel</span><span class="sxs-lookup"><span data-stu-id="34eeb-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="34eeb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="34eeb-146">System.String</span></span>

## <span data-ttu-id="34eeb-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34eeb-147">OUTPUTS</span></span>

### <span data-ttu-id="34eeb-148">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="34eeb-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="34eeb-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34eeb-149">NOTES</span></span>

## <span data-ttu-id="34eeb-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34eeb-150">RELATED LINKS</span></span>