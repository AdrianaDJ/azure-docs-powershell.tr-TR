---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764757"
---
# <span data-ttu-id="724aa-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="724aa-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="724aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="724aa-102">SYNOPSIS</span></span>
<span data-ttu-id="724aa-103">Geçerli saatte anlık görüntüyü kullanan bir SQL veritabanının kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="724aa-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="724aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="724aa-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="724aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="724aa-105">DESCRIPTION</span></span>
<span data-ttu-id="724aa-106">**New-AzureRmSqlDatabaseCopy** cmdlet 'i, geçerli saatte verilerin anlık görüntüsünü kullanan BIR Azure SQL veritabanının kopyasını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="724aa-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="724aa-107">Tek seferlik veritabanı kopyası oluşturmak için Start-AzureSqlDatabaseCopy cmdlet 'i yerine bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="724aa-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="724aa-108">Bu cmdlet kopyanın **veritabanı** nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="724aa-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="724aa-109">Not: veritabanında coğrafi çoğaltma yapılandırmak için New-AzureRmSqlDatabaseSecondary cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="724aa-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="724aa-110">Bu cmdlet, Azure 'da SQL Server genişletme veritabanı hizmeti tarafından da desteklenir.</span><span class="sxs-lookup"><span data-stu-id="724aa-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="724aa-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="724aa-111">EXAMPLES</span></span>

## <span data-ttu-id="724aa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="724aa-112">PARAMETERS</span></span>

### <span data-ttu-id="724aa-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="724aa-113">-CopyDatabaseName</span></span>
<span data-ttu-id="724aa-114">SQL veritabanı kopyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-114">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="724aa-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="724aa-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="724aa-116">Kopyanın atanacağı Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="724aa-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="724aa-117">-CopyServerName</span></span>
<span data-ttu-id="724aa-118">Kopyayı barındıran SQL sunucusunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="724aa-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="724aa-119">-DatabaseName</span></span>
<span data-ttu-id="724aa-120">Kopyalanacak SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="724aa-121">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="724aa-121">-ElasticPoolName</span></span>
<span data-ttu-id="724aa-122">Kopyanın atanacağı esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="724aa-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="724aa-123">-ResourceGroupName</span></span>
<span data-ttu-id="724aa-124">Bu cmdlet 'in kopyalanan veritabanını atadığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="724aa-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="724aa-125">-ServerName</span></span>
<span data-ttu-id="724aa-126">Kopyalanacak veritabanını içeren SQL Server 'ın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="724aa-127">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="724aa-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="724aa-128">Kopyaya atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-128">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="724aa-129">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="724aa-129">-Tags</span></span>
<span data-ttu-id="724aa-130">Azure SQL veritabanı kopyasıyla ilişkilendirilecek karma tablo biçimindeki anahtar değer çiftlerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="724aa-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="724aa-131">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="724aa-131">For example:</span></span>

<span data-ttu-id="724aa-132">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="724aa-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="724aa-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="724aa-133">-Confirm</span></span>
<span data-ttu-id="724aa-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="724aa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="724aa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="724aa-135">-WhatIf</span></span>
<span data-ttu-id="724aa-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="724aa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="724aa-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="724aa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="724aa-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="724aa-138">-DefaultProfile</span></span>
<span data-ttu-id="724aa-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="724aa-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="724aa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="724aa-140">CommonParameters</span></span>
<span data-ttu-id="724aa-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="724aa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="724aa-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="724aa-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="724aa-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="724aa-143">INPUTS</span></span>

## <span data-ttu-id="724aa-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="724aa-144">OUTPUTS</span></span>

### <span data-ttu-id="724aa-145">Microsoft. Azure. Commands. Sql. Replication. model. Azurestabdatabasecopymodel</span><span class="sxs-lookup"><span data-stu-id="724aa-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="724aa-146">Bu cmdlet kopyalanan veritabanını temsil eden bir **veritabanı** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="724aa-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="724aa-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="724aa-147">NOTES</span></span>

## <span data-ttu-id="724aa-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="724aa-148">RELATED LINKS</span></span>

[<span data-ttu-id="724aa-149">Yeni-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="724aa-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="724aa-150">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="724aa-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
