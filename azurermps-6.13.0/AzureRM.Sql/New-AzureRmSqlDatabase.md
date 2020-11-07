---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 7eaa753b973b887cbbddc132b998d05f3e374e3a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764105"
---
# <span data-ttu-id="eec0a-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eec0a-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="eec0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eec0a-102">SYNOPSIS</span></span>
<span data-ttu-id="eec0a-103">Veritabanı veya elastik veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eec0a-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eec0a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eec0a-104">SYNTAX</span></span>

### <span data-ttu-id="eec0a-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eec0a-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <String>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eec0a-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="eec0a-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] -Edition <String> [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>]
 [-SampleName <String>] [-ZoneRedundant] [-AsJob] -VCore <Int32> -ComputeGeneration <String>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eec0a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eec0a-107">DESCRIPTION</span></span>
<span data-ttu-id="eec0a-108">**New-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eec0a-108">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>
<span data-ttu-id="eec0a-109">*Elavepoolname* parametresini varolan bir esnek havuza ayarlayarak, elastik bir veritabanı da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="eec0a-109">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="eec0a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eec0a-110">EXAMPLES</span></span>

### <span data-ttu-id="eec0a-111">Örnek 1: belirtilen sunucuda veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="eec0a-111">Example 1: Create a database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

<span data-ttu-id="eec0a-112">Bu komut, Database01 adında bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eec0a-112">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="eec0a-113">Örnek 2: belirtilen sunucuda elastik bir veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="eec0a-113">Example 2: Create an elastic database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ElasticPoolName "ElasticPool01"
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

<span data-ttu-id="eec0a-114">Bu komut, Database02 adındaki elastik havuzda ElasticPool01 Server server01 adlı bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eec0a-114">This command creates a database named Database02 in the elastic pool named ElasticPool01 on server Server01.</span></span>

