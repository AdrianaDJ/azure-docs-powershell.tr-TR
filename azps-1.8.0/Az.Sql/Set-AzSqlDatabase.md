---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabase.md
ms.openlocfilehash: 62823ec87758142b34490f24d3e1b24e0c434f85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758807"
---
# <span data-ttu-id="5cf8e-101">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5cf8e-101">Set-AzSqlDatabase</span></span>

## <span data-ttu-id="5cf8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cf8e-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf8e-103">Veritabanının özelliklerini ayarlar veya varolan bir veritabanını esnek bir havuza taşıma.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

## <span data-ttu-id="5cf8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cf8e-104">SYNTAX</span></span>

### <span data-ttu-id="5cf8e-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5cf8e-105">Update (Default)</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cf8e-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="5cf8e-106">VcoreBasedDatabase</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cf8e-107">Adlandıramıyor</span><span class="sxs-lookup"><span data-stu-id="5cf8e-107">Rename</span></span>
```
Set-AzSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cf8e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cf8e-108">DESCRIPTION</span></span>
<span data-ttu-id="5cf8e-109">**Set-AzSqlDatabase** cmdlet 'ı Azure SQL veritabanında bir veritabanının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-109">The **Set-AzSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="5cf8e-110">Bu cmdlet, veritabanı için hizmet katmanı ( *Sürüm* ), performans düzeyi ( *Requestedserviceobjectivendı* ) ve depolama boyutu üst sınırı ( *maxsizebytes* ) seçeneğini değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="5cf8e-111">Ayrıca, bir veritabanını esnek bir havuza taşımak için *ela, PoolName* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="5cf8e-112">Bir veritabanı zaten esnek bir havuzda yer alıyorsa, bir esnek havuzun dışına ve tek veritabanları için bir performans düzeyine taşımak için *Requestedserviceobjectivename* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="5cf8e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cf8e-113">EXAMPLES</span></span>

### <span data-ttu-id="5cf8e-114">Örnek 1: veritabanını Standart S0 veritabanında güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5cf8e-114">Example 1: Update a database to a Standard S0 database</span></span>
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

<span data-ttu-id="5cf8e-115">Bu komut Database01 adlı bir sunucudaki server01 adındaki Standart S0 veritabanına güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-115">This command updates a database named Database01 to a Standard S0 database on a server named Server01.</span></span>

### <span data-ttu-id="5cf8e-116">Örnek 2: esnek bir havuza veritabanı ekleme</span><span class="sxs-lookup"><span data-stu-id="5cf8e-116">Example 2: Add a database to an elastic pool</span></span>
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

<span data-ttu-id="5cf8e-117">Bu komut, server01 adlı sunucuda barındırılan ElasticPool01 adındaki esnek havuzuna Database01 adlı bir veritabanı ekler.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="5cf8e-118">Örnek 3: veritabanının depolama boyutu üst sınırını değiştirme</span><span class="sxs-lookup"><span data-stu-id="5cf8e-118">Example 3: Modify the storage max size of a database</span></span>
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

<span data-ttu-id="5cf8e-119">Bu komut, Database01 adlı veritabanını, en büyük boyutunu 1 TB olarak ayarlamak için güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="5cf8e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cf8e-120">PARAMETERS</span></span>

### <span data-ttu-id="5cf8e-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="5cf8e-121">-AsJob</span></span>
<span data-ttu-id="5cf8e-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5cf8e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5cf8e-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5cf8e-123">-ComputeGeneration</span></span>
<span data-ttu-id="5cf8e-124">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="5cf8e-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5cf8e-125">-DatabaseName</span></span>
<span data-ttu-id="5cf8e-126">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-126">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="5cf8e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf8e-127">-DefaultProfile</span></span>
<span data-ttu-id="5cf8e-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5cf8e-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cf8e-129">-Edition</span><span class="sxs-lookup"><span data-stu-id="5cf8e-129">-Edition</span></span>
<span data-ttu-id="5cf8e-130">Veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="5cf8e-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5cf8e-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5cf8e-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5cf8e-132">None</span></span>
- <span data-ttu-id="5cf8e-133">Ana</span><span class="sxs-lookup"><span data-stu-id="5cf8e-133">Basic</span></span>
- <span data-ttu-id="5cf8e-134">Ardından</span><span class="sxs-lookup"><span data-stu-id="5cf8e-134">Standard</span></span>
- <span data-ttu-id="5cf8e-135">Min</span><span class="sxs-lookup"><span data-stu-id="5cf8e-135">Premium</span></span>
- <span data-ttu-id="5cf8e-136">Ambarı</span><span class="sxs-lookup"><span data-stu-id="5cf8e-136">DataWarehouse</span></span>
- <span data-ttu-id="5cf8e-137">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="5cf8e-137">Free</span></span>
- <span data-ttu-id="5cf8e-138">:</span><span class="sxs-lookup"><span data-stu-id="5cf8e-138">Stretch</span></span>
- <span data-ttu-id="5cf8e-139">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="5cf8e-139">GeneralPurpose</span></span>
- <span data-ttu-id="5cf8e-140">Departmanla</span><span class="sxs-lookup"><span data-stu-id="5cf8e-140">BusinessCritical</span></span>

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

### <span data-ttu-id="5cf8e-141">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="5cf8e-141">-ElasticPoolName</span></span>
<span data-ttu-id="5cf8e-142">Veritabanının taşınacağı esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-142">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="5cf8e-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5cf8e-143">-LicenseType</span></span>
<span data-ttu-id="5cf8e-144">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-144">The license type for the Azure Sql database.</span></span> <span data-ttu-id="5cf8e-145">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="5cf8e-145">Possible values are:</span></span>
- <span data-ttu-id="5cf8e-146">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-146">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="5cf8e-147">Var olan SQL Server lisans sahipleri için veritabanı fiyatı düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-147">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="5cf8e-148">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-148">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="5cf8e-149">Veritabanı fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-149">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="5cf8e-150">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5cf8e-150">-MaxSizeBytes</span></span>
<span data-ttu-id="5cf8e-151">En büyük Azure SQL veritabanı boyutu (bayt).</span><span class="sxs-lookup"><span data-stu-id="5cf8e-151">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="5cf8e-152">-NewName</span><span class="sxs-lookup"><span data-stu-id="5cf8e-152">-NewName</span></span>
<span data-ttu-id="5cf8e-153">Veritabanını yeniden adlandırmak için yeni ad.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-153">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="5cf8e-154">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="5cf8e-154">-ReadScale</span></span>
<span data-ttu-id="5cf8e-155">Azure SQL veritabanına atanacak ölçeği oku seçeneği. (Etkin/devre dışı)</span><span class="sxs-lookup"><span data-stu-id="5cf8e-155">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="5cf8e-156">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5cf8e-156">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="5cf8e-157">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-157">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="5cf8e-158">Hizmet amaçları hakkında bilgi için, Microsoft Geliştirici ağ kitaplığındaki [Azure SQL veritabanı hizmet katmanları ve performans düzeyleri](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-158">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-dtu-resource-limits-single-databases) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="5cf8e-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf8e-159">-ResourceGroupName</span></span>
<span data-ttu-id="5cf8e-160">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-160">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5cf8e-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5cf8e-161">-ServerName</span></span>
<span data-ttu-id="5cf8e-162">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5cf8e-163">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="5cf8e-163">-Tags</span></span>
<span data-ttu-id="5cf8e-164">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5cf8e-165">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="5cf8e-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5cf8e-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="5cf8e-166">-VCore</span></span>
<span data-ttu-id="5cf8e-167">Azure SQL veritabanı için Vcore numarası</span><span class="sxs-lookup"><span data-stu-id="5cf8e-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf8e-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="5cf8e-168">-ZoneRedundant</span></span>
<span data-ttu-id="5cf8e-169">Azure SQL veritabanıyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="5cf8e-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="5cf8e-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="5cf8e-170">-Confirm</span></span>
<span data-ttu-id="5cf8e-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cf8e-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cf8e-172">-WhatIf</span></span>
<span data-ttu-id="5cf8e-173">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cf8e-174">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cf8e-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf8e-175">CommonParameters</span></span>
<span data-ttu-id="5cf8e-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf8e-177">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5cf8e-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf8e-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cf8e-178">INPUTS</span></span>

### <span data-ttu-id="5cf8e-179">System. String</span><span class="sxs-lookup"><span data-stu-id="5cf8e-179">System.String</span></span>

## <span data-ttu-id="5cf8e-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cf8e-180">OUTPUTS</span></span>

### <span data-ttu-id="5cf8e-181">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="5cf8e-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5cf8e-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cf8e-182">NOTES</span></span>

## <span data-ttu-id="5cf8e-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cf8e-183">RELATED LINKS</span></span>

[<span data-ttu-id="5cf8e-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5cf8e-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5cf8e-185">Yeni-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5cf8e-185">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5cf8e-186">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5cf8e-186">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="5cf8e-187">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5cf8e-187">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5cf8e-188">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5cf8e-188">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5cf8e-189">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="5cf8e-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)