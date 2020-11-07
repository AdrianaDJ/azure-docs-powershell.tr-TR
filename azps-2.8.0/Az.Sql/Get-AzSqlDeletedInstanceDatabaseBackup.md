---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeletedinstancedatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedInstanceDatabaseBackup.md
ms.openlocfilehash: ce68b8c8a03fbfe99adbb6070df072dd8ebb0cd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933636"
---
# <span data-ttu-id="40f49-101">Get-AzSqlDeletedInstanceDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="40f49-101">Get-AzSqlDeletedInstanceDatabaseBackup</span></span>

## <span data-ttu-id="40f49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40f49-102">SYNOPSIS</span></span>
<span data-ttu-id="40f49-103">Geri yüklediğiniz silinmiş bir veritabanını alır.</span><span class="sxs-lookup"><span data-stu-id="40f49-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="40f49-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40f49-104">SYNTAX</span></span>

### <span data-ttu-id="40f49-105">DeletedDatabaseList (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="40f49-105">DeletedDatabaseList (Default)</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40f49-106">Silinmi?</span><span class="sxs-lookup"><span data-stu-id="40f49-106">DeletedDatabaseByNameAndDeletedTime</span></span>
```
Get-AzSqlDeletedInstanceDatabaseBackup [-ResourceGroupName] <String> [-InstanceName] <String>
 -DatabaseName <String> [-DeletionDate] <DateTime> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="40f49-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="40f49-107">DESCRIPTION</span></span>
<span data-ttu-id="40f49-108">**Get-Azsqldeletedınstancedatabasebackup** cmdlet 'i, geri yüklediğiniz veya geri yüklediğiniz tüm silinmiş yedekleme veritabanı yedeklemesini alır.</span><span class="sxs-lookup"><span data-stu-id="40f49-108">The **Get-AzSqlDeletedInstanceDatabaseBackup** cmdlet gets a specified deleted SQL Instance database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="40f49-109">Bu cmdlet, Azure 'da SQL örneği genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="40f49-109">This cmdlet is also supported by the SQL Instance Stretch Database service on Azure.</span></span>

## <span data-ttu-id="40f49-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40f49-110">EXAMPLES</span></span>

### <span data-ttu-id="40f49-111">Örnek 1: sunucudaki tüm silinmiş veritabanı yedeklemelerini alma</span><span class="sxs-lookup"><span data-stu-id="40f49-111">Example 1: Get all deleted database backups on a server</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000

DeletionDate         : 2019-03-04 04:00:08 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB3
CreationDate         : 2019-03-04 03:00:31 AM
EarliestRestorePoint : 2019-03-04 03:05:23 AM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB3,13196145
                       6082100000
```

<span data-ttu-id="40f49-112">Bu komut, sunucudaki tüm silinmiş veritabanı yedeklemelerini alır.</span><span class="sxs-lookup"><span data-stu-id="40f49-112">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="40f49-113">Örnek 2: belirtilen silinmiş veritabanı yedeklemesini alma</span><span class="sxs-lookup"><span data-stu-id="40f49-113">Example 2: Get a specified deleted database backup</span></span>
```powershell
PS C:\>Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1"
DeletionDate         : 2019-03-03 12:00:17 AM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 11:00:51 PM
EarliestRestorePoint : 2019-03-02 11:05:30 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196044
                       8170400000

DeletionDate         : 2019-03-02 11:00:16 PM
ResourceGroupName    : ContosoResourceGroup
ManagedInstanceName  : ContosoServer
Name                 : DB1
CreationDate         : 2019-03-02 10:00:51 PM
EarliestRestorePoint : 2019-03-02 10:05:29 PM
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoResourceGroup/providers/Microsoft.
                       Sql/managedInstances/ContosoServer/restorableDroppedDatabases/DB1,13196041
                       2168670000
```

## <span data-ttu-id="40f49-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40f49-114">PARAMETERS</span></span>

### <span data-ttu-id="40f49-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40f49-115">-DatabaseName</span></span>
<span data-ttu-id="40f49-116">Yedekleri alacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="40f49-116">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40f49-117">-DefaultProfile</span></span>
<span data-ttu-id="40f49-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="40f49-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40f49-119">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="40f49-119">-DeletionDate</span></span>
<span data-ttu-id="40f49-120">Milisaniye duyarlılığı (örneğin 2016-02-23T00:21:22.847 Z) ile yedeklemelerin alınacağı Azure SQL örnek veritabanının silme tarihi</span><span class="sxs-lookup"><span data-stu-id="40f49-120">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DeletedDatabaseByNameAndDeletedTime
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f49-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="40f49-121">-InstanceName</span></span>
<span data-ttu-id="40f49-122">Veritabanının bulunduğu Azure SQL yönetilen örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="40f49-122">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f49-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f49-123">-ResourceGroupName</span></span>
<span data-ttu-id="40f49-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="40f49-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f49-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f49-125">CommonParameters</span></span>
<span data-ttu-id="40f49-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40f49-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f49-127">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="40f49-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f49-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40f49-128">INPUTS</span></span>

### <span data-ttu-id="40f49-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="40f49-129">None</span></span>

## <span data-ttu-id="40f49-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40f49-130">OUTPUTS</span></span>

### <span data-ttu-id="40f49-131">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. Azuressqldeletedmanageddatabasebackupmodel</span><span class="sxs-lookup"><span data-stu-id="40f49-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlDeletedManagedDatabaseBackupModel</span></span>

## <span data-ttu-id="40f49-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40f49-132">NOTES</span></span>

## <span data-ttu-id="40f49-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40f49-133">RELATED LINKS</span></span>
