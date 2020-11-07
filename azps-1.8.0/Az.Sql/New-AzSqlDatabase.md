---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabase.md
ms.openlocfilehash: ff474116854838c40a4862cf93f4d017ccdf4527
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758908"
---
# <span data-ttu-id="62bcf-101">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62bcf-101">New-AzSqlDatabase</span></span>

## <span data-ttu-id="62bcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="62bcf-103">Veritabanı veya elastik veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62bcf-103">Creates a database or an elastic database.</span></span>

## <span data-ttu-id="62bcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62bcf-104">SYNTAX</span></span>

### <span data-ttu-id="62bcf-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62bcf-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62bcf-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="62bcf-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62bcf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="62bcf-107">DESCRIPTION</span></span>
<span data-ttu-id="62bcf-108">**New-AzSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62bcf-108">The **New-AzSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="62bcf-109">*Elavepoolname* parametresini varolan bir esnek havuza ayarlayarak, elastik bir veritabanı da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62bcf-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="62bcf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62bcf-110">EXAMPLES</span></span>

### <span data-ttu-id="62bcf-111">Örnek 1: belirtilen sunucuda veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="62bcf-111">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="62bcf-112">Bu komut, Database01 adında bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62bcf-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="62bcf-113">Örnek 2: belirtilen sunucuda elastik bir veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="62bcf-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="62bcf-114">Bu komut, Database02 adındaki elastik havuzda ElasticPool01 Server server01 adlı bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62bcf-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="62bcf-115">Örnek 3: belirtilen sunucuda Vcore veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="62bcf-115">Example 3: Create an Vcore database on a specified server</span></span>
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

<span data-ttu-id="62bcf-116">Bu komut, Database03 adında bir Vcore veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="62bcf-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="62bcf-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62bcf-117">PARAMETERS</span></span>

### <span data-ttu-id="62bcf-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="62bcf-118">-AsJob</span></span>
<span data-ttu-id="62bcf-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="62bcf-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62bcf-120">-Catalogharmanlaması</span><span class="sxs-lookup"><span data-stu-id="62bcf-120">-CatalogCollation</span></span>
<span data-ttu-id="62bcf-121">SQL veritabanı kataloğu harmanlamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="62bcf-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="62bcf-122">-CollationName</span></span>
<span data-ttu-id="62bcf-123">SQL veritabanı harmanlaması adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="62bcf-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="62bcf-124">-ComputeGeneration</span></span>
<span data-ttu-id="62bcf-125">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="62bcf-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="62bcf-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="62bcf-126">-DatabaseName</span></span>
<span data-ttu-id="62bcf-127">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="62bcf-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62bcf-128">-DefaultProfile</span></span>
<span data-ttu-id="62bcf-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="62bcf-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62bcf-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="62bcf-130">-Edition</span></span>
<span data-ttu-id="62bcf-131">Veritabanına atanacak sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="62bcf-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="62bcf-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="62bcf-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="62bcf-133">None</span></span>
- <span data-ttu-id="62bcf-134">Ana</span><span class="sxs-lookup"><span data-stu-id="62bcf-134">Basic</span></span>
- <span data-ttu-id="62bcf-135">Ardından</span><span class="sxs-lookup"><span data-stu-id="62bcf-135">Standard</span></span>
- <span data-ttu-id="62bcf-136">Min</span><span class="sxs-lookup"><span data-stu-id="62bcf-136">Premium</span></span>
- <span data-ttu-id="62bcf-137">Ambarı</span><span class="sxs-lookup"><span data-stu-id="62bcf-137">DataWarehouse</span></span>
- <span data-ttu-id="62bcf-138">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="62bcf-138">Free</span></span>
- <span data-ttu-id="62bcf-139">:</span><span class="sxs-lookup"><span data-stu-id="62bcf-139">Stretch</span></span>
- <span data-ttu-id="62bcf-140">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="62bcf-140">GeneralPurpose</span></span>
- <span data-ttu-id="62bcf-141">Departmanla</span><span class="sxs-lookup"><span data-stu-id="62bcf-141">BusinessCritical</span></span>

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

