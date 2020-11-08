---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
ms.openlocfilehash: e4cfdb8cd7ffc99c3beed66de427af458538bab8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096229"
---
# <span data-ttu-id="9efad-101">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="9efad-101">New-AzSqlDatabaseCopy</span></span>

## <span data-ttu-id="9efad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9efad-102">SYNOPSIS</span></span>
<span data-ttu-id="9efad-103">Geçerli saatte anlık görüntüyü kullanan bir SQL veritabanının kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9efad-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

## <span data-ttu-id="9efad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9efad-104">SYNTAX</span></span>

### <span data-ttu-id="9efad-105">Vseçvet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9efad-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>] -CopyDatabaseName <String>
 [-AsJob] [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9efad-106">Vcorebasevseçdatabase</span><span class="sxs-lookup"><span data-stu-id="9efad-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9efad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9efad-107">DESCRIPTION</span></span>
<span data-ttu-id="9efad-108">**New-AzSqlDatabaseCopy** cmdlet 'i, geçerli zamanda verilerin anlık görüntüsünü kullanan BIR Azure SQL veritabanının kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9efad-108">The **New-AzSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="9efad-109">Tek seferlik veritabanı kopyası oluşturmak için Start-AzSqlDatabaseCopy cmdlet 'i yerine bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="9efad-109">Use this cmdlet instead of the Start-AzSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="9efad-110">Bu cmdlet kopyanın **veritabanı** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9efad-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="9efad-111">Not: veritabanında coğrafi çoğaltma yapılandırmak için New-AzSqlDatabaseSecondary cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9efad-111">Note: Use the New-AzSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="9efad-112">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="9efad-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9efad-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9efad-113">EXAMPLES</span></span>

## <span data-ttu-id="9efad-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9efad-114">PARAMETERS</span></span>

### <span data-ttu-id="9efad-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="9efad-115">-AsJob</span></span>
<span data-ttu-id="9efad-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9efad-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9efad-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="9efad-117">-ComputeGeneration</span></span>
<span data-ttu-id="9efad-118">Yeni kopyaya atanacak hesaplama üretimi.</span><span class="sxs-lookup"><span data-stu-id="9efad-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="9efad-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="9efad-119">-CopyDatabaseName</span></span>
<span data-ttu-id="9efad-120">SQL veritabanı kopyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="9efad-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9efad-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="9efad-122">Kopyanın atanacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="9efad-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="9efad-123">-CopyServerName</span></span>
<span data-ttu-id="9efad-124">Kopyayı barındıran SQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="9efad-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9efad-125">-DatabaseName</span></span>
<span data-ttu-id="9efad-126">Kopyalanacak SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="9efad-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9efad-127">-DefaultProfile</span></span>
<span data-ttu-id="9efad-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9efad-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9efad-129">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="9efad-129">-ElasticPoolName</span></span>
<span data-ttu-id="9efad-130">Kopyanın atanacağı esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="9efad-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9efad-131">-LicenseType</span></span>
<span data-ttu-id="9efad-132">Azure SQL veritabanı için lisans türü.</span><span class="sxs-lookup"><span data-stu-id="9efad-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="9efad-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9efad-133">-ResourceGroupName</span></span>
<span data-ttu-id="9efad-134">Kopyalanacak veritabanını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="9efad-135">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9efad-135">-ServerName</span></span>
<span data-ttu-id="9efad-136">Kopyalanacak veritabanını içeren SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="9efad-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9efad-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="9efad-138">Kopyaya atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="9efad-139">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="9efad-139">-Tags</span></span>
<span data-ttu-id="9efad-140">Azure SQL veritabanı kopyasıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9efad-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="9efad-141">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="9efad-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9efad-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="9efad-142">-VCore</span></span>
<span data-ttu-id="9efad-143">Azure SQL veritabanı kopyasının Vcore numaraları.</span><span class="sxs-lookup"><span data-stu-id="9efad-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="9efad-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="9efad-144">-Confirm</span></span>
<span data-ttu-id="9efad-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9efad-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9efad-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9efad-146">-WhatIf</span></span>
<span data-ttu-id="9efad-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9efad-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9efad-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9efad-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9efad-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9efad-149">CommonParameters</span></span>
<span data-ttu-id="9efad-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9efad-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9efad-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9efad-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9efad-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9efad-152">INPUTS</span></span>

### <span data-ttu-id="9efad-153">System. String</span><span class="sxs-lookup"><span data-stu-id="9efad-153">System.String</span></span>

## <span data-ttu-id="9efad-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9efad-154">OUTPUTS</span></span>

### <span data-ttu-id="9efad-155">Microsoft. Azure. Commands. Sql. Replication. model. Azurestabdatabasecopymodel</span><span class="sxs-lookup"><span data-stu-id="9efad-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="9efad-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9efad-156">NOTES</span></span>

## <span data-ttu-id="9efad-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9efad-157">RELATED LINKS</span></span>

[<span data-ttu-id="9efad-158">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="9efad-158">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="9efad-159">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="9efad-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)