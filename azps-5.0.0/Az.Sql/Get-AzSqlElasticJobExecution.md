---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275839"
---
# <span data-ttu-id="b3830-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="b3830-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="b3830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3830-102">SYNOPSIS</span></span>
<span data-ttu-id="b3830-103">Bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="b3830-103">Gets one or more job executions</span></span>

## <span data-ttu-id="b3830-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3830-104">SYNTAX</span></span>

### <span data-ttu-id="b3830-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b3830-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b3830-106">Withjobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="b3830-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3830-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b3830-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3830-108">Withjobexecutionıdusingparentobject</span><span class="sxs-lookup"><span data-stu-id="b3830-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3830-109">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b3830-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3830-110">Withjobexecutionidusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="b3830-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3830-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3830-111">DESCRIPTION</span></span>
<span data-ttu-id="b3830-112">Get-AzSqlElasticJobExecution cmdlet 'i bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="b3830-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="b3830-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3830-113">EXAMPLES</span></span>

### <span data-ttu-id="b3830-114">Örnek 1: tüm işlerde bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="b3830-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="b3830-115">Örnek 2: bir iş için bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="b3830-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="b3830-116">Bir veya daha fazla iş yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="b3830-116">Gets one or more job executions</span></span>

### <span data-ttu-id="b3830-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="b3830-117">Example 3</span></span>

<span data-ttu-id="b3830-118">Bir veya daha fazla iş yürütmelerini alır.</span><span class="sxs-lookup"><span data-stu-id="b3830-118">Gets one or more job executions.</span></span> <span data-ttu-id="b3830-119">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="b3830-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="b3830-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3830-120">PARAMETERS</span></span>

### <span data-ttu-id="b3830-121">-Active</span><span class="sxs-lookup"><span data-stu-id="b3830-121">-Active</span></span>
<span data-ttu-id="b3830-122">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="b3830-122">Filter by create time min</span></span>

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

### <span data-ttu-id="b3830-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b3830-123">-AgentName</span></span>
<span data-ttu-id="b3830-124">Aracı adı.</span><span class="sxs-lookup"><span data-stu-id="b3830-124">The agent name.</span></span>

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

### <span data-ttu-id="b3830-125">-Sayı</span><span class="sxs-lookup"><span data-stu-id="b3830-125">-Count</span></span>
<span data-ttu-id="b3830-126">Sayı, en yüksek yürütme sayısını verir.</span><span class="sxs-lookup"><span data-stu-id="b3830-126">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="b3830-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="b3830-127">-CreateTimeMax</span></span>
<span data-ttu-id="b3830-128">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="b3830-128">Filter by create time min</span></span>

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

### <span data-ttu-id="b3830-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="b3830-129">-CreateTimeMin</span></span>
<span data-ttu-id="b3830-130">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="b3830-130">Filter by create time min</span></span>

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

### <span data-ttu-id="b3830-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3830-131">-DefaultProfile</span></span>
<span data-ttu-id="b3830-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3830-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3830-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="b3830-133">-EndTimeMax</span></span>
<span data-ttu-id="b3830-134">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="b3830-134">Filter by create time min</span></span>

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

### <span data-ttu-id="b3830-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="b3830-135">-EndTimeMin</span></span>
<span data-ttu-id="b3830-136">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="b3830-136">Filter by create time min</span></span>

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

### <span data-ttu-id="b3830-137">-Jobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="b3830-137">-JobExecutionId</span></span>
<span data-ttu-id="b3830-138">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="b3830-138">The job execution id.</span></span>

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

### <span data-ttu-id="b3830-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="b3830-139">-JobName</span></span>
<span data-ttu-id="b3830-140">İş adı.</span><span class="sxs-lookup"><span data-stu-id="b3830-140">The job name.</span></span>

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

### <span data-ttu-id="b3830-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b3830-141">-ParentObject</span></span>
<span data-ttu-id="b3830-142">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="b3830-142">The job execution id.</span></span>

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

### <span data-ttu-id="b3830-143">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="b3830-143">-ParentResourceId</span></span>
<span data-ttu-id="b3830-144">Aracı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="b3830-144">The agent resource id.</span></span>

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

### <span data-ttu-id="b3830-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3830-145">-ResourceGroupName</span></span>
<span data-ttu-id="b3830-146">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b3830-146">The resource group name.</span></span>

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

### <span data-ttu-id="b3830-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3830-147">-ServerName</span></span>
<span data-ttu-id="b3830-148">Sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="b3830-148">The server name.</span></span>

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

### <span data-ttu-id="b3830-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3830-149">CommonParameters</span></span>
<span data-ttu-id="b3830-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3830-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3830-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b3830-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3830-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3830-152">INPUTS</span></span>

### <span data-ttu-id="b3830-153">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="b3830-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b3830-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3830-154">OUTPUTS</span></span>

### <span data-ttu-id="b3830-155">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="b3830-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="b3830-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3830-156">NOTES</span></span>

## <span data-ttu-id="b3830-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3830-157">RELATED LINKS</span></span>
