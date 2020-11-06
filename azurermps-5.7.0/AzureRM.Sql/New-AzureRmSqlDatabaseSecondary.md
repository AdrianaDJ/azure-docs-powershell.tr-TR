---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: b23128d2ef55e971f20569e251601b410b218ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573162"
---
# <span data-ttu-id="78910-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="78910-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="78910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78910-102">SYNOPSIS</span></span>
<span data-ttu-id="78910-103">Var olan bir veritabanı için ikincil bir veritabanı oluşturur ve veri çoğaltması başlatır.</span><span class="sxs-lookup"><span data-stu-id="78910-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78910-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78910-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78910-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="78910-105">DESCRIPTION</span></span>
<span data-ttu-id="78910-106">**Yeni-AzureRMSqlDatabaseSecondary** cmdlet 'i, bir veritabanında coğrafi çoğaltma ayarlamak için kullanıldığında Start-AzureSqlDatabaseCopy cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="78910-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="78910-107">Coğrafi çoğaltma bağlantı nesnesini birincili ikincil veritabanına döndürür.</span><span class="sxs-lookup"><span data-stu-id="78910-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="78910-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78910-108">EXAMPLES</span></span>

### <span data-ttu-id="78910-109">1: etkin Geo-Replication oluştur</span><span class="sxs-lookup"><span data-stu-id="78910-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="78910-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78910-110">PARAMETERS</span></span>

### <span data-ttu-id="78910-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="78910-111">-AllowConnections</span></span>
<span data-ttu-id="78910-112">İkincil Azure SQL veritabanının okuma amacını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="78910-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="78910-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="78910-114">Olsun</span><span class="sxs-lookup"><span data-stu-id="78910-114">No</span></span>
- <span data-ttu-id="78910-115">Tüm</span><span class="sxs-lookup"><span data-stu-id="78910-115">All</span></span>

```yaml
Type: AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78910-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="78910-116">-AsJob</span></span>
<span data-ttu-id="78910-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="78910-117">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="78910-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78910-118">-DatabaseName</span></span>
<span data-ttu-id="78910-119">Birincil olarak davranacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-119">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78910-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78910-120">-DefaultProfile</span></span>
<span data-ttu-id="78910-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="78910-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78910-122">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78910-122">-PartnerResourceGroupName</span></span>
<span data-ttu-id="78910-123">Bu cmdlet 'in ikincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78910-124">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="78910-124">-PartnerServerName</span></span>
<span data-ttu-id="78910-125">İkincil olarak davranacak Azure SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-125">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78910-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78910-126">-ResourceGroupName</span></span>
<span data-ttu-id="78910-127">Bu cmdlet 'in birincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="78910-128">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="78910-128">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="78910-129">İkincil veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-129">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="78910-130">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="78910-130">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="78910-131">İkincil veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-131">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="78910-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78910-132">-ServerName</span></span>
<span data-ttu-id="78910-133">Birincil SQL veritabanının SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-133">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="78910-134">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="78910-134">-Tags</span></span>
<span data-ttu-id="78910-135">SQL veritabanı çoğaltma bağlantısıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="78910-135">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="78910-136">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="78910-136">For example:</span></span>

<span data-ttu-id="78910-137">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="78910-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="78910-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="78910-138">-Confirm</span></span>
<span data-ttu-id="78910-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="78910-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78910-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78910-140">-WhatIf</span></span>
<span data-ttu-id="78910-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="78910-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78910-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78910-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78910-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78910-143">CommonParameters</span></span>
<span data-ttu-id="78910-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78910-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78910-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78910-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78910-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78910-146">INPUTS</span></span>

### <span data-ttu-id="78910-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="78910-147">None</span></span>
<span data-ttu-id="78910-148">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="78910-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="78910-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78910-149">OUTPUTS</span></span>

### <span data-ttu-id="78910-150">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="78910-150">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="78910-151">Bu cmdlet, **Replicationlink** nesnelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="78910-151">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="78910-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78910-152">NOTES</span></span>

## <span data-ttu-id="78910-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78910-153">RELATED LINKS</span></span>

[<span data-ttu-id="78910-154">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="78910-154">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="78910-155">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="78910-155">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="78910-156">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="78910-156">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
