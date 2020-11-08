---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: 264fecd37738a0da484c28f1ec8ce84f14efe159
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278287"
---
# <span data-ttu-id="5aa38-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5aa38-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="5aa38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aa38-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa38-103">Veritabanı veya elastik veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5aa38-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="5aa38-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5aa38-104">SYNTAX</span></span>

### <span data-ttu-id="5aa38-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5aa38-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-Force] [-LicenseType <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5aa38-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="5aa38-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] [-Force] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ComputeModel <String>] [-AutoPauseDelayInMinutes <Int32>]
 [-MinimumCapacity <Double>] [-ReadReplicaCount <Int32>] [-BackupStorageRedundancy <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aa38-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5aa38-107">DESCRIPTION</span></span>
<span data-ttu-id="5aa38-108">**New-AzSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5aa38-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="5aa38-109">*Elavepoolname* parametresini varolan bir esnek havuza ayarlayarak, elastik bir veritabanı da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5aa38-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="5aa38-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5aa38-110">EXAMPLES</span></span>

### <span data-ttu-id="5aa38-111">Örnek 1: belirtilen sunucuda veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5aa38-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="5aa38-112">Bu komut, Database01 adında bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5aa38-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="5aa38-113">Örnek 2: belirtilen sunucuda elastik bir veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5aa38-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02" -ElasticPoolName "ElasticPool01"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database02
Location                      : Central US
DatabaseId                    : 7bd9d561-42a7-484e-bf05-62ddef8015ab
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : ElasticPool01
EarliestRestoreDate           :
LicenseType                   :
Tags                          :
```

<span data-ttu-id="5aa38-114">Bu komut, Database02 adındaki elastik havuzda ElasticPool01 Server server01 adlı bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5aa38-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="5aa38-115">Örnek 3: belirtilen sunucuda Vcore veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5aa38-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database03
Location                      : Central US
DatabaseId                    : 34d9d561-42a7-484e-bf05-62ddef8000ab
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 8/26/2015 10:04:29 PM
CurrentServiceObjectiveName   : GP_Gen4_2
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
LicenseType                   : LicenseIncluded
Tags                          :
```

<span data-ttu-id="5aa38-116">Bu komut, Database03 adında bir Vcore veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5aa38-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

### <span data-ttu-id="5aa38-117">Örnek 4: belirtilen sunucuda bir sunucusuz veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5aa38-117">Example 4: Create an Serverless database on the specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database04" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen5" -ComputeModel Serverless
ResourceGroupName             : ResourceGroup01
ServerName                    : Server01
DatabaseName                  : Database04
Location                      : Central US
DatabaseId                    : ef5a9698-012c-4def-8d94-7f6bfb7b4f04
Edition                       : GeneralPurpose
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              :
MaxSizeBytes                  : 34359738368
Status                        : Online
CreationDate                  : 4/12/2019 11:20:29 PM
CurrentServiceObjectiveName   : GP_S_Gen5_2
RequestedServiceObjectiveName : GP_S_Gen5_2
ElasticPoolName               :
EarliestRestoreDate           : 4/12/2019 11:50:29 PM
Tags                          :
CreateMode                    :
ReadScale                     : Disabled
ZoneRedundant                 : False
Capacity                      : 2
Family                        : Gen5
SkuName                       : GP_S_Gen5
LicenseType                   : LicenseIncluded
AutoPauseDelayInMinutes       : 360
MinimumCapacity          : 0.5
```

<span data-ttu-id="5aa38-118">Bu komut, Database04 adlı sunucuda server01 adında bir sunucusuz veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5aa38-118">This command creates a Serverless database named Database04 on server Server01.</span></span>

## <span data-ttu-id="5aa38-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5aa38-119">PARAMETERS</span></span>

### <span data-ttu-id="5aa38-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="5aa38-120">-AsJob</span></span>
<span data-ttu-id="5aa38-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5aa38-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5aa38-122">-Autopausedelayınminutes</span><span class="sxs-lookup"><span data-stu-id="5aa38-122">-AutoPauseDelayInMinutes</span></span>
<span data-ttu-id="5aa38-123">Veritabanı için otomatik duraklatma gecikmesi (yalnızca sunucusuz);</span><span class="sxs-lookup"><span data-stu-id="5aa38-123">The auto pause delay in minutes for database(serverless only), -1 to opt out</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-124">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="5aa38-124">-BackupStorageRedundancy</span></span>
<span data-ttu-id="5aa38-125">Yedekleme depolama yedeği, SQL veritabanının yedeklerini depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5aa38-125">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="5aa38-126">Seçenekler şunlardır: yerel, bölge ve coğrafi.</span><span class="sxs-lookup"><span data-stu-id="5aa38-126">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="5aa38-127">-Catalogharmanlaması</span><span class="sxs-lookup"><span data-stu-id="5aa38-127">-CatalogCollation</span></span>
<span data-ttu-id="5aa38-128">SQL veritabanı kataloğu harmanlamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-128">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-129">-CollationName</span><span class="sxs-lookup"><span data-stu-id="5aa38-129">-CollationName</span></span>
<span data-ttu-id="5aa38-130">SQL veritabanı harmanlaması adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-130">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-131">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5aa38-131">-ComputeGeneration</span></span>
<span data-ttu-id="5aa38-132">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="5aa38-132">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-133">-ComputeModel</span><span class="sxs-lookup"><span data-stu-id="5aa38-133">-ComputeModel</span></span>
<span data-ttu-id="5aa38-134">Azure SQL veritabanı için işlem modeli.</span><span class="sxs-lookup"><span data-stu-id="5aa38-134">The compute model for Azure Sql database.</span></span> <span data-ttu-id="5aa38-135">Sunucusuz veya sağlanan</span><span class="sxs-lookup"><span data-stu-id="5aa38-135">Serverless or Provisioned</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-136">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5aa38-136">-DatabaseName</span></span>
<span data-ttu-id="5aa38-137">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-137">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa38-138">-DefaultProfile</span></span>
<span data-ttu-id="5aa38-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5aa38-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aa38-140">-Edition</span><span class="sxs-lookup"><span data-stu-id="5aa38-140">-Edition</span></span>
<span data-ttu-id="5aa38-141">Veritabanına atanacak sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-141">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="5aa38-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5aa38-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5aa38-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5aa38-143">None</span></span>
- <span data-ttu-id="5aa38-144">Ana</span><span class="sxs-lookup"><span data-stu-id="5aa38-144">Basic</span></span>
- <span data-ttu-id="5aa38-145">Ardından</span><span class="sxs-lookup"><span data-stu-id="5aa38-145">Standard</span></span>
- <span data-ttu-id="5aa38-146">Min</span><span class="sxs-lookup"><span data-stu-id="5aa38-146">Premium</span></span>
- <span data-ttu-id="5aa38-147">Ambarı</span><span class="sxs-lookup"><span data-stu-id="5aa38-147">DataWarehouse</span></span>
- <span data-ttu-id="5aa38-148">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="5aa38-148">Free</span></span>
- <span data-ttu-id="5aa38-149">:</span><span class="sxs-lookup"><span data-stu-id="5aa38-149">Stretch</span></span>
- <span data-ttu-id="5aa38-150">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="5aa38-150">GeneralPurpose</span></span>
- <span data-ttu-id="5aa38-151">Departmanla</span><span class="sxs-lookup"><span data-stu-id="5aa38-151">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-152">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="5aa38-152">-ElasticPoolName</span></span>
<span data-ttu-id="5aa38-153">Veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-153">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-154">-Force</span><span class="sxs-lookup"><span data-stu-id="5aa38-154">-Force</span></span>
<span data-ttu-id="5aa38-155">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="5aa38-155">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="5aa38-156">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5aa38-156">-LicenseType</span></span>
<span data-ttu-id="5aa38-157">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="5aa38-157">The license type for the Azure Sql database.</span></span> <span data-ttu-id="5aa38-158">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="5aa38-158">Possible values are:</span></span>
- <span data-ttu-id="5aa38-159">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5aa38-159">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="5aa38-160">Var olan SQL Server lisans sahipleri için veritabanı fiyatı düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-160">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="5aa38-161">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="5aa38-161">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="5aa38-162">Veritabanı fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-162">Database price will include a new SQL Server license costs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-163">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5aa38-163">-MaxSizeBytes</span></span>
<span data-ttu-id="5aa38-164">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-164">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-165">-Minimumkapasite</span><span class="sxs-lookup"><span data-stu-id="5aa38-165">-MinimumCapacity</span></span>
<span data-ttu-id="5aa38-166">Duraklatılmışsa veritabanının her zaman tahsis edileceği en az kapasite.</span><span class="sxs-lookup"><span data-stu-id="5aa38-166">The Minimal capacity that database will always have allocated, if not paused.</span></span>
<span data-ttu-id="5aa38-167">Yalnızca sunucusuz Azure SQL veritabanları için.</span><span class="sxs-lookup"><span data-stu-id="5aa38-167">For serverless Azure Sql databases only.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases: MinVCore, MinCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-168">-ReadReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5aa38-168">-ReadReplicaCount</span></span>
<span data-ttu-id="5aa38-169">ReadOnly uygulama hedefi bağlantılarının yönlendirilebilmesi veritabanıyla ilişkili salt okunur ikincil çoğaltmaların sayısı.</span><span class="sxs-lookup"><span data-stu-id="5aa38-169">The number of readonly secondary replicas associated with the database to which readonly application intent connections may be routed.</span></span> <span data-ttu-id="5aa38-170">Bu özellik yalnızca Hiperscale sürümü veritabanları için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-170">This property is only settable for Hyperscale edition databases.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-171">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="5aa38-171">-ReadScale</span></span>
<span data-ttu-id="5aa38-172">Etkinse, bağlantı dizesinde salt okunur olarak ayarlanmış olan bağlantılar salt okunur bir ikincil yinelemeye yönlendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-172">If enabled, connections that have application intent set to readonly in their connection string may be routed to a readonly secondary replica.</span></span> <span data-ttu-id="5aa38-173">Bu özellik yalnızca Premium ve Business Critical veritabanları için ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-173">This property is only settable for Premium and Business Critical databases.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-174">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5aa38-174">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="5aa38-175">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-175">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-176">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa38-176">-ResourceGroupName</span></span>
<span data-ttu-id="5aa38-177">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-177">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5aa38-178">-SampleName</span><span class="sxs-lookup"><span data-stu-id="5aa38-178">-SampleName</span></span>
<span data-ttu-id="5aa38-179">Bu veritabanını oluştururken uygulanacak örnek şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="5aa38-179">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-180">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5aa38-180">-ServerName</span></span>
<span data-ttu-id="5aa38-181">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-181">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5aa38-182">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="5aa38-182">-Tags</span></span>
<span data-ttu-id="5aa38-183">Bu cmdlet 'in yeni veritabanıyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-183">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="5aa38-184">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="5aa38-184">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="5aa38-185">-VCore</span></span>
<span data-ttu-id="5aa38-186">Azure SQL veritabanı için Vcore numarası</span><span class="sxs-lookup"><span data-stu-id="5aa38-186">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity, MaxVCore, MaxCapacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aa38-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5aa38-187">-ZoneRedundant</span></span>
<span data-ttu-id="5aa38-188">Azure SQL veritabanıyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="5aa38-188">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="5aa38-189">-Onay</span><span class="sxs-lookup"><span data-stu-id="5aa38-189">-Confirm</span></span>
<span data-ttu-id="5aa38-190">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5aa38-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aa38-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aa38-191">-WhatIf</span></span>
<span data-ttu-id="5aa38-192">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5aa38-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa38-193">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5aa38-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aa38-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa38-194">CommonParameters</span></span>
<span data-ttu-id="5aa38-195">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5aa38-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa38-196">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5aa38-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa38-197">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5aa38-197">INPUTS</span></span>

### <span data-ttu-id="5aa38-198">System. String</span><span class="sxs-lookup"><span data-stu-id="5aa38-198">System.String</span></span>

## <span data-ttu-id="5aa38-199">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5aa38-199">OUTPUTS</span></span>

### <span data-ttu-id="5aa38-200">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="5aa38-200">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5aa38-201">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5aa38-201">NOTES</span></span>

## <span data-ttu-id="5aa38-202">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5aa38-202">RELATED LINKS</span></span>

[<span data-ttu-id="5aa38-203">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5aa38-203">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5aa38-204">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="5aa38-204">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="5aa38-205">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="5aa38-205">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="5aa38-206">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5aa38-206">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5aa38-207">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5aa38-207">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5aa38-208">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5aa38-208">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="5aa38-209">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5aa38-209">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5aa38-210">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5aa38-210">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

