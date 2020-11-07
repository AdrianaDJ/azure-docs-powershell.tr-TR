---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 08f89698b54585127e957d68082975f8e8e9744f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933839"
---
# <span data-ttu-id="37182-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="37182-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="37182-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37182-102">SYNOPSIS</span></span>
<span data-ttu-id="37182-103">Yeni bir hedef grup oluşturur</span><span class="sxs-lookup"><span data-stu-id="37182-103">Creates a new target group</span></span>

## <span data-ttu-id="37182-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37182-104">SYNTAX</span></span>

### <span data-ttu-id="37182-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37182-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37182-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="37182-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37182-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="37182-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37182-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="37182-108">DESCRIPTION</span></span>
<span data-ttu-id="37182-109">New-AzSqlElasticJobTargetGroup cmdlet 'i yeni bir hedef grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="37182-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="37182-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37182-110">EXAMPLES</span></span>

### <span data-ttu-id="37182-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37182-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="37182-112">Boş bir hedef grup oluşturur</span><span class="sxs-lookup"><span data-stu-id="37182-112">Creates an empty target group</span></span>

## <span data-ttu-id="37182-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37182-113">PARAMETERS</span></span>

### <span data-ttu-id="37182-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="37182-114">-AgentName</span></span>
<span data-ttu-id="37182-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="37182-115">The agent name</span></span>

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

### <span data-ttu-id="37182-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37182-116">-DefaultProfile</span></span>
<span data-ttu-id="37182-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37182-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37182-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="37182-118">-Name</span></span>
<span data-ttu-id="37182-119">Hedef grup adı</span><span class="sxs-lookup"><span data-stu-id="37182-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37182-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="37182-120">-ParentObject</span></span>
<span data-ttu-id="37182-121">Aracı giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="37182-121">The agent input object</span></span>

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

### <span data-ttu-id="37182-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="37182-122">-ParentResourceId</span></span>
<span data-ttu-id="37182-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="37182-123">The agent resource id</span></span>

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

### <span data-ttu-id="37182-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37182-124">-ResourceGroupName</span></span>
<span data-ttu-id="37182-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="37182-125">The resource group name</span></span>

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

### <span data-ttu-id="37182-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="37182-126">-ServerName</span></span>
<span data-ttu-id="37182-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="37182-127">The server name</span></span>

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

### <span data-ttu-id="37182-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="37182-128">-Confirm</span></span>
<span data-ttu-id="37182-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37182-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37182-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37182-130">-WhatIf</span></span>
<span data-ttu-id="37182-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37182-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37182-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="37182-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37182-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37182-133">CommonParameters</span></span>
<span data-ttu-id="37182-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37182-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37182-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="37182-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37182-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37182-136">INPUTS</span></span>

### <span data-ttu-id="37182-137">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="37182-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="37182-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37182-138">OUTPUTS</span></span>

### <span data-ttu-id="37182-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobtargetgroupmodel</span><span class="sxs-lookup"><span data-stu-id="37182-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="37182-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37182-140">NOTES</span></span>

## <span data-ttu-id="37182-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37182-141">RELATED LINKS</span></span>
