---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d2af2095198cf0a1102e3422716013f2f2e02fc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589308"
---
# <span data-ttu-id="b7ac1-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7ac1-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b7ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ac1-103">Var olan bir veritabanı için ikincil bir veritabanı oluşturur ve veri çoğaltması başlatır.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7ac1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7ac1-104">SYNTAX</span></span>

### <span data-ttu-id="b7ac1-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7ac1-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7ac1-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="b7ac1-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7ac1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7ac1-107">DESCRIPTION</span></span>
<span data-ttu-id="b7ac1-108">**Yeni-AzureRMSqlDatabaseSecondary** cmdlet 'i, bir veritabanında coğrafi çoğaltma ayarlamak için kullanıldığında Start-AzureSqlDatabaseCopy cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-108">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="b7ac1-109">Coğrafi çoğaltma bağlantı nesnesini birincili ikincil veritabanına döndürür.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="b7ac1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7ac1-110">EXAMPLES</span></span>

### <span data-ttu-id="b7ac1-111">1: etkin Geo-Replication oluştur</span><span class="sxs-lookup"><span data-stu-id="b7ac1-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="b7ac1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7ac1-112">PARAMETERS</span></span>

### <span data-ttu-id="b7ac1-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="b7ac1-113">-AllowConnections</span></span>
<span data-ttu-id="b7ac1-114">İkincil Azure SQL veritabanının okuma amacını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="b7ac1-115">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b7ac1-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7ac1-116">Olsun</span><span class="sxs-lookup"><span data-stu-id="b7ac1-116">No</span></span>
- <span data-ttu-id="b7ac1-117">Tüm</span><span class="sxs-lookup"><span data-stu-id="b7ac1-117">All</span></span>

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

### <span data-ttu-id="b7ac1-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="b7ac1-118">-AsJob</span></span>
<span data-ttu-id="b7ac1-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b7ac1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7ac1-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7ac1-120">-DatabaseName</span></span>
<span data-ttu-id="b7ac1-121">Birincil olarak davranacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="b7ac1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ac1-122">-DefaultProfile</span></span>
<span data-ttu-id="b7ac1-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b7ac1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7ac1-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b7ac1-124">-LicenseType</span></span>
<span data-ttu-id="b7ac1-125">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="b7ac1-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ac1-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b7ac1-127">Bu cmdlet 'in ikincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="b7ac1-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="b7ac1-128">-PartnerServerName</span></span>
<span data-ttu-id="b7ac1-129">İkincil olarak davranacak Azure SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="b7ac1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ac1-130">-ResourceGroupName</span></span>
<span data-ttu-id="b7ac1-131">Bu cmdlet 'in birincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="b7ac1-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b7ac1-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="b7ac1-133">Azure SQL veritabanı ikincili için üretim oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="b7ac1-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b7ac1-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="b7ac1-135">İkincil veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="b7ac1-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b7ac1-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="b7ac1-137">İkincil veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="b7ac1-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="b7ac1-138">-SecondaryVCore</span></span>
<span data-ttu-id="b7ac1-139">Azure SQL veritabanı ikincil 'ın Vcore numaraları.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="b7ac1-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7ac1-140">-ServerName</span></span>
<span data-ttu-id="b7ac1-141">Birincil SQL veritabanının SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="b7ac1-142">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="b7ac1-142">-Tags</span></span>
<span data-ttu-id="b7ac1-143">SQL veritabanı çoğaltma bağlantısıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="b7ac1-144">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="b7ac1-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b7ac1-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7ac1-145">-Confirm</span></span>
<span data-ttu-id="b7ac1-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ac1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ac1-147">-WhatIf</span></span>
<span data-ttu-id="b7ac1-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7ac1-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ac1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ac1-150">CommonParameters</span></span>
<span data-ttu-id="b7ac1-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7ac1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ac1-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7ac1-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ac1-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7ac1-153">INPUTS</span></span>

### <span data-ttu-id="b7ac1-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ac1-154">System.String</span></span>

## <span data-ttu-id="b7ac1-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7ac1-155">OUTPUTS</span></span>

### <span data-ttu-id="b7ac1-156">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b7ac1-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="b7ac1-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7ac1-157">NOTES</span></span>

## <span data-ttu-id="b7ac1-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7ac1-158">RELATED LINKS</span></span>

[<span data-ttu-id="b7ac1-159">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7ac1-159">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b7ac1-160">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b7ac1-160">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b7ac1-161">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="b7ac1-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
