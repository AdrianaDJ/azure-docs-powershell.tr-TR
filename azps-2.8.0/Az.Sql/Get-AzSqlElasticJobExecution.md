---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: 5b5837fb0c5fa56e8e8f9887b6d85bfc3a3a559c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933630"
---
# <span data-ttu-id="3003e-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="3003e-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="3003e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3003e-102">SYNOPSIS</span></span>
<span data-ttu-id="3003e-103">Bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="3003e-103">Gets one or more job executions</span></span>

## <span data-ttu-id="3003e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3003e-104">SYNTAX</span></span>

### <span data-ttu-id="3003e-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3003e-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3003e-106">Withjobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="3003e-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3003e-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3003e-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3003e-108">Withjobexecutionıdusingparentobject</span><span class="sxs-lookup"><span data-stu-id="3003e-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3003e-109">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="3003e-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3003e-110">Withjobexecutionidusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="3003e-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3003e-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="3003e-111">DESCRIPTION</span></span>
<span data-ttu-id="3003e-112">Get-AzSqlElasticJobExecution cmdlet 'i bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="3003e-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="3003e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3003e-113">EXAMPLES</span></span>

### <span data-ttu-id="3003e-114">Örnek 1-tüm işlerde bir veya birden çok iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="3003e-114">Example 1 - Gets one or more job executions across all jobs</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="3003e-115">Örnek 2-bir iş için bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="3003e-115">Example 2 - Gets one or more job executions for a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="3003e-116">Bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="3003e-116">Gets one or more job executions</span></span>

## <span data-ttu-id="3003e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3003e-117">PARAMETERS</span></span>

### <span data-ttu-id="3003e-118">-Active</span><span class="sxs-lookup"><span data-stu-id="3003e-118">-Active</span></span>
<span data-ttu-id="3003e-119">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="3003e-119">Filter by create time min</span></span>

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

### <span data-ttu-id="3003e-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3003e-120">-AgentName</span></span>
<span data-ttu-id="3003e-121">Aracı adı.</span><span class="sxs-lookup"><span data-stu-id="3003e-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3003e-122">-Sayı</span><span class="sxs-lookup"><span data-stu-id="3003e-122">-Count</span></span>
<span data-ttu-id="3003e-123">Sayı, en yüksek yürütme sayısını verir.</span><span class="sxs-lookup"><span data-stu-id="3003e-123">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3003e-124">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="3003e-124">-CreateTimeMax</span></span>
<span data-ttu-id="3003e-125">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="3003e-125">Filter by create time min</span></span>

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

### <span data-ttu-id="3003e-126">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="3003e-126">-CreateTimeMin</span></span>
<span data-ttu-id="3003e-127">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="3003e-127">Filter by create time min</span></span>

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

### <span data-ttu-id="3003e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3003e-128">-DefaultProfile</span></span>
<span data-ttu-id="3003e-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3003e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3003e-130">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="3003e-130">-EndTimeMax</span></span>
<span data-ttu-id="3003e-131">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="3003e-131">Filter by create time min</span></span>

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

### <span data-ttu-id="3003e-132">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="3003e-132">-EndTimeMin</span></span>
<span data-ttu-id="3003e-133">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="3003e-133">Filter by create time min</span></span>

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

### <span data-ttu-id="3003e-134">-Jobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="3003e-134">-JobExecutionId</span></span>
<span data-ttu-id="3003e-135">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="3003e-135">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3003e-136">-JobName</span><span class="sxs-lookup"><span data-stu-id="3003e-136">-JobName</span></span>
<span data-ttu-id="3003e-137">İş adı.</span><span class="sxs-lookup"><span data-stu-id="3003e-137">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3003e-138">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3003e-138">-ParentObject</span></span>
<span data-ttu-id="3003e-139">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="3003e-139">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3003e-140">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="3003e-140">-ParentResourceId</span></span>
<span data-ttu-id="3003e-141">Aracı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="3003e-141">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3003e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3003e-142">-ResourceGroupName</span></span>
<span data-ttu-id="3003e-143">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3003e-143">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3003e-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3003e-144">-ServerName</span></span>
<span data-ttu-id="3003e-145">Sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="3003e-145">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3003e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3003e-146">CommonParameters</span></span>
<span data-ttu-id="3003e-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3003e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3003e-148">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3003e-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3003e-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3003e-149">INPUTS</span></span>

### <span data-ttu-id="3003e-150">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="3003e-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="3003e-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3003e-151">OUTPUTS</span></span>

### <span data-ttu-id="3003e-152">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="3003e-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="3003e-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3003e-153">NOTES</span></span>

## <span data-ttu-id="3003e-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3003e-154">RELATED LINKS</span></span>
