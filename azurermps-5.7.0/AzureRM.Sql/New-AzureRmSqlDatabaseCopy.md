---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573166"
---
# <span data-ttu-id="cc1ae-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="cc1ae-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="cc1ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1ae-103">Geçerli saatte anlık görüntüyü kullanan bir SQL veritabanının kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc1ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc1ae-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc1ae-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="cc1ae-106">**New-AzureRmSqlDatabaseCopy** cmdlet 'i, geçerli saatte verilerin anlık görüntüsünü kullanan BIR Azure SQL veritabanının kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="cc1ae-107">Tek seferlik veritabanı kopyası oluşturmak için Start-AzureSqlDatabaseCopy cmdlet 'i yerine bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="cc1ae-108">Bu cmdlet kopyanın **veritabanı** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="cc1ae-109">Not: veritabanında coğrafi çoğaltma yapılandırmak için New-AzureRmSqlDatabaseSecondary cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="cc1ae-110">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cc1ae-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc1ae-111">EXAMPLES</span></span>

## <span data-ttu-id="cc1ae-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc1ae-112">PARAMETERS</span></span>

### <span data-ttu-id="cc1ae-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="cc1ae-113">-AsJob</span></span>
<span data-ttu-id="cc1ae-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="cc1ae-114">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="cc1ae-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc1ae-115">-CopyDatabaseName</span></span>
<span data-ttu-id="cc1ae-116">SQL veritabanı kopyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-116">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="cc1ae-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1ae-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="cc1ae-118">Kopyanın atanacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="cc1ae-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="cc1ae-119">-CopyServerName</span></span>
<span data-ttu-id="cc1ae-120">Kopyayı barındıran SQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="cc1ae-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc1ae-121">-DatabaseName</span></span>
<span data-ttu-id="cc1ae-122">Kopyalanacak SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-122">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="cc1ae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1ae-123">-DefaultProfile</span></span>
<span data-ttu-id="cc1ae-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cc1ae-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc1ae-125">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="cc1ae-125">-ElasticPoolName</span></span>
<span data-ttu-id="cc1ae-126">Kopyanın atanacağı esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="cc1ae-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1ae-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc1ae-128">Kopyalanacak veritabanını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="cc1ae-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc1ae-129">-ServerName</span></span>
<span data-ttu-id="cc1ae-130">Kopyalanacak veritabanını içeren SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="cc1ae-131">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="cc1ae-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="cc1ae-132">Kopyaya atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-132">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="cc1ae-133">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="cc1ae-133">-Tags</span></span>
<span data-ttu-id="cc1ae-134">Azure SQL veritabanı kopyasıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="cc1ae-135">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="cc1ae-135">For example:</span></span>

<span data-ttu-id="cc1ae-136">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="cc1ae-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cc1ae-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc1ae-137">-Confirm</span></span>
<span data-ttu-id="cc1ae-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc1ae-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc1ae-139">-WhatIf</span></span>
<span data-ttu-id="cc1ae-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc1ae-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc1ae-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1ae-142">CommonParameters</span></span>
<span data-ttu-id="cc1ae-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1ae-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc1ae-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1ae-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc1ae-145">INPUTS</span></span>

### <span data-ttu-id="cc1ae-146">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cc1ae-146">None</span></span>
<span data-ttu-id="cc1ae-147">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cc1ae-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc1ae-148">OUTPUTS</span></span>

### <span data-ttu-id="cc1ae-149">Microsoft. Azure. Commands. Sql. Replication. model. Azurestabdatabasecopymodel</span><span class="sxs-lookup"><span data-stu-id="cc1ae-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="cc1ae-150">Bu cmdlet kopyalanan veritabanını temsil eden bir **veritabanı** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="cc1ae-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="cc1ae-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc1ae-151">NOTES</span></span>

## <span data-ttu-id="cc1ae-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc1ae-152">RELATED LINKS</span></span>

[<span data-ttu-id="cc1ae-153">Yeni-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="cc1ae-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="cc1ae-154">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="cc1ae-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
