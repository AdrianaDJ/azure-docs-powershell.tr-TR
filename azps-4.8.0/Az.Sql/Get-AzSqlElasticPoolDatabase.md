---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolDatabase.md
ms.openlocfilehash: 2e24dc80b93d72722d05a7dced05cbea02751a05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108682"
---
# <span data-ttu-id="f6fe3-101">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="f6fe3-101">Get-AzSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="f6fe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fe3-103">Elastik bir havuzda ve özellik değerleriyle elastik veritabanları alır.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-103">Gets elastic databases in an elastic pool and their property values.</span></span>

## <span data-ttu-id="f6fe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6fe3-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6fe3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6fe3-105">DESCRIPTION</span></span>
<span data-ttu-id="f6fe3-106">**Get-Azsqlela, Pooldatabase** cmdlet 'i, elastik havuzda elastik veritabanları ve özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-106">The **Get-AzSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="f6fe3-107">Yalnızca bu veritabanının özellik değerlerini görmek için Azure SQL veritabanında elastik veritabanının adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="f6fe3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6fe3-108">EXAMPLES</span></span>

### <span data-ttu-id="f6fe3-109">Örnek 1: esnek havuzdaki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="f6fe3-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="f6fe3-110">Bu komut, ElasticPool01 adlı bir elastik havuzda tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="f6fe3-111">Örnek 2: filtreleme kullanarak elastik havuzda tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="f6fe3-111">Example 2: Get all databases in an elastic pool using filtering</span></span>
```
PS C:\> Get-AzSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -DatabaseName "Database*"
```

<span data-ttu-id="f6fe3-112">Bu komut, ElasticPool01 adlı bir elastik havuzda "veritabanı" ile başlayan tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-112">This command gets all databases in an elastic pool named ElasticPool01 that start with "Database".</span></span>

## <span data-ttu-id="f6fe3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6fe3-113">PARAMETERS</span></span>

### <span data-ttu-id="f6fe3-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6fe3-114">-DatabaseName</span></span>
<span data-ttu-id="f6fe3-115">Bu cmdlet 'in aldığı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-115">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f6fe3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fe3-116">-DefaultProfile</span></span>
<span data-ttu-id="f6fe3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f6fe3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6fe3-118">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="f6fe3-118">-ElasticPoolName</span></span>
<span data-ttu-id="f6fe3-119">Esnek bir havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-119">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="f6fe3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6fe3-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6fe3-121">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-121">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="f6fe3-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6fe3-122">-ServerName</span></span>
<span data-ttu-id="f6fe3-123">Elastik havuz içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-123">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="f6fe3-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="f6fe3-124">-Confirm</span></span>
<span data-ttu-id="f6fe3-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6fe3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6fe3-126">-WhatIf</span></span>
<span data-ttu-id="f6fe3-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6fe3-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6fe3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fe3-129">CommonParameters</span></span>
<span data-ttu-id="f6fe3-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fe3-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f6fe3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fe3-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6fe3-132">INPUTS</span></span>

### <span data-ttu-id="f6fe3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f6fe3-133">System.String</span></span>

## <span data-ttu-id="f6fe3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6fe3-134">OUTPUTS</span></span>

### <span data-ttu-id="f6fe3-135">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="f6fe3-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f6fe3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6fe3-136">NOTES</span></span>

## <span data-ttu-id="f6fe3-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6fe3-137">RELATED LINKS</span></span>

[<span data-ttu-id="f6fe3-138">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="f6fe3-138">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="f6fe3-139">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="f6fe3-139">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="f6fe3-140">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="f6fe3-140">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="f6fe3-141">Remove-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="f6fe3-141">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="f6fe3-142">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="f6fe3-142">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

