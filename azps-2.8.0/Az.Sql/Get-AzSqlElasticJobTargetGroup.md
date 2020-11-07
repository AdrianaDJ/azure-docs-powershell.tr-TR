---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: fd2f8cc12faa1a08eb8f30743c88d5d3e44e48fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933725"
---
# <span data-ttu-id="69150-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="69150-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="69150-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69150-102">SYNOPSIS</span></span>
<span data-ttu-id="69150-103">Bir veya daha fazla iş hedef grubunu alır</span><span class="sxs-lookup"><span data-stu-id="69150-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="69150-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69150-104">SYNTAX</span></span>

### <span data-ttu-id="69150-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69150-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69150-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="69150-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69150-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="69150-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69150-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="69150-108">DESCRIPTION</span></span>
<span data-ttu-id="69150-109">Get-AzSqlElasticJobTargetGroup cmdlet 'i hedef grubu alır ve hedefler</span><span class="sxs-lookup"><span data-stu-id="69150-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="69150-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69150-110">EXAMPLES</span></span>

### <span data-ttu-id="69150-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="69150-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="69150-112">Hedef grubu ve hedeflerini alır</span><span class="sxs-lookup"><span data-stu-id="69150-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="69150-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69150-113">PARAMETERS</span></span>

### <span data-ttu-id="69150-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="69150-114">-AgentName</span></span>
<span data-ttu-id="69150-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="69150-115">The agent name</span></span>

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

### <span data-ttu-id="69150-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69150-116">-DefaultProfile</span></span>
<span data-ttu-id="69150-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69150-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69150-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="69150-118">-Name</span></span>
<span data-ttu-id="69150-119">Hedef grup adı</span><span class="sxs-lookup"><span data-stu-id="69150-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69150-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="69150-120">-ParentObject</span></span>
<span data-ttu-id="69150-121">Aracı nesnesi</span><span class="sxs-lookup"><span data-stu-id="69150-121">The agent object</span></span>

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

### <span data-ttu-id="69150-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="69150-122">-ParentResourceId</span></span>
<span data-ttu-id="69150-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="69150-123">The agent resource id</span></span>

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

### <span data-ttu-id="69150-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69150-124">-ResourceGroupName</span></span>
<span data-ttu-id="69150-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="69150-125">The resource group name</span></span>

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

### <span data-ttu-id="69150-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69150-126">-ServerName</span></span>
<span data-ttu-id="69150-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="69150-127">The server name</span></span>

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

### <span data-ttu-id="69150-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69150-128">CommonParameters</span></span>
<span data-ttu-id="69150-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69150-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69150-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="69150-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69150-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69150-131">INPUTS</span></span>

### <span data-ttu-id="69150-132">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="69150-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="69150-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69150-133">OUTPUTS</span></span>

### <span data-ttu-id="69150-134">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobtargetgroupmodel</span><span class="sxs-lookup"><span data-stu-id="69150-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="69150-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69150-135">NOTES</span></span>

## <span data-ttu-id="69150-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69150-136">RELATED LINKS</span></span>
