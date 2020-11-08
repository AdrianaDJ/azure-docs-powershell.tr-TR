---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 9408e51cfcdab3cd2c82617ee7f8cb9bc7d3918a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104276"
---
# <span data-ttu-id="16fe4-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="16fe4-101">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="16fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="16fe4-103">Uzun süreli bekletme yedeklemesi alır.</span><span class="sxs-lookup"><span data-stu-id="16fe4-103">Gets long term retention backup(s).</span></span>

## <span data-ttu-id="16fe4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16fe4-104">SYNTAX</span></span>

### <span data-ttu-id="16fe4-105">Konum (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16fe4-105">Location (Default)</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceGroupName <String>]
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fe4-106">InstanceName</span><span class="sxs-lookup"><span data-stu-id="16fe4-106">InstanceName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-ResourceGroupName <String>] [-OnlyLatestPerDatabase] [-DatabaseState <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fe4-107">DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16fe4-107">DatabaseName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-ResourceGroupName <String>] [-OnlyLatestPerDatabase]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fe4-108">BackupName</span><span class="sxs-lookup"><span data-stu-id="16fe4-108">BackupName</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fe4-109">Getbackupbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="16fe4-109">GetBackupByResourceId</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fe4-110">GetBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="16fe4-110">GetBackupByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-BackupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16fe4-111">GetBackupsByInputObject</span><span class="sxs-lookup"><span data-stu-id="16fe4-111">GetBackupsByInputObject</span></span>
```
Get-AzSqlInstanceDatabaseLongTermRetentionBackup [-InputObject] <AzureSqlManagedDatabaseModel>
 [-OnlyLatestPerDatabase] [-DatabaseState <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16fe4-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="16fe4-112">DESCRIPTION</span></span>
<span data-ttu-id="16fe4-113">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="16fe4-113">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="16fe4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16fe4-114">EXAMPLES</span></span>

### <span data-ttu-id="16fe4-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="16fe4-115">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


BackupExpirationTime : 3/10/2020 1:10:45 PM
BackupName           : 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
BackupTime           : 2/22/2020 6:04:15 AM
DatabaseName         : test
DatabaseDeletionTime : 2/24/2020 2:56:44 PM
Location             : southeastasia
ResourceId           : /subscriptions/f46521f3-5bb0-4eea-a3c2-c2d5987df96b/resourceGroups/testResourceGroup/providers/Microsoft.Sql/locations/southeastasia/longTermRetentionManaged
                       Instances/testInstance/longTermRetentionDatabases/test/longTermRetentionManagedInstanceBackups/15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
ManagedInstanceName  : testInstance
InstanceCreateTime   : 10/17/2019 4:52:10 PM
ResourceGroupName    : testResourceGroup
```

<span data-ttu-id="16fe4-116">Belirli bir veritabanı için tüm uzun süreli bekletme yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="16fe4-116">Gets all long term retention backups for a particular database.</span></span>  <span data-ttu-id="16fe4-117">Kaynak grubu isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="16fe4-117">Resource Group is optional.</span></span> 

## <span data-ttu-id="16fe4-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16fe4-118">PARAMETERS</span></span>

### <span data-ttu-id="16fe4-119">-BackupName</span><span class="sxs-lookup"><span data-stu-id="16fe4-119">-BackupName</span></span>
<span data-ttu-id="16fe4-120">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="16fe4-120">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: BackupName, GetBackupByInputObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16fe4-121">-DatabaseName</span></span>
<span data-ttu-id="16fe4-122">Yedeklemelerin altında olduğu yönetilen veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="16fe4-122">The name of the Managed Database the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: DatabaseName, BackupName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-123">-DatabaseState</span><span class="sxs-lookup"><span data-stu-id="16fe4-123">-DatabaseState</span></span>
<span data-ttu-id="16fe4-124">Yedekleri bulmak, canlı, silinmesini veya tamamını bulmak istediğiniz veritabanının durumu.</span><span class="sxs-lookup"><span data-stu-id="16fe4-124">The state of the database whose backups you want to find, Alive, Deleted, or All.</span></span>
<span data-ttu-id="16fe4-125">Varsayılan olarak tüm</span><span class="sxs-lookup"><span data-stu-id="16fe4-125">Defaults to All</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, GetBackupsByInputObject
Aliases:
Accepted values: All, Deleted, Live

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16fe4-126">-DefaultProfile</span></span>
<span data-ttu-id="16fe4-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="16fe4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16fe4-128">-InputObject</span></span>
<span data-ttu-id="16fe4-129">Yedeklemelerin alınacağı veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="16fe4-129">The database object to get backups for.</span></span>

```yaml
Type: AzureSqlManagedDatabaseModel
Parameter Sets: GetBackupByInputObject, GetBackupsByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-130">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="16fe4-130">-InstanceName</span></span>
<span data-ttu-id="16fe4-131">Yedeklemelerin altında olduğu yönetilen örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="16fe4-131">The name of the Managed Instance the backups are under.</span></span>

```yaml
Type: String
Parameter Sets: InstanceName, DatabaseName, BackupName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="16fe4-132">-Location</span></span>
<span data-ttu-id="16fe4-133">Yedeklemelerin kaynak yönetimli örneğinin konumu.</span><span class="sxs-lookup"><span data-stu-id="16fe4-133">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName, GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-134">-OnlyLatestPerDatabase</span><span class="sxs-lookup"><span data-stu-id="16fe4-134">-OnlyLatestPerDatabase</span></span>
<span data-ttu-id="16fe4-135">Her veritabanı için yalnızca en son yedeklemeyi alma.</span><span class="sxs-lookup"><span data-stu-id="16fe4-135">Whether or not to only get the latest backup per database.</span></span>
<span data-ttu-id="16fe4-136">Varsayılan olarak false olur.</span><span class="sxs-lookup"><span data-stu-id="16fe4-136">Defaults to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Location, InstanceName, DatabaseName, GetBackupsByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16fe4-137">-ResourceGroupName</span></span>
<span data-ttu-id="16fe4-138">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="16fe4-138">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Location, InstanceName, DatabaseName, BackupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-139">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="16fe4-139">-ResourceId</span></span>
<span data-ttu-id="16fe4-140">Yedeklemelerin alınacağı veritabanı kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="16fe4-140">The database Resource ID to get backups for.</span></span>

```yaml
Type: String
Parameter Sets: GetBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16fe4-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="16fe4-141">-Confirm</span></span>
<span data-ttu-id="16fe4-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16fe4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16fe4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16fe4-143">-WhatIf</span></span>
<span data-ttu-id="16fe4-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16fe4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16fe4-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16fe4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16fe4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16fe4-146">CommonParameters</span></span>
<span data-ttu-id="16fe4-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16fe4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16fe4-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="16fe4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16fe4-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16fe4-149">INPUTS</span></span>

### <span data-ttu-id="16fe4-150">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="16fe4-150">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

### <span data-ttu-id="16fe4-151">System. String</span><span class="sxs-lookup"><span data-stu-id="16fe4-151">System.String</span></span>

## <span data-ttu-id="16fe4-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16fe4-152">OUTPUTS</span></span>

### <span data-ttu-id="16fe4-153">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="16fe4-153">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="16fe4-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16fe4-154">NOTES</span></span>

## <span data-ttu-id="16fe4-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16fe4-155">RELATED LINKS</span></span>

[<span data-ttu-id="16fe4-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="16fe4-156">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="16fe4-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="16fe4-157">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="16fe4-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="16fe4-158">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="16fe4-159">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="16fe4-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)