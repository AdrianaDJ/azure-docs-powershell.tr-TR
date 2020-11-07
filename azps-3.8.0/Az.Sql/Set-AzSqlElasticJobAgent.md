---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938024"
---
# <span data-ttu-id="d1156-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="d1156-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="d1156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1156-102">SYNOPSIS</span></span>
<span data-ttu-id="d1156-103">Elastik iş aracısını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="d1156-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="d1156-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d1156-104">SYNTAX</span></span>

### <span data-ttu-id="d1156-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d1156-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1156-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d1156-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1156-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="d1156-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1156-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d1156-108">DESCRIPTION</span></span>
<span data-ttu-id="d1156-109">Set-AzSqlElasticJobAgent cmdlet 'i elastik Iş aracılarını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="d1156-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="d1156-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d1156-110">EXAMPLES</span></span>

### <span data-ttu-id="d1156-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d1156-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="d1156-112">Elastik Iş aracısını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="d1156-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="d1156-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d1156-113">PARAMETERS</span></span>

### <span data-ttu-id="d1156-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1156-114">-DefaultProfile</span></span>
<span data-ttu-id="d1156-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d1156-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1156-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1156-116">-InputObject</span></span>
<span data-ttu-id="d1156-117">Aracı giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="d1156-117">The agent input object</span></span>

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

### <span data-ttu-id="d1156-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="d1156-118">-Name</span></span>
<span data-ttu-id="d1156-119">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="d1156-119">The agent name</span></span>

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

### <span data-ttu-id="d1156-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1156-120">-ResourceGroupName</span></span>
<span data-ttu-id="d1156-121">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d1156-121">The resource group name</span></span>

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

### <span data-ttu-id="d1156-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d1156-122">-ResourceId</span></span>
<span data-ttu-id="d1156-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d1156-123">The agent resource id</span></span>

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

### <span data-ttu-id="d1156-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1156-124">-ServerName</span></span>
<span data-ttu-id="d1156-125">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="d1156-125">The server name</span></span>

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

### <span data-ttu-id="d1156-126">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d1156-126">-Tag</span></span>
<span data-ttu-id="d1156-127">Azure SQL veritabanı aracısıyla ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="d1156-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="d1156-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d1156-128">-Confirm</span></span>
<span data-ttu-id="d1156-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d1156-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1156-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1156-130">-WhatIf</span></span>
<span data-ttu-id="d1156-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d1156-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1156-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d1156-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1156-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1156-133">CommonParameters</span></span>
<span data-ttu-id="d1156-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d1156-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1156-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d1156-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1156-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d1156-136">INPUTS</span></span>

### <span data-ttu-id="d1156-137">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="d1156-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d1156-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d1156-138">OUTPUTS</span></span>

### <span data-ttu-id="d1156-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="d1156-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="d1156-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d1156-140">NOTES</span></span>

## <span data-ttu-id="d1156-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d1156-141">RELATED LINKS</span></span>
