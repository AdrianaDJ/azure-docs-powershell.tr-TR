---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097946"
---
# <span data-ttu-id="c4b01-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c4b01-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c4b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4b01-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b01-103">Var olan bir veritabanı için ikincil bir veritabanı oluşturur ve veri çoğaltması başlatır.</span><span class="sxs-lookup"><span data-stu-id="c4b01-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="c4b01-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4b01-104">SYNTAX</span></span>

### <span data-ttu-id="c4b01-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4b01-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4b01-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="c4b01-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4b01-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4b01-107">DESCRIPTION</span></span>
<span data-ttu-id="c4b01-108">**Yeni-AzSqlDatabaseSecondary** cmdlet 'i, veritabanında coğrafi çoğaltma ayarlamak için kullanıldığında Start-AzSqlDatabaseCopy cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="c4b01-109">Coğrafi çoğaltma bağlantı nesnesini birincili ikincil veritabanına döndürür.</span><span class="sxs-lookup"><span data-stu-id="c4b01-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="c4b01-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4b01-110">EXAMPLES</span></span>

### <span data-ttu-id="c4b01-111">1: etkin Geo-Replication oluştur</span><span class="sxs-lookup"><span data-stu-id="c4b01-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="c4b01-112">2: etkin Geo-Replication oluşturun ve iş ortağı veritabanı adını kaynak veritabanı adından farklı olacak şekilde belirtin</span><span class="sxs-lookup"><span data-stu-id="c4b01-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="c4b01-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4b01-113">PARAMETERS</span></span>

### <span data-ttu-id="c4b01-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="c4b01-114">-AllowConnections</span></span>
<span data-ttu-id="c4b01-115">İkincil Azure SQL veritabanının okuma amacını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="c4b01-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c4b01-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c4b01-117">Olsun</span><span class="sxs-lookup"><span data-stu-id="c4b01-117">No</span></span>
- <span data-ttu-id="c4b01-118">Tüm</span><span class="sxs-lookup"><span data-stu-id="c4b01-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b01-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="c4b01-119">-AsJob</span></span>
<span data-ttu-id="c4b01-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c4b01-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4b01-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4b01-121">-DatabaseName</span></span>
<span data-ttu-id="c4b01-122">Birincil olarak davranacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-122">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4b01-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b01-123">-DefaultProfile</span></span>
<span data-ttu-id="c4b01-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c4b01-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4b01-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="c4b01-125">-LicenseType</span></span>
<span data-ttu-id="c4b01-126">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="c4b01-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="c4b01-127">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4b01-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="c4b01-128">Oluşturulacak ikincil veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="c4b01-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="c4b01-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b01-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c4b01-130">Bu cmdlet 'in ikincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b01-131">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c4b01-131">-PartnerServerName</span></span>
<span data-ttu-id="c4b01-132">İkincil olarak davranacak Azure SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4b01-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b01-133">-ResourceGroupName</span></span>
<span data-ttu-id="c4b01-134">Bu cmdlet 'in birincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="c4b01-135">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="c4b01-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="c4b01-136">Azure SQL veritabanı ikincili için üretim oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="c4b01-136">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="c4b01-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c4b01-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="c4b01-138">İkincil veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="c4b01-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="c4b01-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="c4b01-140">İkincil veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="c4b01-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="c4b01-141">-SecondaryVCore</span></span>
<span data-ttu-id="c4b01-142">Azure SQL veritabanı ikincil 'ın Vcore numaraları.</span><span class="sxs-lookup"><span data-stu-id="c4b01-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="c4b01-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4b01-143">-ServerName</span></span>
<span data-ttu-id="c4b01-144">Birincil SQL veritabanının SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="c4b01-145">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="c4b01-145">-Tags</span></span>
<span data-ttu-id="c4b01-146">SQL veritabanı çoğaltma bağlantısıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="c4b01-147">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="c4b01-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="c4b01-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4b01-148">-Confirm</span></span>
<span data-ttu-id="c4b01-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4b01-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4b01-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4b01-150">-WhatIf</span></span>
<span data-ttu-id="c4b01-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4b01-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4b01-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4b01-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4b01-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b01-153">CommonParameters</span></span>
<span data-ttu-id="c4b01-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4b01-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b01-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c4b01-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b01-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4b01-156">INPUTS</span></span>

### <span data-ttu-id="c4b01-157">System. String</span><span class="sxs-lookup"><span data-stu-id="c4b01-157">System.String</span></span>

## <span data-ttu-id="c4b01-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4b01-158">OUTPUTS</span></span>

### <span data-ttu-id="c4b01-159">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="c4b01-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="c4b01-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4b01-160">NOTES</span></span>

## <span data-ttu-id="c4b01-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4b01-161">RELATED LINKS</span></span>

[<span data-ttu-id="c4b01-162">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c4b01-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c4b01-163">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c4b01-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c4b01-164">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c4b01-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
