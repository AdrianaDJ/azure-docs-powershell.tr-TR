---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266832"
---
# <span data-ttu-id="452ee-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="452ee-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="452ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="452ee-102">SYNOPSIS</span></span>
<span data-ttu-id="452ee-103">Yeni bir esnek iş Aracısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="452ee-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="452ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="452ee-104">SYNTAX</span></span>

### <span data-ttu-id="452ee-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="452ee-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="452ee-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="452ee-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="452ee-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="452ee-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="452ee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="452ee-108">DESCRIPTION</span></span>
<span data-ttu-id="452ee-109">New-AzSqlElasticJobAgent cmdlet 'i yeni bir elastik Iş Aracısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="452ee-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="452ee-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="452ee-110">EXAMPLES</span></span>

### <span data-ttu-id="452ee-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="452ee-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="452ee-112">Yeni bir esnek Iş Aracısı oluşturur</span><span class="sxs-lookup"><span data-stu-id="452ee-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="452ee-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="452ee-113">PARAMETERS</span></span>

### <span data-ttu-id="452ee-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="452ee-114">-DatabaseName</span></span>
<span data-ttu-id="452ee-115">Veritabanı adı</span><span class="sxs-lookup"><span data-stu-id="452ee-115">The database name</span></span>

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

### <span data-ttu-id="452ee-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="452ee-116">-DatabaseObject</span></span>
<span data-ttu-id="452ee-117">Aracı denetimi veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="452ee-117">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="452ee-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="452ee-118">-DatabaseResourceId</span></span>
<span data-ttu-id="452ee-119">Aracı denetimi veritabanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="452ee-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="452ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="452ee-120">-DefaultProfile</span></span>
<span data-ttu-id="452ee-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="452ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="452ee-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="452ee-122">-Name</span></span>
<span data-ttu-id="452ee-123">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="452ee-123">The Agent Name</span></span>

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

### <span data-ttu-id="452ee-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="452ee-124">-ResourceGroupName</span></span>
<span data-ttu-id="452ee-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="452ee-125">The resource group name</span></span>

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

### <span data-ttu-id="452ee-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="452ee-126">-ServerName</span></span>
<span data-ttu-id="452ee-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="452ee-127">The server name</span></span>

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

### <span data-ttu-id="452ee-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="452ee-128">-Tag</span></span>
<span data-ttu-id="452ee-129">Aracı etiketleri</span><span class="sxs-lookup"><span data-stu-id="452ee-129">The Agent Tags</span></span>

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

### <span data-ttu-id="452ee-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="452ee-130">-Confirm</span></span>
<span data-ttu-id="452ee-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="452ee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="452ee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="452ee-132">-WhatIf</span></span>
<span data-ttu-id="452ee-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="452ee-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="452ee-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="452ee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="452ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="452ee-135">CommonParameters</span></span>
<span data-ttu-id="452ee-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="452ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="452ee-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="452ee-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="452ee-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="452ee-138">INPUTS</span></span>

### <span data-ttu-id="452ee-139">Microsoft. Azure. Commands. Sql. Database. model. Azuressqldatabasemodel</span><span class="sxs-lookup"><span data-stu-id="452ee-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="452ee-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="452ee-140">OUTPUTS</span></span>

### <span data-ttu-id="452ee-141">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="452ee-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="452ee-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="452ee-142">NOTES</span></span>

## <span data-ttu-id="452ee-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="452ee-143">RELATED LINKS</span></span>
