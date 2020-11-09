---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323599"
---
# <span data-ttu-id="9fda7-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="9fda7-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="9fda7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fda7-102">SYNOPSIS</span></span>
<span data-ttu-id="9fda7-103">Elastik iş aracısını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="9fda7-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="9fda7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9fda7-104">SYNTAX</span></span>

### <span data-ttu-id="9fda7-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9fda7-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fda7-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9fda7-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fda7-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="9fda7-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fda7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="9fda7-108">DESCRIPTION</span></span>
<span data-ttu-id="9fda7-109">Set-AzSqlElasticJobAgent cmdlet 'i elastik Iş aracılarını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="9fda7-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="9fda7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9fda7-110">EXAMPLES</span></span>

### <span data-ttu-id="9fda7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9fda7-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="9fda7-112">Elastik Iş aracısını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="9fda7-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="9fda7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9fda7-113">PARAMETERS</span></span>

### <span data-ttu-id="9fda7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fda7-114">-DefaultProfile</span></span>
<span data-ttu-id="9fda7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9fda7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fda7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fda7-116">-InputObject</span></span>
<span data-ttu-id="9fda7-117">Aracı giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="9fda7-117">The agent input object</span></span>

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

### <span data-ttu-id="9fda7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="9fda7-118">-Name</span></span>
<span data-ttu-id="9fda7-119">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="9fda7-119">The agent name</span></span>

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

### <span data-ttu-id="9fda7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fda7-120">-ResourceGroupName</span></span>
<span data-ttu-id="9fda7-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9fda7-121">The resource group name</span></span>

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

### <span data-ttu-id="9fda7-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9fda7-122">-ResourceId</span></span>
<span data-ttu-id="9fda7-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9fda7-123">The agent resource id</span></span>

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

### <span data-ttu-id="9fda7-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9fda7-124">-ServerName</span></span>
<span data-ttu-id="9fda7-125">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="9fda7-125">The server name</span></span>

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

### <span data-ttu-id="9fda7-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="9fda7-126">-Tag</span></span>
<span data-ttu-id="9fda7-127">Azure SQL veritabanı aracısıyla ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="9fda7-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="9fda7-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="9fda7-128">-Confirm</span></span>
<span data-ttu-id="9fda7-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9fda7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fda7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fda7-130">-WhatIf</span></span>
<span data-ttu-id="9fda7-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9fda7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fda7-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9fda7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fda7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fda7-133">CommonParameters</span></span>
<span data-ttu-id="9fda7-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9fda7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fda7-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9fda7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fda7-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9fda7-136">INPUTS</span></span>

### <span data-ttu-id="9fda7-137">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="9fda7-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9fda7-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9fda7-138">OUTPUTS</span></span>

### <span data-ttu-id="9fda7-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="9fda7-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9fda7-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9fda7-140">NOTES</span></span>

## <span data-ttu-id="9fda7-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9fda7-141">RELATED LINKS</span></span>