### <span data-ttu-id="eec0a-115">Örnek 3: belirtilen sunucuda Vcore veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="eec0a-115">Example 3: Create an Vcore database on a specified server</span></span>
```
PS C:\>New-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database03" -Edition "GeneralPurpose" -Vcore 2 -ComputeGeneration "Gen4"
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

<span data-ttu-id="eec0a-116">Bu komut, Database03 adında bir Vcore veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="eec0a-116">This command creates a Vcore database named Database03 on server Server01.</span></span>

## <span data-ttu-id="eec0a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eec0a-117">PARAMETERS</span></span>

### <span data-ttu-id="eec0a-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="eec0a-118">-AsJob</span></span>
<span data-ttu-id="eec0a-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="eec0a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eec0a-120">-Catalogharmanlaması</span><span class="sxs-lookup"><span data-stu-id="eec0a-120">-CatalogCollation</span></span>
<span data-ttu-id="eec0a-121">SQL veritabanı kataloğu harmanlamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-121">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="eec0a-122">-CollationName</span><span class="sxs-lookup"><span data-stu-id="eec0a-122">-CollationName</span></span>
<span data-ttu-id="eec0a-123">SQL veritabanı harmanlaması adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-123">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="eec0a-124">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="eec0a-124">-ComputeGeneration</span></span>
<span data-ttu-id="eec0a-125">Atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="eec0a-125">The compute generation to assign.</span></span>

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

### <span data-ttu-id="eec0a-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eec0a-126">-DatabaseName</span></span>
<span data-ttu-id="eec0a-127">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="eec0a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eec0a-128">-DefaultProfile</span></span>
<span data-ttu-id="eec0a-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="eec0a-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eec0a-130">-Edition</span><span class="sxs-lookup"><span data-stu-id="eec0a-130">-Edition</span></span>
<span data-ttu-id="eec0a-131">Veritabanına atanacak sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-131">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="eec0a-132">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="eec0a-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eec0a-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eec0a-133">None</span></span>
- <span data-ttu-id="eec0a-134">Ana</span><span class="sxs-lookup"><span data-stu-id="eec0a-134">Basic</span></span>
- <span data-ttu-id="eec0a-135">Ardından</span><span class="sxs-lookup"><span data-stu-id="eec0a-135">Standard</span></span>
- <span data-ttu-id="eec0a-136">Min</span><span class="sxs-lookup"><span data-stu-id="eec0a-136">Premium</span></span>
- <span data-ttu-id="eec0a-137">Ambarı</span><span class="sxs-lookup"><span data-stu-id="eec0a-137">DataWarehouse</span></span>
- <span data-ttu-id="eec0a-138">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="eec0a-138">Free</span></span>
- <span data-ttu-id="eec0a-139">:</span><span class="sxs-lookup"><span data-stu-id="eec0a-139">Stretch</span></span>
- <span data-ttu-id="eec0a-140">Generalamacını</span><span class="sxs-lookup"><span data-stu-id="eec0a-140">GeneralPurpose</span></span>
- <span data-ttu-id="eec0a-141">Departmanla</span><span class="sxs-lookup"><span data-stu-id="eec0a-141">BusinessCritical</span></span>

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

### <span data-ttu-id="eec0a-142">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="eec0a-142">-ElasticPoolName</span></span>
<span data-ttu-id="eec0a-143">Veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-143">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="eec0a-144">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="eec0a-144">-LicenseType</span></span>
<span data-ttu-id="eec0a-145">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="eec0a-145">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="eec0a-146">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="eec0a-146">-MaxSizeBytes</span></span>
<span data-ttu-id="eec0a-147">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-147">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="eec0a-148">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="eec0a-148">-ReadScale</span></span>
<span data-ttu-id="eec0a-149">Azure SQL veritabanına atanacak ölçeği oku seçeneği. (Etkin/devre dışı)</span><span class="sxs-lookup"><span data-stu-id="eec0a-149">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="eec0a-150">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="eec0a-150">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="eec0a-151">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-151">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="eec0a-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eec0a-152">-ResourceGroupName</span></span>
<span data-ttu-id="eec0a-153">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-153">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="eec0a-154">-SampleName</span><span class="sxs-lookup"><span data-stu-id="eec0a-154">-SampleName</span></span>
<span data-ttu-id="eec0a-155">Bu veritabanını oluştururken uygulanacak örnek şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="eec0a-155">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="eec0a-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="eec0a-156">-ServerName</span></span>
<span data-ttu-id="eec0a-157">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-157">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="eec0a-158">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="eec0a-158">-Tags</span></span>
<span data-ttu-id="eec0a-159">Bu cmdlet 'in yeni veritabanıyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-159">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="eec0a-160">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="eec0a-160">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="eec0a-161">-VCore</span><span class="sxs-lookup"><span data-stu-id="eec0a-161">-VCore</span></span>
<span data-ttu-id="eec0a-162">Azure SQL veritabanı için Vcore numarası</span><span class="sxs-lookup"><span data-stu-id="eec0a-162">The Vcore number for the Azure Sql database</span></span>

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

### <span data-ttu-id="eec0a-163">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="eec0a-163">-ZoneRedundant</span></span>
<span data-ttu-id="eec0a-164">Azure SQL veritabanıyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="eec0a-164">The zone redundancy to associate with the Azure Sql Database</span></span>

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

### <span data-ttu-id="eec0a-165">-Onay</span><span class="sxs-lookup"><span data-stu-id="eec0a-165">-Confirm</span></span>
<span data-ttu-id="eec0a-166">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eec0a-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eec0a-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eec0a-167">-WhatIf</span></span>
<span data-ttu-id="eec0a-168">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eec0a-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eec0a-169">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eec0a-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eec0a-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eec0a-170">CommonParameters</span></span>
<span data-ttu-id="eec0a-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eec0a-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eec0a-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eec0a-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eec0a-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eec0a-173">INPUTS</span></span>

### <span data-ttu-id="eec0a-174">System. String</span><span class="sxs-lookup"><span data-stu-id="eec0a-174">System.String</span></span>

## <span data-ttu-id="eec0a-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eec0a-175">OUTPUTS</span></span>

### <span data-ttu-id="eec0a-176">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="eec0a-176">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="eec0a-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eec0a-177">NOTES</span></span>

## <span data-ttu-id="eec0a-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eec0a-178">RELATED LINKS</span></span>

[<span data-ttu-id="eec0a-179">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eec0a-179">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="eec0a-180">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="eec0a-180">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="eec0a-181">Yeni-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="eec0a-181">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="eec0a-182">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eec0a-182">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="eec0a-183">Özgeçmiş-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eec0a-183">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="eec0a-184">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eec0a-184">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="eec0a-185">Askıya al-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eec0a-185">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="eec0a-186">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="eec0a-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

