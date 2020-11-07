---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 2E4F5C27-C50F-4133-B193-BC477BCD6778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabase.md
ms.openlocfilehash: 3d36c94ebcc1b733559f9fb4075fb20e4ec67144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762677"
---
# <span data-ttu-id="89998-101">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89998-101">Set-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="89998-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89998-102">SYNOPSIS</span></span>
<span data-ttu-id="89998-103">Veritabanının özelliklerini ayarlar veya varolan bir veritabanını esnek bir havuza taşıma.</span><span class="sxs-lookup"><span data-stu-id="89998-103">Sets properties for a database, or moves an existing database into an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89998-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="89998-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabase [-DatabaseName] <String> [-MaxSizeBytes <Int64>] [-Edition <DatabaseEdition>]
 [-RequestedServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ReadScale <DatabaseReadScale>]
 [-Tags <Hashtable>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89998-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="89998-105">DESCRIPTION</span></span>
<span data-ttu-id="89998-106">**Set-AzureRmSqlDatabase** cmdlet 'ı BIR Azure SQL veritabanının özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="89998-106">The **Set-AzureRmSqlDatabase** cmdlet sets properties for an Azure SQL database.</span></span>
<span data-ttu-id="89998-107">Ayrıca, bir veritabanını esnek bir havuza taşımak için *ela, PoolName* parametresini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89998-107">In addition, you can specify the *ElasticPoolName* parameter to move a database into an elastic pool.</span></span>
<span data-ttu-id="89998-108">Bir veritabanı zaten esnek bir havuzda yer alıyorsa, bir performans düzeyi atamak için *Requestedserviceobjectivename* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89998-108">If a database is already in an elastic pool, you can use the *RequestedServiceObjectiveName* parameter to assign a performance level.</span></span>

## <span data-ttu-id="89998-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="89998-109">EXAMPLES</span></span>

### <span data-ttu-id="89998-110">Örnek 1: veritabanını Standart S2 veritabanına güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="89998-110">Example 1: Update a database to a Standard S2 database</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -Edition "Standard" -RequestedServiceObjectiveName "S2"
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
CurrentServiceObjectiveId     : 455330e1-00cd-488b-b5fa-177c226f28b7
CurrentServiceObjectiveName   : S2
RequestedServiceObjectiveId   : 455330e1-00cd-488b-b5fa-177c226f28b7
RequestedServiceObjectiveName :
ElasticPoolName               :
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="89998-111">Bu komut Database01 adındaki bir veritabanını server01 adlı sunucudaki standart bir S2 veritabanına güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="89998-111">This command updates a database named Database01 to a Standard S2 database on a server named Server01.</span></span>

### <span data-ttu-id="89998-112">Örnek 2: esnek bir havuza veritabanı ekleme</span><span class="sxs-lookup"><span data-stu-id="89998-112">Example 2: Add a database to an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -DatabaseName "Database01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
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
CurrentServiceObjectiveId     : d1737d22-a8ea-4de7-9bd0-33395d2a7419
CurrentServiceObjectiveName   : ElasticPool
RequestedServiceObjectiveId   : d1737d22-a8ea-4de7-9bd0-33395d2a7419
RequestedServiceObjectiveName :
ElasticPoolName               : elasticpool01
EarliestRestoreDate           :
Tags                          :
```

<span data-ttu-id="89998-113">Bu komut, server01 adlı sunucuda barındırılan ElasticPool01 adındaki esnek havuzuna Database01 adlı bir veritabanı ekler.</span><span class="sxs-lookup"><span data-stu-id="89998-113">This command adds a database named Database01 to the elastic pool named ElasticPool01 hosted on the server named Server01.</span></span>

## <span data-ttu-id="89998-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="89998-114">PARAMETERS</span></span>

### <span data-ttu-id="89998-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="89998-115">-DatabaseName</span></span>
<span data-ttu-id="89998-116">Veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89998-116">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89998-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="89998-117">-Edition</span></span>
<span data-ttu-id="89998-118">Veritabanının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="89998-118">Specifies the edition for the database.</span></span>
<span data-ttu-id="89998-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="89998-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="89998-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="89998-120">None</span></span>
- <span data-ttu-id="89998-121">Min</span><span class="sxs-lookup"><span data-stu-id="89998-121">Premium</span></span>
- <span data-ttu-id="89998-122">Ana</span><span class="sxs-lookup"><span data-stu-id="89998-122">Basic</span></span>
- <span data-ttu-id="89998-123">Ardından</span><span class="sxs-lookup"><span data-stu-id="89998-123">Standard</span></span>
- <span data-ttu-id="89998-124">Ambarı</span><span class="sxs-lookup"><span data-stu-id="89998-124">DataWarehouse</span></span>
- <span data-ttu-id="89998-125">Bırakılamıyor</span><span class="sxs-lookup"><span data-stu-id="89998-125">Free</span></span>

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

### <span data-ttu-id="89998-126">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="89998-126">-ElasticPoolName</span></span>
<span data-ttu-id="89998-127">Veritabanının taşınacağı esnek havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89998-127">Specifies name of the elastic pool in which to move the database.</span></span>

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

### <span data-ttu-id="89998-128">-MaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="89998-128">-MaxSizeBytes</span></span>
<span data-ttu-id="89998-129">En yüksek veritabanı boyutunu bayt olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="89998-129">Specifies the new maximum size for the database in bytes.</span></span>
<span data-ttu-id="89998-130">Bu parametreyi veya *Maxsizegb* 'yi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="89998-130">You can specify either this parameter or *MaxSizeGB*.</span></span>
<span data-ttu-id="89998-131">Sürüm başına kabul edilebilir değerler için *Maxsizegb* parametresine bakın.</span><span class="sxs-lookup"><span data-stu-id="89998-131">See the *MaxSizeGB* parameter for acceptable values per edition.</span></span>

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

### <span data-ttu-id="89998-132">-ReadScale</span><span class="sxs-lookup"><span data-stu-id="89998-132">-ReadScale</span></span>
<span data-ttu-id="89998-133">Azure SQL veritabanına atanacak ölçeği oku seçeneği. (Etkin/devre dışı)</span><span class="sxs-lookup"><span data-stu-id="89998-133">The read scale option to assign to the Azure SQL Database.(Enabled/Disabled)</span></span>

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

### <span data-ttu-id="89998-134">-RequestedServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="89998-134">-RequestedServiceObjectiveName</span></span>
<span data-ttu-id="89998-135">Veritabanına atanacak hizmet amacın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89998-135">Specifies the name of the service objective to assign to the database.</span></span> <span data-ttu-id="89998-136">Hizmet amaçları hakkında bilgi için, Microsoft Geliştirici ağ kitaplığındaki [Azure SQL veritabanı hizmet katmanları ve performans düzeyleri](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="89998-136">For information about service objectives, see [Azure SQL Database Service Tiers and Performance Levels](https://msdn.microsoft.com/en-us/library/azure/dn741336.aspx) in the Microsoft Developer Network Library.</span></span>

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

### <span data-ttu-id="89998-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89998-137">-ResourceGroupName</span></span>
<span data-ttu-id="89998-138">Sunucunun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89998-138">Specifies the name of resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="89998-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="89998-139">-ServerName</span></span>
<span data-ttu-id="89998-140">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="89998-140">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="89998-141">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="89998-141">-Tags</span></span>
<span data-ttu-id="89998-142">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="89998-142">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="89998-143">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="89998-143">For example:</span></span>

<span data-ttu-id="89998-144">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="89998-144">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="89998-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="89998-145">-Confirm</span></span>
<span data-ttu-id="89998-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="89998-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89998-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89998-147">-WhatIf</span></span>
<span data-ttu-id="89998-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="89998-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89998-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="89998-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89998-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89998-150">-DefaultProfile</span></span>
<span data-ttu-id="89998-151">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="89998-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89998-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89998-152">CommonParameters</span></span>
<span data-ttu-id="89998-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="89998-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89998-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89998-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89998-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="89998-155">INPUTS</span></span>

## <span data-ttu-id="89998-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="89998-156">OUTPUTS</span></span>

### <span data-ttu-id="89998-157">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="89998-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="89998-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="89998-158">NOTES</span></span>

## <span data-ttu-id="89998-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="89998-159">RELATED LINKS</span></span>

[<span data-ttu-id="89998-160">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89998-160">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="89998-161">Yeni-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89998-161">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="89998-162">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89998-162">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="89998-163">Özgeçmiş-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89998-163">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="89998-164">Askıya al-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="89998-164">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="89998-165">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="89998-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
