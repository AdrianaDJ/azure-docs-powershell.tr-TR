---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: a9f86b9b316c14e40505932e0bf3b30fc66c55c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592709"
---
# <span data-ttu-id="a7c29-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="a7c29-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="a7c29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7c29-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c29-103">Elastik bir havuzda ve özellik değerleriyle elastik veritabanları alır.</span><span class="sxs-lookup"><span data-stu-id="a7c29-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7c29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7c29-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7c29-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7c29-105">DESCRIPTION</span></span>
<span data-ttu-id="a7c29-106">**Get-Azurermsqlelaraz Pooldatabase** cmdlet 'i elastik havuzda elastik veritabanları ve özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="a7c29-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="a7c29-107">Yalnızca bu veritabanının özellik değerlerini görmek için Azure SQL veritabanında elastik veritabanının adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7c29-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="a7c29-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7c29-108">EXAMPLES</span></span>

### <span data-ttu-id="a7c29-109">Örnek 1: esnek havuzdaki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="a7c29-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="a7c29-110">Bu komut, ElasticPool01 adlı bir elastik havuzda tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="a7c29-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="a7c29-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7c29-111">PARAMETERS</span></span>

### <span data-ttu-id="a7c29-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7c29-112">-DatabaseName</span></span>
<span data-ttu-id="a7c29-113">Bu cmdlet 'in aldığı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7c29-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a7c29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c29-114">-DefaultProfile</span></span>
<span data-ttu-id="a7c29-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a7c29-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7c29-116">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="a7c29-116">-ElasticPoolName</span></span>
<span data-ttu-id="a7c29-117">Esnek bir havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7c29-117">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="a7c29-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c29-118">-ResourceGroupName</span></span>
<span data-ttu-id="a7c29-119">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7c29-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="a7c29-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a7c29-120">-ServerName</span></span>
<span data-ttu-id="a7c29-121">Elastik havuz içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7c29-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="a7c29-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7c29-122">-Confirm</span></span>
<span data-ttu-id="a7c29-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7c29-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c29-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c29-124">-WhatIf</span></span>
<span data-ttu-id="a7c29-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7c29-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7c29-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7c29-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c29-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c29-127">CommonParameters</span></span>
<span data-ttu-id="a7c29-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7c29-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c29-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7c29-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c29-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7c29-130">INPUTS</span></span>

### <span data-ttu-id="a7c29-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a7c29-131">System.String</span></span>

## <span data-ttu-id="a7c29-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7c29-132">OUTPUTS</span></span>

### <span data-ttu-id="a7c29-133">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="a7c29-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a7c29-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7c29-134">NOTES</span></span>

## <span data-ttu-id="a7c29-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7c29-135">RELATED LINKS</span></span>

[<span data-ttu-id="a7c29-136">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a7c29-136">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a7c29-137">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a7c29-137">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="a7c29-138">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a7c29-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a7c29-139">Remove-Azurermsqlelaunpool</span><span class="sxs-lookup"><span data-stu-id="a7c29-139">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a7c29-140">Set-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="a7c29-140">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

