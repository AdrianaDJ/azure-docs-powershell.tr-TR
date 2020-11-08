---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096350"
---
# <span data-ttu-id="4a2d8-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="4a2d8-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="4a2d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a2d8-102">SYNOPSIS</span></span>
<span data-ttu-id="4a2d8-103">Elastik bir havuzda ve özellik değerleriyle elastik veritabanları alır.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="4a2d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a2d8-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a2d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a2d8-105">DESCRIPTION</span></span>
<span data-ttu-id="4a2d8-106">**Get-Azsqlela, Pooldatabase** cmdlet 'i, elastik havuzda elastik veritabanları ve özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="4a2d8-107">Yalnızca bu veritabanının özellik değerlerini görmek için Azure SQL veritabanında elastik veritabanının adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="4a2d8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a2d8-108">EXAMPLES</span></span>

### <span data-ttu-id="4a2d8-109">Örnek 1: esnek havuzdaki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="4a2d8-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="4a2d8-110">Bu komut, ElasticPool01 adlı bir elastik havuzda tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="4a2d8-111">Örnek 2: filtreleme kullanarak elastik havuzda tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="4a2d8-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="4a2d8-112">Bu komut, ElasticPool01 adlı bir elastik havuzda "veritabanı" ile başlayan tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="4a2d8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a2d8-113">PARAMETERS</span></span>

### <span data-ttu-id="4a2d8-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4a2d8-114">-DatabaseName</span></span>
<span data-ttu-id="4a2d8-115">Bu cmdlet 'in aldığı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a2d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a2d8-116">-DefaultProfile</span></span>
<span data-ttu-id="4a2d8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4a2d8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a2d8-118">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="4a2d8-118">-ElasticPoolName</span></span>
<span data-ttu-id="4a2d8-119">Esnek bir havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="4a2d8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a2d8-120">-ResourceGroupName</span></span>
<span data-ttu-id="4a2d8-121">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="4a2d8-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4a2d8-122">-ServerName</span></span>
<span data-ttu-id="4a2d8-123">Elastik havuz içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="4a2d8-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a2d8-124">-Confirm</span></span>
<span data-ttu-id="4a2d8-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a2d8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a2d8-126">-WhatIf</span></span>
<span data-ttu-id="4a2d8-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a2d8-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a2d8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a2d8-129">CommonParameters</span></span>
<span data-ttu-id="4a2d8-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a2d8-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4a2d8-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a2d8-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a2d8-132">INPUTS</span></span>

### <span data-ttu-id="4a2d8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4a2d8-133">System.String</span></span>

## <span data-ttu-id="4a2d8-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a2d8-134">OUTPUTS</span></span>

### <span data-ttu-id="4a2d8-135">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="4a2d8-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4a2d8-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a2d8-136">NOTES</span></span>

## <span data-ttu-id="4a2d8-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a2d8-137">RELATED LINKS</span></span>

[<span data-ttu-id="4a2d8-138">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="4a2d8-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="4a2d8-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="4a2d8-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="4a2d8-140">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="4a2d8-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="4a2d8-141">Remove-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="4a2d8-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="4a2d8-142">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="4a2d8-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)
