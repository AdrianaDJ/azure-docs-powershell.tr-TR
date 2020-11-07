---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: e39239b7434d61642ad5fcfc1f487ac5bbc5829a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758895"
---
# <span data-ttu-id="9dfe3-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9dfe3-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="9dfe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dfe3-102">SYNOPSIS</span></span>
<span data-ttu-id="9dfe3-103">Var olan bir veritabanı için ikincil bir veritabanı oluşturur ve veri çoğaltması başlatır.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="9dfe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9dfe3-104">SYNTAX</span></span>

### <span data-ttu-id="9dfe3-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9dfe3-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dfe3-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="9dfe3-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9dfe3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9dfe3-107">DESCRIPTION</span></span>
<span data-ttu-id="9dfe3-108">**Yeni-AzSqlDatabaseSecondary** cmdlet 'i, veritabanında coğrafi çoğaltma ayarlamak için kullanıldığında Start-AzSqlDatabaseCopy cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="9dfe3-109">Coğrafi çoğaltma bağlantı nesnesini birincili ikincil veritabanına döndürür.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="9dfe3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9dfe3-110">EXAMPLES</span></span>

### <span data-ttu-id="9dfe3-111">1: etkin Geo-Replication oluştur</span><span class="sxs-lookup"><span data-stu-id="9dfe3-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="9dfe3-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9dfe3-112">PARAMETERS</span></span>

### <span data-ttu-id="9dfe3-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="9dfe3-113">-AllowConnections</span></span>
<span data-ttu-id="9dfe3-114">İkincil Azure SQL veritabanının okuma amacını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="9dfe3-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9dfe3-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9dfe3-116">Olsun</span><span class="sxs-lookup"><span data-stu-id="9dfe3-116">No</span></span>
- <span data-ttu-id="9dfe3-117">Tüm</span><span class="sxs-lookup"><span data-stu-id="9dfe3-117">All</span></span>

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

### <span data-ttu-id="9dfe3-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="9dfe3-118">-AsJob</span></span>
<span data-ttu-id="9dfe3-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9dfe3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9dfe3-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9dfe3-120">-DatabaseName</span></span>
<span data-ttu-id="9dfe3-121">Birincil olarak davranacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="9dfe3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dfe3-122">-DefaultProfile</span></span>
<span data-ttu-id="9dfe3-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9dfe3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dfe3-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9dfe3-124">-LicenseType</span></span>
<span data-ttu-id="9dfe3-125">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="9dfe3-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dfe3-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="9dfe3-127">Bu cmdlet 'in ikincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="9dfe3-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="9dfe3-128">-PartnerServerName</span></span>
<span data-ttu-id="9dfe3-129">İkincil olarak davranacak Azure SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="9dfe3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dfe3-130">-ResourceGroupName</span></span>
<span data-ttu-id="9dfe3-131">Bu cmdlet 'in birincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="9dfe3-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="9dfe3-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="9dfe3-133">Azure SQL veritabanı ikincili için üretim oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="9dfe3-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9dfe3-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="9dfe3-135">İkincil veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="9dfe3-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9dfe3-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="9dfe3-137">İkincil veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="9dfe3-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="9dfe3-138">-SecondaryVCore</span></span>
<span data-ttu-id="9dfe3-139">Azure SQL veritabanı ikincil 'ın Vcore numaraları.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="9dfe3-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9dfe3-140">-ServerName</span></span>
<span data-ttu-id="9dfe3-141">Birincil SQL veritabanının SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="9dfe3-142">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="9dfe3-142">-Tags</span></span>
<span data-ttu-id="9dfe3-143">SQL veritabanı çoğaltma bağlantısıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="9dfe3-144">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="9dfe3-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9dfe3-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="9dfe3-145">-Confirm</span></span>
<span data-ttu-id="9dfe3-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dfe3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dfe3-147">-WhatIf</span></span>
<span data-ttu-id="9dfe3-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dfe3-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dfe3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dfe3-150">CommonParameters</span></span>
<span data-ttu-id="9dfe3-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dfe3-152">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9dfe3-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dfe3-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9dfe3-153">INPUTS</span></span>

### <span data-ttu-id="9dfe3-154">System. String</span><span class="sxs-lookup"><span data-stu-id="9dfe3-154">System.String</span></span>

## <span data-ttu-id="9dfe3-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9dfe3-155">OUTPUTS</span></span>

### <span data-ttu-id="9dfe3-156">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="9dfe3-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="9dfe3-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9dfe3-157">NOTES</span></span>

## <span data-ttu-id="9dfe3-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9dfe3-158">RELATED LINKS</span></span>

[<span data-ttu-id="9dfe3-159">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9dfe3-159">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="9dfe3-160">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9dfe3-160">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="9dfe3-161">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="9dfe3-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
