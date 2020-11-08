---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279446"
---
# <span data-ttu-id="05363-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="05363-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="05363-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05363-102">SYNOPSIS</span></span>
<span data-ttu-id="05363-103">Yedekleme kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="05363-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="05363-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="05363-104">SYNTAX</span></span>

### <span data-ttu-id="05363-105">Policybyresourceınstancedatabaseset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="05363-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05363-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="05363-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05363-107">Policybyresourceıdset</span><span class="sxs-lookup"><span data-stu-id="05363-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05363-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="05363-108">DESCRIPTION</span></span>
<span data-ttu-id="05363-109">**Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="05363-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="05363-110">İlke, bir defalık geri yükleme yedekleri için gün cinsinden bekletme dönemidir.</span><span class="sxs-lookup"><span data-stu-id="05363-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="05363-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="05363-111">EXAMPLES</span></span>

### <span data-ttu-id="05363-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="05363-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="05363-113">Bu komut, database01 için kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="05363-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="05363-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="05363-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="05363-115">Bu komut, database01 için kısa süreli bekletme ilkesini bir veritabanı nesnesinde boru ile alır.</span><span class="sxs-lookup"><span data-stu-id="05363-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="05363-116">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="05363-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="05363-117">Bu komut, silinmiş bir veritabanı nesnesinde database01 adındaki tüm silinmiş veritabanları için kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="05363-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="05363-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="05363-118">PARAMETERS</span></span>

### <span data-ttu-id="05363-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="05363-119">-DatabaseName</span></span>
<span data-ttu-id="05363-120">Yedekleri alacak Azure SQL örneği veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="05363-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="05363-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05363-121">-DefaultProfile</span></span>
<span data-ttu-id="05363-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="05363-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05363-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="05363-123">-DeletionDate</span></span>
<span data-ttu-id="05363-124">Milisaniye duyarlılığı (örneğin 2016-02-23T00:21:22.847 Z) ile yedeklemelerin alınacağı Azure SQL örnek veritabanının silme tarihi</span><span class="sxs-lookup"><span data-stu-id="05363-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="05363-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05363-125">-InputObject</span></span>
<span data-ttu-id="05363-126">İlkesi alınacak/ayarlanacak olan Live veya Deleted veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="05363-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05363-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="05363-127">-InstanceName</span></span>
<span data-ttu-id="05363-128">Veritabanının bulunduğu Azure SQL yönetilen örneğinin adı.</span><span class="sxs-lookup"><span data-stu-id="05363-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="05363-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05363-129">-ResourceGroupName</span></span>
<span data-ttu-id="05363-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="05363-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="05363-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="05363-131">-ResourceId</span></span>
<span data-ttu-id="05363-132">Kısa süreli bekletme ilkesi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="05363-132">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05363-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05363-133">CommonParameters</span></span>
<span data-ttu-id="05363-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="05363-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05363-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="05363-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05363-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="05363-136">INPUTS</span></span>

### <span data-ttu-id="05363-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. Azuressqlmanageddatabasebasemodel</span><span class="sxs-lookup"><span data-stu-id="05363-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="05363-138">System. String</span><span class="sxs-lookup"><span data-stu-id="05363-138">System.String</span></span>

## <span data-ttu-id="05363-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="05363-139">OUTPUTS</span></span>

### <span data-ttu-id="05363-140">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="05363-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="05363-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="05363-141">NOTES</span></span>

## <span data-ttu-id="05363-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="05363-142">RELATED LINKS</span></span>
