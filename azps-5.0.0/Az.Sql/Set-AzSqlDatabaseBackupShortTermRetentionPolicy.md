---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278799"
---
# <span data-ttu-id="d671f-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d671f-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="d671f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d671f-102">SYNOPSIS</span></span>
<span data-ttu-id="d671f-103">Yedekleme kısa süreli bekletme ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d671f-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="d671f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d671f-104">SYNTAX</span></span>

### <span data-ttu-id="d671f-105">PolicyByResourceServerDatabaseSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d671f-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d671f-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d671f-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d671f-107">Policybyresourceıdset</span><span class="sxs-lookup"><span data-stu-id="d671f-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d671f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d671f-108">DESCRIPTION</span></span>
<span data-ttu-id="d671f-109">**Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d671f-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="d671f-110">İlke, bir defalık geri yükleme yedekleri için gün cinsinden bekletme dönemidir.</span><span class="sxs-lookup"><span data-stu-id="d671f-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="d671f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d671f-111">EXAMPLES</span></span>

### <span data-ttu-id="d671f-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d671f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="d671f-113">Bu komut, database01 için kısa süreli bekletme ilkesini 35 güne ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d671f-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="d671f-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d671f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="d671f-115">Bu komut, database01 için kısa süreli bekletme ilkesini bir veritabanı nesnesinin boruları aracılığıyla 35 gün içinde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d671f-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="d671f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d671f-116">PARAMETERS</span></span>

### <span data-ttu-id="d671f-117">-Azuressqldatabaseobject</span><span class="sxs-lookup"><span data-stu-id="d671f-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="d671f-118">İlkenin alınacağı veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d671f-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d671f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d671f-119">-DatabaseName</span></span>
<span data-ttu-id="d671f-120">Kullanılacak Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="d671f-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d671f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d671f-121">-DefaultProfile</span></span>
<span data-ttu-id="d671f-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d671f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d671f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d671f-123">-ResourceGroupName</span></span>
<span data-ttu-id="d671f-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d671f-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d671f-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d671f-125">-ResourceId</span></span>
<span data-ttu-id="d671f-126">Kısa süreli bekletme ilkesi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d671f-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="d671f-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="d671f-127">-RetentionDays</span></span>
<span data-ttu-id="d671f-128">Gün cinsinden yedekleme tutma ayarı.</span><span class="sxs-lookup"><span data-stu-id="d671f-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="d671f-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d671f-129">-ServerName</span></span>
<span data-ttu-id="d671f-130">Veritabanının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="d671f-130">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d671f-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="d671f-131">-Confirm</span></span>
<span data-ttu-id="d671f-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d671f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d671f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d671f-133">-WhatIf</span></span>
<span data-ttu-id="d671f-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d671f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d671f-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d671f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d671f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d671f-136">CommonParameters</span></span>
<span data-ttu-id="d671f-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d671f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d671f-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d671f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d671f-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d671f-139">INPUTS</span></span>

### <span data-ttu-id="d671f-140">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="d671f-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="d671f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d671f-141">System.String</span></span>

## <span data-ttu-id="d671f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d671f-142">OUTPUTS</span></span>

### <span data-ttu-id="d671f-143">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d671f-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d671f-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d671f-144">NOTES</span></span>

## <span data-ttu-id="d671f-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d671f-145">RELATED LINKS</span></span>
