---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 5f8b237a6f7d08fc0339d3ba34d253bc457dd49f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933816"
---
# <span data-ttu-id="30bdf-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="30bdf-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="30bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="30bdf-103">Elastik iş aracısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="30bdf-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="30bdf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30bdf-104">SYNTAX</span></span>

### <span data-ttu-id="30bdf-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="30bdf-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30bdf-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="30bdf-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30bdf-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="30bdf-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30bdf-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="30bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="30bdf-109">Remove-AzSqlElasticJobAgent cmdlet 'i, esnek bir Iş aracısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="30bdf-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="30bdf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30bdf-110">EXAMPLES</span></span>

### <span data-ttu-id="30bdf-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="30bdf-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="30bdf-112">Elastik Iş aracısını kaldırır</span><span class="sxs-lookup"><span data-stu-id="30bdf-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="30bdf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30bdf-113">PARAMETERS</span></span>

### <span data-ttu-id="30bdf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30bdf-114">-DefaultProfile</span></span>
<span data-ttu-id="30bdf-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30bdf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30bdf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="30bdf-116">-Force</span></span>
<span data-ttu-id="30bdf-117">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="30bdf-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bdf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="30bdf-118">-InputObject</span></span>
<span data-ttu-id="30bdf-119">Aracı nesnesi</span><span class="sxs-lookup"><span data-stu-id="30bdf-119">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30bdf-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="30bdf-120">-Name</span></span>
<span data-ttu-id="30bdf-121">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="30bdf-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bdf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30bdf-122">-ResourceGroupName</span></span>
<span data-ttu-id="30bdf-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="30bdf-123">The resource group name</span></span>

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

### <span data-ttu-id="30bdf-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="30bdf-124">-ResourceId</span></span>
<span data-ttu-id="30bdf-125">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="30bdf-125">The agent resource id</span></span>

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

### <span data-ttu-id="30bdf-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="30bdf-126">-ServerName</span></span>
<span data-ttu-id="30bdf-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="30bdf-127">The server name</span></span>

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

### <span data-ttu-id="30bdf-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="30bdf-128">-Confirm</span></span>
<span data-ttu-id="30bdf-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30bdf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30bdf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30bdf-130">-WhatIf</span></span>
<span data-ttu-id="30bdf-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30bdf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30bdf-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30bdf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30bdf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30bdf-133">CommonParameters</span></span>
<span data-ttu-id="30bdf-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30bdf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30bdf-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="30bdf-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30bdf-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30bdf-136">INPUTS</span></span>

### <span data-ttu-id="30bdf-137">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="30bdf-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="30bdf-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30bdf-138">OUTPUTS</span></span>

### <span data-ttu-id="30bdf-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="30bdf-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="30bdf-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30bdf-140">NOTES</span></span>

## <span data-ttu-id="30bdf-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30bdf-141">RELATED LINKS</span></span>
