---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 0b0934ffe9a5721ff08438ca7a24d97e2b4a34cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276981"
---
# <span data-ttu-id="37f9b-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="37f9b-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="37f9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37f9b-102">SYNOPSIS</span></span>
<span data-ttu-id="37f9b-103">Var olan bir veritabanı için ikincil bir veritabanı oluşturur ve veri çoğaltması başlatır.</span><span class="sxs-lookup"><span data-stu-id="37f9b-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="37f9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37f9b-104">SYNTAX</span></span>

### <span data-ttu-id="37f9b-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37f9b-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37f9b-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="37f9b-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37f9b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="37f9b-107">DESCRIPTION</span></span>
<span data-ttu-id="37f9b-108">**Yeni-AzSqlDatabaseSecondary** cmdlet 'i, veritabanında coğrafi çoğaltma ayarlamak için kullanıldığında Start-AzSqlDatabaseCopy cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="37f9b-109">Coğrafi çoğaltma bağlantı nesnesini birincili ikincil veritabanına döndürür.</span><span class="sxs-lookup"><span data-stu-id="37f9b-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="37f9b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37f9b-110">EXAMPLES</span></span>

### <span data-ttu-id="37f9b-111">Örnek 1: etkin Geo-Replication oluştur</span><span class="sxs-lookup"><span data-stu-id="37f9b-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="37f9b-112">Örnek 2: etkin Geo-Replication oluşturun ve iş ortağı veritabanı adını kaynak veritabanı adından farklı olacak şekilde belirtin</span><span class="sxs-lookup"><span data-stu-id="37f9b-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="37f9b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37f9b-113">PARAMETERS</span></span>

### <span data-ttu-id="37f9b-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="37f9b-114">-AllowConnections</span></span>
<span data-ttu-id="37f9b-115">İkincil Azure SQL veritabanının okuma amacını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="37f9b-116">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="37f9b-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37f9b-117">Olsun</span><span class="sxs-lookup"><span data-stu-id="37f9b-117">No</span></span>
- <span data-ttu-id="37f9b-118">Tüm</span><span class="sxs-lookup"><span data-stu-id="37f9b-118">All</span></span>

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

### <span data-ttu-id="37f9b-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="37f9b-119">-AsJob</span></span>
<span data-ttu-id="37f9b-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="37f9b-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37f9b-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="37f9b-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="37f9b-122">Yedekleme depolama yedeği, SQL veritabanının yedeklerini depolamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="37f9b-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="37f9b-123">Seçenekler şunlardır: yerel, bölge ve coğrafi.</span><span class="sxs-lookup"><span data-stu-id="37f9b-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="37f9b-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="37f9b-124">-DatabaseName</span></span>
<span data-ttu-id="37f9b-125">Birincil olarak davranacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="37f9b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f9b-126">-DefaultProfile</span></span>
<span data-ttu-id="37f9b-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="37f9b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37f9b-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="37f9b-128">-LicenseType</span></span>
<span data-ttu-id="37f9b-129">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="37f9b-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="37f9b-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="37f9b-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="37f9b-131">Oluşturulacak ikincil veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="37f9b-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="37f9b-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37f9b-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="37f9b-133">Bu cmdlet 'in ikincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="37f9b-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="37f9b-134">-PartnerServerName</span></span>
<span data-ttu-id="37f9b-135">İkincil olarak davranacak Azure SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="37f9b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37f9b-136">-ResourceGroupName</span></span>
<span data-ttu-id="37f9b-137">Bu cmdlet 'in birincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="37f9b-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="37f9b-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="37f9b-139">Azure SQL veritabanı ikincili için üretim oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="37f9b-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="37f9b-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="37f9b-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="37f9b-141">İkincil veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="37f9b-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="37f9b-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="37f9b-143">İkincil veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="37f9b-144">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="37f9b-144">-SecondaryVCore</span></span>
<span data-ttu-id="37f9b-145">Azure SQL veritabanı ikincil 'ın Vcore numaraları.</span><span class="sxs-lookup"><span data-stu-id="37f9b-145">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="37f9b-146">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37f9b-146">-ServerName</span></span>
<span data-ttu-id="37f9b-147">Birincil SQL veritabanının SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-147">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="37f9b-148">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="37f9b-148">-Tags</span></span>
<span data-ttu-id="37f9b-149">SQL veritabanı çoğaltma bağlantısıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-149">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="37f9b-150">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="37f9b-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="37f9b-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="37f9b-151">-Confirm</span></span>
<span data-ttu-id="37f9b-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37f9b-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37f9b-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37f9b-153">-WhatIf</span></span>
<span data-ttu-id="37f9b-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37f9b-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37f9b-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="37f9b-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37f9b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f9b-156">CommonParameters</span></span>
<span data-ttu-id="37f9b-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37f9b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f9b-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="37f9b-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f9b-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37f9b-159">INPUTS</span></span>

### <span data-ttu-id="37f9b-160">System. String</span><span class="sxs-lookup"><span data-stu-id="37f9b-160">System.String</span></span>

## <span data-ttu-id="37f9b-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37f9b-161">OUTPUTS</span></span>

### <span data-ttu-id="37f9b-162">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="37f9b-162">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="37f9b-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37f9b-163">NOTES</span></span>

## <span data-ttu-id="37f9b-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37f9b-164">RELATED LINKS</span></span>

[<span data-ttu-id="37f9b-165">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="37f9b-165">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="37f9b-166">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="37f9b-166">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="37f9b-167">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="37f9b-167">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
