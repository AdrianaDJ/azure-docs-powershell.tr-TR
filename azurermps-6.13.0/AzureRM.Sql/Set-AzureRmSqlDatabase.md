---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 283b12ca63f92086369f273b1f04d5e3f0cd1716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588036"
---
# <span data-ttu-id="c7ea9-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7ea9-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="c7ea9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ea9-103">Veritabanının özelliklerini ayarlar veya varolan bir veritabanını esnek bir havuza taşıma.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7ea9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7ea9-104">SYNTAX</span></span>

### <span data-ttu-id="c7ea9-105">Güncelleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c7ea9-105">Update (Default)</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7ea9-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="c7ea9-106">VcoreBasedDatabase</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <String>]
 [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-ZoneRedundant] [-AsJob] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7ea9-107">Adlandıramıyor</span><span class="sxs-lookup"><span data-stu-id="c7ea9-107">Rename</span></span>
```
Set-AzureRmSqlDatabase [-DatabaseName] <String> -NewName <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7ea9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7ea9-108">DESCRIPTION</span></span>
<span data-ttu-id="c7ea9-109">**Set-AzureRmSqlDatabase** cmdlet 'ı Azure SQL veritabanındaki bir veritabanının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-109">The **Set-AzureRmSqlDatabase** cmdlet sets properties for a database in Azure SQL Database.</span></span> <span data-ttu-id="c7ea9-110">Bu cmdlet, veritabanı için hizmet katmanı ( *Sürüm* ), performans düzeyi ( *Requestedserviceobjectivendı* ) ve depolama boyutu üst sınırı ( *maxsizebytes* ) seçeneğini değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-110">This cmdlet can modify the service tier ( *Edition* ), performance level ( *RequestedServiceObjectiveName* ), and storage max size ( *MaxSizeBytes* ) for the database.</span></span>  <span data-ttu-id="c7ea9-111">Ayrıca, bir veritabanını esnek bir havuza taşımak için *ela, PoolName* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-111">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span> <span data-ttu-id="c7ea9-112">Bir veritabanı zaten esnek bir havuzda yer alıyorsa, bir esnek havuzun dışına ve tek veritabanları için bir performans düzeyine taşımak için *Requestedserviceobjectivename* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-112">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to move the database out of an elastic pool and into a performance level for single databases.</span></span>

## <span data-ttu-id="c7ea9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7ea9-113">EXAMPLES</span></span>

### <span data-ttu-id="c7ea9-114">Örnek 1: veritabanını Standart S2 veritabanına güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c7ea9-114">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="c7ea9-115">Bu komut Database01 adındaki bir veritabanını server01 adlı sunucudaki standart bir S2 veritabanına güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-115">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="c7ea9-116">Örnek 2: esnek bir havuza veritabanı ekleme</span><span class="sxs-lookup"><span data-stu-id="c7ea9-116">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="c7ea9-117">Bu komut, server01 adlı sunucuda barındırılan ElasticPool01 adındaki esnek havuzuna Database01 adlı bir veritabanı ekler.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-117">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

### <span data-ttu-id="c7ea9-118">Örnek 3: veritabanının depolama boyutu üst sınırını değiştirme</span><span class="sxs-lookup"><span data-stu-id="c7ea9-118">Example 3: Modify the storage max size of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -MaxSizeBytes 1099511627776
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

<span data-ttu-id="c7ea9-119">Bu komut, Database01 adlı veritabanını, en büyük boyutunu 1 TB olarak ayarlamak için güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-119">This command updates a database named Database01 to set its max size to 1 TB.</span></span>

## <span data-ttu-id="c7ea9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7ea9-120">PARAMETERS</span></span>

### <span data-ttu-id="c7ea9-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="c7ea9-121">-AsJob</span></span>
<span data-ttu-id="c7ea9-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c7ea9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7ea9-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c7ea9-123">-ComputeGeneration</span></span>
<span data-ttu-id="c7ea9-124">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-124">The compute generation to assign.</span></span>

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

### <span data-ttu-id="c7ea9-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c7ea9-125">-DatabaseName</span></span>
<span data-ttu-id="c7ea9-126">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-126">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="c7ea9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ea9-127">-DefaultProfile</span></span>
<span data-ttu-id="c7ea9-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c7ea9-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ea9-129">-Edition</span><span class="sxs-lookup"><span data-stu-id="c7ea9-129">-Edition</span></span>
<span data-ttu-id="c7ea9-130">Veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-130">Specifies the edition for the database.</span></span>
<span data-ttu-id="c7ea9-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c7ea9-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c7ea9-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c7ea9-132">None</span></span>
- <span data-ttu-id="c7ea9-133">Ana</span><span class="sxs-lookup"><span data-stu-id="c7ea9-133">Basic</span></span>
- <span data-ttu-id="c7ea9-134">Ardından</span><span class="sxs-lookup"><span data-stu-id="c7ea9-134">Standard</span></span>
- <span data-ttu-id="c7ea9-135">Min</span><span class="sxs-lookup"><span data-stu-id="c7ea9-135">Premium</span></span>
- <span data-ttu-id="c7ea9-136">Ambarı</span><span class="sxs-lookup"><span data-stu-id="c7ea9-136">DataWarehouse</span></span>
- <span data-ttu-id="c7ea9-137">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="c7ea9-137">Free</span></span>
- <span data-ttu-id="c7ea9-138">:</span><span class="sxs-lookup"><span data-stu-id="c7ea9-138">Stretch</span></span>
- <span data-ttu-id="c7ea9-139">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="c7ea9-139">GeneralPurpose</span></span>
- <span data-ttu-id="c7ea9-140">Departmanla</span><span class="sxs-lookup"><span data-stu-id="c7ea9-140">BusinessCritical</span></span>

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

### <span data-ttu-id="c7ea9-141">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="c7ea9-141">-ElasticPoolName</span></span>
<span data-ttu-id="c7ea9-142">Veritabanının taşınacağı esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-142">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="c7ea9-143">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c7ea9-143">-LicenseType</span></span>
<span data-ttu-id="c7ea9-144">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-144">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="c7ea9-145">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="c7ea9-145">-MaxSizeBytes</span></span>
<span data-ttu-id="c7ea9-146">En büyük Azure SQL veritabanı boyutu (bayt).</span><span class="sxs-lookup"><span data-stu-id="c7ea9-146">The maximum size of the Azure SQL Database in bytes.</span></span>

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

### <span data-ttu-id="c7ea9-147">-NewName</span><span class="sxs-lookup"><span data-stu-id="c7ea9-147">-NewName</span></span>
<span data-ttu-id="c7ea9-148">Veritabanını yeniden adlandırmak için yeni ad.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-148">The new name to rename the database to.</span></span>

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

### <span data-ttu-id="c7ea9-149">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="c7ea9-149">-ReadScale</span></span>
<span data-ttu-id="c7ea9-150">Azure SQL veritabanına atanacak ölçeği oku seçeneği. (Etkin/devre dışı)</span><span class="sxs-lookup"><span data-stu-id="c7ea9-150">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="c7ea9-151">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c7ea9-151">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="c7ea9-152">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-152">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="c7ea9-153">Hizmet amaçları hakkında bilgi için, Microsoft Geliştirici ağ kitaplığındaki [Azure SQL veritabanı hizmet katmanları ve performans düzeyleri](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-153">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="c7ea9-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7ea9-154">-ResourceGroupName</span></span>
<span data-ttu-id="c7ea9-155">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-155">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c7ea9-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c7ea9-156">-ServerName</span></span>
<span data-ttu-id="c7ea9-157">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c7ea9-158">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="c7ea9-158">-Tags</span></span>
<span data-ttu-id="c7ea9-159">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-159">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c7ea9-160">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c7ea9-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c7ea9-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="c7ea9-161">-VCore</span></span>
<span data-ttu-id="c7ea9-162">Azure SQL veritabanı için Vcore numarası</span><span class="sxs-lookup"><span data-stu-id="c7ea9-162">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="c7ea9-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="c7ea9-163">-ZoneRedundant</span></span>
<span data-ttu-id="c7ea9-164">Azure SQL veritabanıyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="c7ea9-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="c7ea9-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="c7ea9-165">-Confirm</span></span>
<span data-ttu-id="c7ea9-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7ea9-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7ea9-167">-WhatIf</span></span>
<span data-ttu-id="c7ea9-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7ea9-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7ea9-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ea9-170">CommonParameters</span></span>
<span data-ttu-id="c7ea9-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7ea9-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ea9-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ea9-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ea9-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7ea9-173">INPUTS</span></span>

### <span data-ttu-id="c7ea9-174">System. String</span><span class="sxs-lookup"><span data-stu-id="c7ea9-174">System.String</span></span>

## <span data-ttu-id="c7ea9-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7ea9-175">OUTPUTS</span></span>

### <span data-ttu-id="c7ea9-176">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="c7ea9-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c7ea9-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7ea9-177">NOTES</span></span>

## <span data-ttu-id="c7ea9-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7ea9-178">RELATED LINKS</span></span>

[<span data-ttu-id="c7ea9-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7ea9-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="c7ea9-180">Yeni-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7ea9-180">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="c7ea9-181">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7ea9-181">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="c7ea9-182">Özgeçmiş-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7ea9-182">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="c7ea9-183">Askıya al-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c7ea9-183">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="c7ea9-184">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c7ea9-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
