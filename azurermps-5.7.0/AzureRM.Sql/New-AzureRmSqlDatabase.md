---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: f5fc78f3e06150f3283e35c23bf80edce4f47650
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592384"
---
# <span data-ttu-id="4eb54-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4eb54-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="4eb54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4eb54-102">SYNOPSIS</span></span>
<span data-ttu-id="4eb54-103">Veritabanı veya elastik veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4eb54-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4eb54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4eb54-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ZoneRedundant] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4eb54-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4eb54-105">DESCRIPTION</span></span>
<span data-ttu-id="4eb54-106">**New-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4eb54-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="4eb54-107">*Elavepoolname* parametresini varolan bir esnek havuza ayarlayarak, elastik bir veritabanı da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4eb54-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="4eb54-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4eb54-108">EXAMPLES</span></span>

### <span data-ttu-id="4eb54-109">Örnek 1: belirtilen sunucuda veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4eb54-109">Example 1: Create a database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="4eb54-110">Bu komut, Database01 adında bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4eb54-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="4eb54-111">Örnek 2: belirtilen sunucuda elastik bir veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="4eb54-111">Example 2: Create an elastic database on a specified server</span></span>
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
Tags                          :
```

<span data-ttu-id="4eb54-112">Bu komut, Database01 adındaki elastik havuzda ElasticPool01 Server server01 adlı bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4eb54-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="4eb54-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4eb54-113">PARAMETERS</span></span>

### <span data-ttu-id="4eb54-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="4eb54-114">-AsJob</span></span>
<span data-ttu-id="4eb54-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4eb54-115">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-116">-Catalogharmanlaması</span><span class="sxs-lookup"><span data-stu-id="4eb54-116">-CatalogCollation</span></span>
<span data-ttu-id="4eb54-117">SQL veritabanı kataloğu harmanlamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-117">Specifies the name of the SQL database catalog collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-118">-CollationName</span><span class="sxs-lookup"><span data-stu-id="4eb54-118">-CollationName</span></span>
<span data-ttu-id="4eb54-119">SQL veritabanı harmanlaması adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-119">Specifies the name of the SQL database collation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4eb54-120">-DatabaseName</span></span>
<span data-ttu-id="4eb54-121">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-121">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4eb54-122">-DefaultProfile</span></span>
<span data-ttu-id="4eb54-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4eb54-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-124">-Edition</span><span class="sxs-lookup"><span data-stu-id="4eb54-124">-Edition</span></span>
<span data-ttu-id="4eb54-125">Veritabanına atanacak sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-125">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="4eb54-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4eb54-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4eb54-127">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="4eb54-127">Default</span></span>
- <span data-ttu-id="4eb54-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4eb54-128">None</span></span>
- <span data-ttu-id="4eb54-129">Min</span><span class="sxs-lookup"><span data-stu-id="4eb54-129">Premium</span></span>
- <span data-ttu-id="4eb54-130">Ana</span><span class="sxs-lookup"><span data-stu-id="4eb54-130">Basic</span></span>
- <span data-ttu-id="4eb54-131">Ardından</span><span class="sxs-lookup"><span data-stu-id="4eb54-131">Standard</span></span>
- <span data-ttu-id="4eb54-132">Ambarı</span><span class="sxs-lookup"><span data-stu-id="4eb54-132">DataWarehouse</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-133">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="4eb54-133">-ElasticPoolName</span></span>
<span data-ttu-id="4eb54-134">Veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-134">Specifies the name of the elastic pool in which to put the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-135">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="4eb54-135">-MaxSizeBytes</span></span>
<span data-ttu-id="4eb54-136">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-136">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-137">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="4eb54-137">-ReadScale</span></span>
<span data-ttu-id="4eb54-138">Azure SQL veritabanına atanacak ölçeği oku seçeneği. (Etkin/devre dışı)</span><span class="sxs-lookup"><span data-stu-id="4eb54-138">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

```yaml
Type: DatabaseReadScale
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-139">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4eb54-139">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="4eb54-140">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-140">Specifies the name of the service objective to assign to the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4eb54-141">-ResourceGroupName</span></span>
<span data-ttu-id="4eb54-142">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-142">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-143">-SampleName</span><span class="sxs-lookup"><span data-stu-id="4eb54-143">-SampleName</span></span>
<span data-ttu-id="4eb54-144">Bu veritabanını oluştururken uygulanacak örnek şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="4eb54-144">The name of the sample schema to apply when creating this database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: AdventureWorksLT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4eb54-145">-ServerName</span></span>
<span data-ttu-id="4eb54-146">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-146">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-147">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="4eb54-147">-Tags</span></span>
<span data-ttu-id="4eb54-148">Bu cmdlet 'in yeni veritabanıyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-148">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="4eb54-149">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="4eb54-149">For example:</span></span>

<span data-ttu-id="4eb54-150">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="4eb54-150">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-151">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="4eb54-151">-ZoneRedundant</span></span>
<span data-ttu-id="4eb54-152">Azure SQL veritabanıyla ilişkilendirilecek bölge fazlalığı</span><span class="sxs-lookup"><span data-stu-id="4eb54-152">The zone redundancy to associate with the Azure Sql Database</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="4eb54-153">-Confirm</span></span>
<span data-ttu-id="4eb54-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4eb54-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4eb54-155">-WhatIf</span></span>
<span data-ttu-id="4eb54-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4eb54-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4eb54-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4eb54-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4eb54-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4eb54-158">CommonParameters</span></span>
<span data-ttu-id="4eb54-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4eb54-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4eb54-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4eb54-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4eb54-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4eb54-161">INPUTS</span></span>

### <span data-ttu-id="4eb54-162">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4eb54-162">None</span></span>
<span data-ttu-id="4eb54-163">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4eb54-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4eb54-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4eb54-164">OUTPUTS</span></span>

### <span data-ttu-id="4eb54-165">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="4eb54-165">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4eb54-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4eb54-166">NOTES</span></span>

## <span data-ttu-id="4eb54-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4eb54-167">RELATED LINKS</span></span>

[<span data-ttu-id="4eb54-168">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4eb54-168">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="4eb54-169">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="4eb54-169">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4eb54-170">Yeni-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="4eb54-170">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="4eb54-171">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4eb54-171">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="4eb54-172">Özgeçmiş-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4eb54-172">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="4eb54-173">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4eb54-173">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="4eb54-174">Askıya al-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4eb54-174">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="4eb54-175">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="4eb54-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
