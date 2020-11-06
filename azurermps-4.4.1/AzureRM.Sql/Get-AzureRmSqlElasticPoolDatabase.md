---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: f2229fa904144b0dd95a054da95db99600963406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589043"
---
# <span data-ttu-id="38eaf-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="38eaf-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="38eaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="38eaf-103">Elastik bir havuzda ve özellik değerleriyle elastik veritabanları alır.</span><span class="sxs-lookup"><span data-stu-id="38eaf-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38eaf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38eaf-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38eaf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="38eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="38eaf-106">**Get-Azurermsqlelaraz Pooldatabase** cmdlet 'i elastik havuzda elastik veritabanları ve özellik değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="38eaf-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="38eaf-107">Yalnızca bu veritabanının özellik değerlerini görmek için Azure SQL veritabanında elastik veritabanının adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="38eaf-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="38eaf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38eaf-108">EXAMPLES</span></span>

### <span data-ttu-id="38eaf-109">Örnek 1: esnek havuzdaki tüm veritabanlarını alma</span><span class="sxs-lookup"><span data-stu-id="38eaf-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="38eaf-110">Bu komut, ElasticPool01 adlı bir elastik havuzda tüm veritabanlarını alır.</span><span class="sxs-lookup"><span data-stu-id="38eaf-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="38eaf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38eaf-111">PARAMETERS</span></span>

### <span data-ttu-id="38eaf-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="38eaf-112">-DatabaseName</span></span>
<span data-ttu-id="38eaf-113">Bu cmdlet 'in aldığı SQL veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38eaf-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38eaf-114">-Elana PoolName</span><span class="sxs-lookup"><span data-stu-id="38eaf-114">-ElasticPoolName</span></span>
<span data-ttu-id="38eaf-115">Esnek bir havuzun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38eaf-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="38eaf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38eaf-116">-ResourceGroupName</span></span>
<span data-ttu-id="38eaf-117">Esnek havuzun atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38eaf-117">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="38eaf-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="38eaf-118">-ServerName</span></span>
<span data-ttu-id="38eaf-119">Elastik havuz içeren sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38eaf-119">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="38eaf-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="38eaf-120">-Confirm</span></span>
<span data-ttu-id="38eaf-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38eaf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38eaf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38eaf-122">-WhatIf</span></span>
<span data-ttu-id="38eaf-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38eaf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38eaf-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38eaf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38eaf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38eaf-125">-DefaultProfile</span></span>
<span data-ttu-id="38eaf-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38eaf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38eaf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38eaf-127">CommonParameters</span></span>
<span data-ttu-id="38eaf-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38eaf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38eaf-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38eaf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38eaf-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38eaf-130">INPUTS</span></span>

## <span data-ttu-id="38eaf-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38eaf-131">OUTPUTS</span></span>

### <span data-ttu-id="38eaf-132">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="38eaf-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="38eaf-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38eaf-133">NOTES</span></span>

## <span data-ttu-id="38eaf-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38eaf-134">RELATED LINKS</span></span>

[<span data-ttu-id="38eaf-135">Get-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="38eaf-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="38eaf-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="38eaf-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="38eaf-137">Yeni-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="38eaf-137">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="38eaf-138">Remove-Azurermsqlelaunpool</span><span class="sxs-lookup"><span data-stu-id="38eaf-138">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="38eaf-139">Set-Azurermkarekölet havuz</span><span class="sxs-lookup"><span data-stu-id="38eaf-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

