---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762190"
---
# <span data-ttu-id="a2f4d-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a2f4d-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="a2f4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2f4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2f4d-103">Var olan bir veritabanı için ikincil bir veritabanı oluşturur ve veri çoğaltması başlatır.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2f4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2f4d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2f4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2f4d-105">DESCRIPTION</span></span>
<span data-ttu-id="a2f4d-106">**Yeni-AzureRMSqlDatabaseSecondary** cmdlet 'i, bir veritabanında coğrafi çoğaltma ayarlamak için kullanıldığında Start-AzureSqlDatabaseCopy cmdlet 'ini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="a2f4d-107">Coğrafi çoğaltma bağlantı nesnesini birincili ikincil veritabanına döndürür.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="a2f4d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2f4d-108">EXAMPLES</span></span>

### <span data-ttu-id="a2f4d-109">1: etkin Geo-Replication oluştur</span><span class="sxs-lookup"><span data-stu-id="a2f4d-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="a2f4d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2f4d-110">PARAMETERS</span></span>

### <span data-ttu-id="a2f4d-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="a2f4d-111">-AllowConnections</span></span>
<span data-ttu-id="a2f4d-112">İkincil Azure SQL veritabanının okuma amacını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="a2f4d-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a2f4d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a2f4d-114">Olsun</span><span class="sxs-lookup"><span data-stu-id="a2f4d-114">No</span></span>
- <span data-ttu-id="a2f4d-115">Tüm</span><span class="sxs-lookup"><span data-stu-id="a2f4d-115">All</span></span>

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

### <span data-ttu-id="a2f4d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2f4d-116">-DatabaseName</span></span>
<span data-ttu-id="a2f4d-117">Birincil olarak davranacak veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="a2f4d-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f4d-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a2f4d-119">Bu cmdlet 'in ikincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="a2f4d-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="a2f4d-120">-PartnerServerName</span></span>
<span data-ttu-id="a2f4d-121">İkincil olarak davranacak Azure SQL veritabanı sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="a2f4d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2f4d-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2f4d-123">Bu cmdlet 'in birincil veritabanını atadığı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="a2f4d-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a2f4d-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="a2f4d-125">İkincil veritabanının yerleştirileceği elastik havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="a2f4d-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a2f4d-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="a2f4d-127">İkincil veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="a2f4d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a2f4d-128">-ServerName</span></span>
<span data-ttu-id="a2f4d-129">Birincil SQL veritabanının SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="a2f4d-130">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="a2f4d-130">-Tags</span></span>
<span data-ttu-id="a2f4d-131">SQL veritabanı çoğaltma bağlantısıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="a2f4d-132">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="a2f4d-132">For example:</span></span>

<span data-ttu-id="a2f4d-133">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="a2f4d-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a2f4d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2f4d-134">-Confirm</span></span>
<span data-ttu-id="a2f4d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2f4d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2f4d-136">-WhatIf</span></span>
<span data-ttu-id="a2f4d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2f4d-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2f4d-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2f4d-139">-DefaultProfile</span></span>
<span data-ttu-id="a2f4d-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2f4d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2f4d-141">CommonParameters</span></span>
<span data-ttu-id="a2f4d-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2f4d-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2f4d-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2f4d-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2f4d-144">INPUTS</span></span>

## <span data-ttu-id="a2f4d-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2f4d-145">OUTPUTS</span></span>

### <span data-ttu-id="a2f4d-146">Microsoft. Azure. Commands. Sql. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="a2f4d-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="a2f4d-147">Bu cmdlet, **Replicationlink** nesnelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a2f4d-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="a2f4d-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2f4d-148">NOTES</span></span>

## <span data-ttu-id="a2f4d-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2f4d-149">RELATED LINKS</span></span>

[<span data-ttu-id="a2f4d-150">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a2f4d-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="a2f4d-151">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a2f4d-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="a2f4d-152">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a2f4d-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
