---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096231"
---
# <span data-ttu-id="c6114-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="c6114-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="c6114-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6114-102">SYNOPSIS</span></span>
<span data-ttu-id="c6114-103">Esnek bir havuzun yerine çalışma.</span><span class="sxs-lookup"><span data-stu-id="c6114-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="c6114-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6114-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6114-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6114-105">DESCRIPTION</span></span>
<span data-ttu-id="c6114-106">Invoke-AzSqlElasticPoolFailover cmdlet 'i esnek bir havuzda kullanın.</span><span class="sxs-lookup"><span data-stu-id="c6114-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="c6114-107">Bu cmdlet çalıştırıldıktan sonra, esnek havuzundaki tüm veritabanlarında yük devretme gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="c6114-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="c6114-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6114-108">EXAMPLES</span></span>

### <span data-ttu-id="c6114-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c6114-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="c6114-110">Bu komut, "Server01" adlı sunucudaki "ElasticPool01" adlı esnek havuzun yerine çalışır.</span><span class="sxs-lookup"><span data-stu-id="c6114-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="c6114-111">Bu, yerine çalışma, "ElasticPool01" adlı elastik havuzdaki tüm veritabanlarında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="c6114-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="c6114-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6114-112">PARAMETERS</span></span>

### <span data-ttu-id="c6114-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="c6114-113">-AsJob</span></span>
<span data-ttu-id="c6114-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c6114-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6114-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6114-115">-DefaultProfile</span></span>
<span data-ttu-id="c6114-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6114-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6114-117">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="c6114-117">-ElasticPoolName</span></span>
<span data-ttu-id="c6114-118">Kaldırılacak Azure SQL esnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="c6114-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="c6114-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c6114-119">-Force</span></span>
<span data-ttu-id="c6114-120">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="c6114-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c6114-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c6114-121">-PassThru</span></span>
<span data-ttu-id="c6114-122">Başarılı bir yürütmede, doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="c6114-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="c6114-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c6114-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6114-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6114-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6114-125">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c6114-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="c6114-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6114-126">-ServerName</span></span>
<span data-ttu-id="c6114-127">Elastik havuzun bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="c6114-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="c6114-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6114-128">-Confirm</span></span>
<span data-ttu-id="c6114-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6114-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6114-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6114-130">-WhatIf</span></span>
<span data-ttu-id="c6114-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6114-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6114-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6114-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6114-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6114-133">CommonParameters</span></span>
<span data-ttu-id="c6114-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6114-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6114-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c6114-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6114-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6114-136">INPUTS</span></span>

### <span data-ttu-id="c6114-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c6114-137">System.String</span></span>

## <span data-ttu-id="c6114-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6114-138">OUTPUTS</span></span>

## <span data-ttu-id="c6114-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6114-139">NOTES</span></span>

## <span data-ttu-id="c6114-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6114-140">RELATED LINKS</span></span>

[<span data-ttu-id="c6114-141">Get-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="c6114-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="c6114-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c6114-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="c6114-143">Get-Azsqlelaunpooldatabase</span><span class="sxs-lookup"><span data-stu-id="c6114-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="c6114-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="c6114-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="c6114-145">New-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="c6114-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="c6114-146">Remove-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="c6114-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="c6114-147">Set-Azkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="c6114-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="c6114-148">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c6114-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)