### <span data-ttu-id="62bcf-142">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="62bcf-142">-ElasticPoolName</span></span>
<span data-ttu-id="62bcf-143">Veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="62bcf-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="62bcf-144">-LicenseType</span></span>
<span data-ttu-id="62bcf-145">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="62bcf-145">The license type for the Azure Sql database.</span></span> <span data-ttu-id="62bcf-146">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="62bcf-146">Possible values are:</span></span>
- <span data-ttu-id="62bcf-147">Temel fiyat-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirimli fiyatlandırması uygulanır.</span><span class="sxs-lookup"><span data-stu-id="62bcf-147">BasePrice - Azure Hybrid Benefit (AHB) discounted pricing for existing SQL Server license owners is applied.</span></span> <span data-ttu-id="62bcf-148">Var olan SQL Server lisans sahipleri için veritabanı fiyatı düşülecektir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-148">Database price will be discounted for existing SQL Server license owners.</span></span>
- <span data-ttu-id="62bcf-149">Licenseeklenmiş-Azure Karma avantajı (AHB) mevcut SQL Server lisans sahiplerinin indirim fiyatlandırması uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="62bcf-149">LicenseIncluded - Azure Hybrid Benefit (AHB) discount pricing for existing SQL Server license owners is not applied.</span></span> <span data-ttu-id="62bcf-150">Veritabanı fiyatı Yeni bir SQL Server lisans maliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-150">Database price will include a new SQL Server license costs.</span></span>

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

### <span data-ttu-id="62bcf-151">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="62bcf-151">-MaxSizeBytes</span></span>
<span data-ttu-id="62bcf-152">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-152">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="62bcf-153">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="62bcf-153">-ReadScale</span></span>
<span data-ttu-id="62bcf-154">Azure SQL veritabanına atanacak ölçeği oku seçeneği. (Etkin/devre dışı)</span><span class="sxs-lookup"><span data-stu-id="62bcf-154">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="62bcf-155">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="62bcf-155">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="62bcf-156">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-156">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="62bcf-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62bcf-157">-ResourceGroupName</span></span>
<span data-ttu-id="62bcf-158">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-158">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="62bcf-159">-SampleName</span><span class="sxs-lookup"><span data-stu-id="62bcf-159">-SampleName</span></span>
<span data-ttu-id="62bcf-160">Bu veritabanını oluştururken uygulanacak örnek şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="62bcf-160">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="62bcf-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62bcf-161">-ServerName</span></span>
<span data-ttu-id="62bcf-162">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-162">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="62bcf-163">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="62bcf-163">-Tags</span></span>
<span data-ttu-id="62bcf-164">Bu cmdlet 'in yeni veritabanıyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-164">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="62bcf-165">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="62bcf-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="62bcf-166">-VCore</span><span class="sxs-lookup"><span data-stu-id="62bcf-166">-VCore</span></span>
<span data-ttu-id="62bcf-167">Azure SQL veritabanı için Vcore numarası</span><span class="sxs-lookup"><span data-stu-id="62bcf-167">The Vcore number for the Azure Sql database</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62bcf-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="62bcf-168">-ZoneRedundant</span></span>
<span data-ttu-id="62bcf-169">Azure SQL veritabanıyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="62bcf-169">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="62bcf-170">-Onay</span><span class="sxs-lookup"><span data-stu-id="62bcf-170">-Confirm</span></span>
<span data-ttu-id="62bcf-171">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62bcf-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62bcf-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62bcf-172">-WhatIf</span></span>
<span data-ttu-id="62bcf-173">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62bcf-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62bcf-174">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62bcf-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62bcf-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62bcf-175">CommonParameters</span></span>
<span data-ttu-id="62bcf-176">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62bcf-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62bcf-177">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62bcf-177">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62bcf-178">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62bcf-178">INPUTS</span></span>

### <span data-ttu-id="62bcf-179">System. String</span><span class="sxs-lookup"><span data-stu-id="62bcf-179">System.String</span></span>

## <span data-ttu-id="62bcf-180">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62bcf-180">OUTPUTS</span></span>

### <span data-ttu-id="62bcf-181">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="62bcf-181">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="62bcf-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62bcf-182">NOTES</span></span>

## <span data-ttu-id="62bcf-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62bcf-183">RELATED LINKS</span></span>

[<span data-ttu-id="62bcf-184">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62bcf-184">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="62bcf-185">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="62bcf-185">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="62bcf-186">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="62bcf-186">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="62bcf-187">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62bcf-187">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="62bcf-188">Özgeçmiş-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62bcf-188">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="62bcf-189">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62bcf-189">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="62bcf-190">Askıya al-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="62bcf-190">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="62bcf-191">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="62bcf-191">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

