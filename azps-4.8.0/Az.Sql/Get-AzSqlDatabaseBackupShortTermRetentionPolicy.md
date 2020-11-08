---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266837"
---
# <span data-ttu-id="d9fac-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d9fac-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="d9fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9fac-102">SYNOPSIS</span></span>
<span data-ttu-id="d9fac-103">Yedekleme kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d9fac-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="d9fac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9fac-104">SYNTAX</span></span>

### <span data-ttu-id="d9fac-105">PolicyByResourceServerDatabaseSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d9fac-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9fac-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9fac-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9fac-107">Policybyresourceıdset</span><span class="sxs-lookup"><span data-stu-id="d9fac-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9fac-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9fac-108">DESCRIPTION</span></span>
<span data-ttu-id="d9fac-109">**Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet 'i, bu veritabanına kaydedilen kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d9fac-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="d9fac-110">İlke, bir defalık geri yükleme yedekleri için gün cinsinden bekletme dönemidir.</span><span class="sxs-lookup"><span data-stu-id="d9fac-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="d9fac-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9fac-111">EXAMPLES</span></span>

### <span data-ttu-id="d9fac-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d9fac-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="d9fac-113">Bu komut, database01 için kısa süreli bekletme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d9fac-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="d9fac-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d9fac-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="d9fac-115">Bu komut, database01 için kısa süreli bekletme ilkesini bir veritabanı nesnesinde boru ile alır.</span><span class="sxs-lookup"><span data-stu-id="d9fac-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="d9fac-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9fac-116">PARAMETERS</span></span>

### <span data-ttu-id="d9fac-117">-Azuressqldatabaseobject</span><span class="sxs-lookup"><span data-stu-id="d9fac-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="d9fac-118">İlkenin alınacağı veritabanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d9fac-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="d9fac-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d9fac-119">-DatabaseName</span></span>
<span data-ttu-id="d9fac-120">Kullanılacak Azure SQL veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="d9fac-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="d9fac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9fac-121">-DefaultProfile</span></span>
<span data-ttu-id="d9fac-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9fac-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9fac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9fac-123">-ResourceGroupName</span></span>
<span data-ttu-id="d9fac-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d9fac-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d9fac-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d9fac-125">-ResourceId</span></span>
<span data-ttu-id="d9fac-126">Kısa süreli bekletme ilkesi kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="d9fac-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="d9fac-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d9fac-127">-ServerName</span></span>
<span data-ttu-id="d9fac-128">Veritabanının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="d9fac-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="d9fac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9fac-129">CommonParameters</span></span>
<span data-ttu-id="d9fac-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9fac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9fac-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d9fac-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9fac-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9fac-132">INPUTS</span></span>

### <span data-ttu-id="d9fac-133">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="d9fac-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="d9fac-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d9fac-134">System.String</span></span>

## <span data-ttu-id="d9fac-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9fac-135">OUTPUTS</span></span>

### <span data-ttu-id="d9fac-136">Microsoft. Azure. Commands. Sql. Backup. model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d9fac-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d9fac-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9fac-137">NOTES</span></span>

## <span data-ttu-id="d9fac-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9fac-138">RELATED LINKS</span></span>
