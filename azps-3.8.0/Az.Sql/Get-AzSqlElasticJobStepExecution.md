---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938440"
---
# <span data-ttu-id="2e789-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="2e789-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="2e789-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e789-102">SYNOPSIS</span></span>
<span data-ttu-id="2e789-103">Bir veya daha fazla iş adımı yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="2e789-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="2e789-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e789-104">SYNTAX</span></span>

### <span data-ttu-id="2e789-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e789-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e789-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="2e789-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e789-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2e789-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e789-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2e789-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e789-109">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="2e789-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e789-110">Withjobstepnameusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="2e789-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e789-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e789-111">DESCRIPTION</span></span>
<span data-ttu-id="2e789-112">Get-AzSqlElasticJobStepExecution cmdlet 'i iş yürütmesinden bir veya daha fazla iş adımı yürütmelerini alıyor</span><span class="sxs-lookup"><span data-stu-id="2e789-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="2e789-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e789-113">EXAMPLES</span></span>

### <span data-ttu-id="2e789-114">Örnek 1-iş yürütmelerinin bir veya birden çok iş adımı yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="2e789-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="2e789-115">Örnek 2-iş yürütmeden bir veya daha fazla iş adımı yürütmelerini alır, adım adına göre filtreleme</span><span class="sxs-lookup"><span data-stu-id="2e789-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="2e789-116">Bir veya daha fazla iş adımı yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="2e789-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="2e789-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e789-117">PARAMETERS</span></span>

### <span data-ttu-id="2e789-118">-Active</span><span class="sxs-lookup"><span data-stu-id="2e789-118">-Active</span></span>
<span data-ttu-id="2e789-119">Etkin yürütmeleri tarafından filtre uygulanacak bayrak.</span><span class="sxs-lookup"><span data-stu-id="2e789-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2e789-120">-AgentName</span></span>
<span data-ttu-id="2e789-121">Aracı adı.</span><span class="sxs-lookup"><span data-stu-id="2e789-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="2e789-122">-CreateTimeMax</span></span>
<span data-ttu-id="2e789-123">Zaman sınırı oluşturma ölçütü</span><span class="sxs-lookup"><span data-stu-id="2e789-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="2e789-124">-CreateTimeMin</span></span>
<span data-ttu-id="2e789-125">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="2e789-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e789-126">-DefaultProfile</span></span>
<span data-ttu-id="2e789-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e789-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e789-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="2e789-128">-EndTimeMax</span></span>
<span data-ttu-id="2e789-129">Bitiş zamanı maks.</span><span class="sxs-lookup"><span data-stu-id="2e789-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="2e789-130">-EndTimeMin</span></span>
<span data-ttu-id="2e789-131">Bitiş saatine göre filtrele.</span><span class="sxs-lookup"><span data-stu-id="2e789-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-132">-Jobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="2e789-132">-JobExecutionId</span></span>
<span data-ttu-id="2e789-133">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="2e789-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="2e789-134">-JobName</span></span>
<span data-ttu-id="2e789-135">İş adı.</span><span class="sxs-lookup"><span data-stu-id="2e789-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e789-136">-ParentObject</span></span>
<span data-ttu-id="2e789-137">Aracı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2e789-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-138">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="2e789-138">-ParentResourceId</span></span>
<span data-ttu-id="2e789-139">İş yürütme kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="2e789-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e789-140">-ResourceGroupName</span></span>
<span data-ttu-id="2e789-141">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2e789-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e789-142">-ServerName</span></span>
<span data-ttu-id="2e789-143">Sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="2e789-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="2e789-144">-StepName</span></span>
<span data-ttu-id="2e789-145">İş adımı adı.</span><span class="sxs-lookup"><span data-stu-id="2e789-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e789-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e789-146">CommonParameters</span></span>
<span data-ttu-id="2e789-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e789-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e789-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2e789-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e789-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e789-149">INPUTS</span></span>

### <span data-ttu-id="2e789-150">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="2e789-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2e789-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e789-151">OUTPUTS</span></span>

### <span data-ttu-id="2e789-152">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="2e789-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2e789-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e789-153">NOTES</span></span>

## <span data-ttu-id="2e789-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e789-154">RELATED LINKS</span></span>