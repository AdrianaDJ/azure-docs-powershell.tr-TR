---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: f236c00f50d9ec74a98def114d08ab851e5a89f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276965"
---
# <span data-ttu-id="ccf7f-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccf7f-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="ccf7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf7f-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf7f-103">Veritabanının özelliklerini ayarlar veya varolan bir veritabanını esnek bir havuza taşıma.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="ccf7f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccf7f-104">SYNTAX</span></span>

### <span data-ttu-id="ccf7f-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ccf7f-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf7f-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="ccf7f-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ComputeModel <String>]
 [-AutoPauseDelayInMinutes <Int32>] [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccf7f-107">Adlandıramıyor</span><span class="sxs-lookup"><span data-stu-id="ccf7f-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf7f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccf7f-108">DESCRIPTION</span></span>
<span data-ttu-id="ccf7f-109">**Set-AzSqlDatabase** cmdlet 'ı Azure SQL veritabanında bir veritabanının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="ccf7f-110">Bu cmdlet, veritabanı için hizmet katmanı ( *Sürüm* ), performans düzeyi ( *Requestedserviceobjectivendı* ) ve depolama boyutu üst sınırı ( *maxsizebytes* ) seçeneğini değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="ccf7f-111">Ayrıca, bir veritabanını esnek bir havuza taşımak için *ela, PoolName* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="ccf7f-112">Bir veritabanı zaten esnek bir havuzda yer alıyorsa, bir esnek havuzun dışına ve tek veritabanları için bir performans düzeyine taşımak için *Requestedserviceobjectivename* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="ccf7f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccf7f-113">EXAMPLES</span></span>

### <span data-ttu-id="ccf7f-114">Örnek 1: veritabanını Standart S0 veritabanında güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ccf7f-114">Example 1: Update a database to a Standard S0 database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S0"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="ccf7f-115">Bu komut Database01 adlı bir sunucudaki server01 adındaki Standart S0 veritabanına güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="ccf7f-116">Örnek 2: esnek bir havuza veritabanı ekleme</span><span class="sxs-lookup"><span data-stu-id="ccf7f-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="ccf7f-117">Bu komut, server01 adlı sunucuda barındırılan ElasticPool01 adındaki esnek havuzuna Database01 adlı bir veritabanı ekler.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="ccf7f-118">Örnek 3: veritabanının depolama boyutu üst sınırını değiştirme</span><span class="sxs-lookup"><span data-stu-id="ccf7f-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 1099511627776
Status                        : Online
CreationDate                  : 8/24/2017 9:00:37 AM
CurrentServiceObjectiveId     : 789681b8-ca10-4eb0-bdf2-e0b050601b40
CurrentServiceObjectiveName   : S3
RequestedServiceObjectiveId   : 789681b8-ca10-4eb0-bdf2-e0b050601b40
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="ccf7f-119">Bu komut, Database01 adlı veritabanını, en büyük boyutunu 1 TB olarak ayarlamak için güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="ccf7f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccf7f-120">PARAMETERS</span></span>

### <span data-ttu-id="ccf7f-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="ccf7f-121">-AsJob</span></span>
<span data-ttu-id="ccf7f-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ccf7f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccf7f-123">-Autopausedelayınminutes</span><span class="sxs-lookup"><span data-stu-id="ccf7f-123">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="ccf7f-124">Veritabanı için otomatik duraklatma gecikmesi (yalnızca sunucusuz);</span><span class="sxs-lookup"><span data-stu-id="ccf7f-124">The auto pause delay in minutes for database (serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-125">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ccf7f-125">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ccf7f-126">Yedekleme depolama yedeği, SQL veritabanının yedeklerini depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-126">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="ccf7f-127">Seçenekler şunlardır: yerel, bölge ve coğrafi.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-127">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-128">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ccf7f-128">-ComputeGeneration</span></span>
<span data-ttu-id="ccf7f-129">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-129">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-130">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="ccf7f-130">-ComputeModel</span></span>
<span data-ttu-id="ccf7f-131">Azure SQL veritabanının hesaplanan modeli.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-131">Computed model of Azure Sql database.</span></span> <span data-ttu-id="ccf7f-132">Sunucusuz veya sağlanan</span><span class="sxs-lookup"><span data-stu-id="ccf7f-132">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ccf7f-133">-DatabaseName</span></span>
<span data-ttu-id="ccf7f-134">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-134">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf7f-135">-DefaultProfile</span></span>
<span data-ttu-id="ccf7f-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ccf7f-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccf7f-137">-Edition</span><span class="sxs-lookup"><span data-stu-id="ccf7f-137">-Edition</span></span>
<span data-ttu-id="ccf7f-138">Veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-138">Specifies the edition for the database.</span></span>
<span data-ttu-id="ccf7f-139">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ccf7f-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ccf7f-140">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ccf7f-140">None</span></span>
- <span data-ttu-id="ccf7f-141">Ana</span><span class="sxs-lookup"><span data-stu-id="ccf7f-141">Basic</span></span>
- <span data-ttu-id="ccf7f-142">Ardından</span><span class="sxs-lookup"><span data-stu-id="ccf7f-142">Standard</span></span>
- <span data-ttu-id="ccf7f-143">Min</span><span class="sxs-lookup"><span data-stu-id="ccf7f-143">Premium</span></span>
- <span data-ttu-id="ccf7f-144">Ambarı</span><span class="sxs-lookup"><span data-stu-id="ccf7f-144">DataWarehouse</span></span>
- <span data-ttu-id="ccf7f-145">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="ccf7f-145">Free</span></span>
- <span data-ttu-id="ccf7f-146">:</span><span class="sxs-lookup"><span data-stu-id="ccf7f-146">Stretch</span></span>
- <span data-ttu-id="ccf7f-147">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="ccf7f-147">GeneralPurpose</span></span>
- <span data-ttu-id="ccf7f-148">Departmanla</span><span class="sxs-lookup"><span data-stu-id="ccf7f-148">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-149">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="ccf7f-149">-ElasticPoolName</span></span>
<span data-ttu-id="ccf7f-150">Veritabanının taşınacağı esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-150">Specifies name of the elastic pool in which to move the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-151">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ccf7f-151">-LicenseType</span></span>
<span data-ttu-id="ccf7f-152">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-152">The license type for the Azure Sql database.</span></span> <span data-ttu-id="ccf7f-153">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="ccf7f-153">Possible values are:</span></span>
- <span data-ttu-id="ccf7f-154">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-154">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="ccf7f-155">Var olan SQL Server lisans sahipleri için veritabanı fiyatı düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-155">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="ccf7f-156">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-156">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="ccf7f-157">Veritabanı fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-157">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-158">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="ccf7f-158">-MaxSizeBytes</span></span>
<span data-ttu-id="ccf7f-159">En büyük Azure SQL veritabanı boyutu (bayt).</span><span class="sxs-lookup"><span data-stu-id="ccf7f-159">The maximum size of the Azure SQL Database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-160">-Minimumkapasite</span><span class="sxs-lookup"><span data-stu-id="ccf7f-160">-MinimumCapacity</span></span>
<span data-ttu-id="ccf7f-161">Duraklatılmışsa veritabanının her zaman tahsis edileceği en az kapasite.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-161">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="ccf7f-162">Yalnızca sunucusuz Azure SQL veritabanları için.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-162">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: Update, VcoreBasedDatabase
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-163">-NewName</span><span class="sxs-lookup"><span data-stu-id="ccf7f-163">-NewName</span></span>
<span data-ttu-id="ccf7f-164">Veritabanını yeniden adlandırmak için yeni ad.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-164">The new name to rename the database to.</span></span>

```yaml
Type: System.String
Parameter Sets: Rename
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-165">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="ccf7f-165">-ReadReplicaCount</span></span>
<span data-ttu-id="ccf7f-166">Veritabanıyla ilişkili salt okunur ikincil çoğaltmaların sayısı.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-166">The number of readonly secondary replicas associated with the database.</span></span>  <span data-ttu-id="ccf7f-167">Yalnızca Hyperscale Edition için.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-167">For Hyperscale edition only.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-168">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="ccf7f-168">-ReadScale</span></span>
<span data-ttu-id="ccf7f-169">Etkinse, bağlantı dizesinde salt okunur olarak ayarlanmış olan bağlantılar salt okunur bir ikincil yinelemeye yönlendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-169">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="ccf7f-170">Bu özellik yalnızca Premium ve Business Critical veritabanları için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-170">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: Update, VcoreBasedDatabase
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-171">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ccf7f-171">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="ccf7f-172">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-172">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="ccf7f-173">Hizmet amaçları hakkında bilgi için, Microsoft Geliştirici ağ kitaplığındaki [Azure SQL veritabanı hizmet katmanları ve performans düzeyleri](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-173">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-174">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf7f-174">-ResourceGroupName</span></span>
<span data-ttu-id="ccf7f-175">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-175">Specifies the name of resource group to which the server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-176">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ccf7f-176">-ServerName</span></span>
<span data-ttu-id="ccf7f-177">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-177">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-178">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="ccf7f-178">-Tags</span></span>
<span data-ttu-id="ccf7f-179">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-179">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ccf7f-180">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="ccf7f-180">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Update, VcoreBasedDatabase
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-181">-VCore</span><span class="sxs-lookup"><span data-stu-id="ccf7f-181">-VCore</span></span>
<span data-ttu-id="ccf7f-182">Azure SQL veritabanı için Vcore numarası</span><span class="sxs-lookup"><span data-stu-id="ccf7f-182">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-183">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="ccf7f-183">-ZoneRedundant</span></span>
<span data-ttu-id="ccf7f-184">Azure SQL veritabanıyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="ccf7f-184">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Update, VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-185">-Onay</span><span class="sxs-lookup"><span data-stu-id="ccf7f-185">-Confirm</span></span>
<span data-ttu-id="ccf7f-186">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-186">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-187">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf7f-187">-WhatIf</span></span>
<span data-ttu-id="ccf7f-188">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-188">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf7f-189">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-189">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf7f-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf7f-190">CommonParameters</span></span>
<span data-ttu-id="ccf7f-191">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf7f-192">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ccf7f-192">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf7f-193">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccf7f-193">INPUTS</span></span>

### <span data-ttu-id="ccf7f-194">System. String</span><span class="sxs-lookup"><span data-stu-id="ccf7f-194">System.String</span></span>

## <span data-ttu-id="ccf7f-195">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccf7f-195">OUTPUTS</span></span>

### <span data-ttu-id="ccf7f-196">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="ccf7f-196">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="ccf7f-197">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccf7f-197">NOTES</span></span>

## <span data-ttu-id="ccf7f-198">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccf7f-198">RELATED LINKS</span></span>

[<span data-ttu-id="ccf7f-199">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccf7f-199">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="ccf7f-200">Yeni-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccf7f-200">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="ccf7f-201">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccf7f-201">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="ccf7f-202">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccf7f-202">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="ccf7f-203">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="ccf7f-203">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="ccf7f-204">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ccf7f-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
