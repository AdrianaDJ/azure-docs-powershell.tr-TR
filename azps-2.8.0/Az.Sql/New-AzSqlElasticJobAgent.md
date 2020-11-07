---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: e4517f99c44a734902f2d75ec7d432ad73ad8038
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933840"
---
# <span data-ttu-id="d5c73-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="d5c73-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="d5c73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5c73-102">SYNOPSIS</span></span>
<span data-ttu-id="d5c73-103">Yeni bir esnek iş Aracısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="d5c73-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="d5c73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5c73-104">SYNTAX</span></span>

### <span data-ttu-id="d5c73-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5c73-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5c73-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5c73-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5c73-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d5c73-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5c73-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5c73-108">DESCRIPTION</span></span>
<span data-ttu-id="d5c73-109">New-AzSqlElasticJobAgent cmdlet 'i yeni bir elastik Iş Aracısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="d5c73-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="d5c73-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5c73-110">EXAMPLES</span></span>

### <span data-ttu-id="d5c73-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d5c73-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="d5c73-112">Yeni bir esnek Iş Aracısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="d5c73-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="d5c73-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5c73-113">PARAMETERS</span></span>

### <span data-ttu-id="d5c73-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5c73-114">-DatabaseName</span></span>
<span data-ttu-id="d5c73-115">Veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="d5c73-115">The database name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c73-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d5c73-116">-DatabaseObject</span></span>
<span data-ttu-id="d5c73-117">Aracı denetimi veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d5c73-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c73-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="d5c73-118">-DatabaseResourceId</span></span>
<span data-ttu-id="d5c73-119">Aracı denetimi veritabanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d5c73-119">The Agent Control Database Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5c73-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5c73-120">-DefaultProfile</span></span>
<span data-ttu-id="d5c73-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d5c73-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5c73-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5c73-122">-Name</span></span>
<span data-ttu-id="d5c73-123">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="d5c73-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c73-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5c73-124">-ResourceGroupName</span></span>
<span data-ttu-id="d5c73-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d5c73-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c73-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5c73-126">-ServerName</span></span>
<span data-ttu-id="d5c73-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="d5c73-127">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c73-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d5c73-128">-Tag</span></span>
<span data-ttu-id="d5c73-129">Aracı etiketleri</span><span class="sxs-lookup"><span data-stu-id="d5c73-129">The Agent Tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5c73-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5c73-130">-Confirm</span></span>
<span data-ttu-id="d5c73-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5c73-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5c73-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5c73-132">-WhatIf</span></span>
<span data-ttu-id="d5c73-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5c73-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5c73-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5c73-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5c73-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5c73-135">CommonParameters</span></span>
<span data-ttu-id="d5c73-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5c73-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5c73-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d5c73-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5c73-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5c73-138">INPUTS</span></span>

### <span data-ttu-id="d5c73-139">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="d5c73-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d5c73-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5c73-140">OUTPUTS</span></span>

### <span data-ttu-id="d5c73-141">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="d5c73-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d5c73-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5c73-142">NOTES</span></span>

## <span data-ttu-id="d5c73-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5c73-143">RELATED LINKS</span></span>
