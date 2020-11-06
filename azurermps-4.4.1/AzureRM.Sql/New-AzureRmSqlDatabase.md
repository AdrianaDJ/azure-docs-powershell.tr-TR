---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D2DB7821-A7D2-4017-8522-78793DDE040E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabase.md
ms.openlocfilehash: 22b74b3dcd76577d7c864a3779d12c8474c431a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587752"
---
# <span data-ttu-id="1b526-101">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b526-101">New-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="1b526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b526-102">SYNOPSIS</span></span>
<span data-ttu-id="1b526-103">Veritabanı veya elastik veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b526-103">Creates a database or an elastic database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b526-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b526-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabase -DatabaseName <String> [-CollationName <String>] [-CatalogCollation <String>]
 [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>] [-RequestedServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>] [-Tags <Hashtable>] [-SampleName <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b526-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b526-105">DESCRIPTION</span></span>
<span data-ttu-id="1b526-106">**New-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b526-106">The **New-AzureRmSqlDatabase** cmdlet creates an Azure SQL database.</span></span>

<span data-ttu-id="1b526-107">*Elavepoolname* parametresini varolan bir esnek havuza ayarlayarak, elastik bir veritabanı da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1b526-107">You can also create an elastic database by setting the *ElasticPoolName* parameter to an existing elastic pool.</span></span>

## <span data-ttu-id="1b526-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b526-108">EXAMPLES</span></span>

### <span data-ttu-id="1b526-109">Örnek 1: belirtilen sunucuda veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1b526-109">Example 1: Create a database on a specified server</span></span>
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

<span data-ttu-id="1b526-110">Bu komut, Database01 adında bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b526-110">This command creates a database named Database01 on server Server01.</span></span>

### <span data-ttu-id="1b526-111">Örnek 2: belirtilen sunucuda elastik bir veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="1b526-111">Example 2: Create an elastic database on a specified server</span></span>
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

<span data-ttu-id="1b526-112">Bu komut, Database01 adındaki elastik havuzda ElasticPool01 Server server01 adlı bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1b526-112">This command creates a database named Database01 in the elastic pool named ElasticPool01 on server Server01.</span></span>

## <span data-ttu-id="1b526-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b526-113">PARAMETERS</span></span>

### <span data-ttu-id="1b526-114">-Catalogharmanlaması</span><span class="sxs-lookup"><span data-stu-id="1b526-114">-CatalogCollation</span></span>
<span data-ttu-id="1b526-115">SQL veritabanı kataloğu harmanlamasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-115">Specifies the name of the SQL database catalog collation.</span></span>

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

### <span data-ttu-id="1b526-116">-CollationName</span><span class="sxs-lookup"><span data-stu-id="1b526-116">-CollationName</span></span>
<span data-ttu-id="1b526-117">SQL veritabanı harmanlaması adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-117">Specifies the name of the SQL database collation.</span></span>

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

### <span data-ttu-id="1b526-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b526-118">-DatabaseName</span></span>
<span data-ttu-id="1b526-119">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-119">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1b526-120">-Edition</span><span class="sxs-lookup"><span data-stu-id="1b526-120">-Edition</span></span>
<span data-ttu-id="1b526-121">Veritabanına atanacak sürümü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-121">Specifies the edition to assign to the database.</span></span> <span data-ttu-id="1b526-122">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1b526-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1b526-123">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="1b526-123">Default</span></span>
- <span data-ttu-id="1b526-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1b526-124">None</span></span>
- <span data-ttu-id="1b526-125">Min</span><span class="sxs-lookup"><span data-stu-id="1b526-125">Premium</span></span>
- <span data-ttu-id="1b526-126">Ana</span><span class="sxs-lookup"><span data-stu-id="1b526-126">Basic</span></span>
- <span data-ttu-id="1b526-127">Ardından</span><span class="sxs-lookup"><span data-stu-id="1b526-127">Standard</span></span>
- <span data-ttu-id="1b526-128">Ambarı</span><span class="sxs-lookup"><span data-stu-id="1b526-128">DataWarehouse</span></span>
- <span data-ttu-id="1b526-129">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="1b526-129">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b526-130">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="1b526-130">-ElasticPoolName</span></span>
<span data-ttu-id="1b526-131">Veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-131">Specifies the name of the elastic pool in which to put the database.</span></span>

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

### <span data-ttu-id="1b526-132">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="1b526-132">-MaxSizeBytes</span></span>
<span data-ttu-id="1b526-133">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-133">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="1b526-134">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="1b526-134">-ReadScale</span></span>
<span data-ttu-id="1b526-135">Azure SQL veritabanına atanacak ölçeği oku seçeneği. (Etkin/devre dışı)</span><span class="sxs-lookup"><span data-stu-id="1b526-135">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="1b526-136">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1b526-136">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="1b526-137">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-137">Specifies the name of the service objective to assign to the database.</span></span>

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

### <span data-ttu-id="1b526-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b526-138">-ResourceGroupName</span></span>
<span data-ttu-id="1b526-139">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-139">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1b526-140">-SampleName</span><span class="sxs-lookup"><span data-stu-id="1b526-140">-SampleName</span></span>
<span data-ttu-id="1b526-141">Bu veritabanını oluştururken uygulanacak örnek şemanın adı.</span><span class="sxs-lookup"><span data-stu-id="1b526-141">The name of the sample schema to apply when creating this database.</span></span>

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

### <span data-ttu-id="1b526-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1b526-142">-ServerName</span></span>
<span data-ttu-id="1b526-143">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-143">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="1b526-144">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="1b526-144">-Tags</span></span>
<span data-ttu-id="1b526-145">Bu cmdlet 'in yeni veritabanıyla ilişki kurduğu karma tablo biçimindeki anahtar-değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b526-145">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the new database.</span></span> <span data-ttu-id="1b526-146">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="1b526-146">For example:</span></span>

<span data-ttu-id="1b526-147">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="1b526-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1b526-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b526-148">-Confirm</span></span>
<span data-ttu-id="1b526-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b526-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b526-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b526-150">-WhatIf</span></span>
<span data-ttu-id="1b526-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b526-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b526-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b526-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b526-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b526-153">-DefaultProfile</span></span>
<span data-ttu-id="1b526-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b526-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b526-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b526-155">CommonParameters</span></span>
<span data-ttu-id="1b526-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b526-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b526-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b526-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b526-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b526-158">INPUTS</span></span>

## <span data-ttu-id="1b526-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b526-159">OUTPUTS</span></span>

### <span data-ttu-id="1b526-160">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="1b526-160">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1b526-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b526-161">NOTES</span></span>

## <span data-ttu-id="1b526-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b526-162">RELATED LINKS</span></span>

[<span data-ttu-id="1b526-163">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b526-163">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="1b526-164">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="1b526-164">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="1b526-165">Yeni-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="1b526-165">New-AzureRmSqlServer</span></span>](./New-AzureRmSqlServer.md)

[<span data-ttu-id="1b526-166">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b526-166">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="1b526-167">Özgeçmiş-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b526-167">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="1b526-168">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b526-168">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="1b526-169">Askıya al-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b526-169">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="1b526-170">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="1b526-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
