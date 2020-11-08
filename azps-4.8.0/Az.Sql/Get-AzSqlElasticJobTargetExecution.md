---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 6e61a83d843e0ceaa7d7926060da848d80d16eae
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268743"
---
# <span data-ttu-id="28841-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="28841-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="28841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28841-102">SYNOPSIS</span></span>
<span data-ttu-id="28841-103">Bir veya daha fazla iş hedef yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="28841-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="28841-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="28841-104">SYNTAX</span></span>

### <span data-ttu-id="28841-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="28841-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28841-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="28841-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28841-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="28841-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28841-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="28841-108">DESCRIPTION</span></span>
<span data-ttu-id="28841-109">Get-AzSqlElasticJobTargetExecution cmdlet 'i iş yürütmesinden bir veya daha fazla iş hedefi yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="28841-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="28841-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="28841-110">EXAMPLES</span></span>

### <span data-ttu-id="28841-111">Örnek 1: iş yürütmelerinin bir veya daha fazla iş hedefi yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="28841-111">Example 1: Gets one or more job target executions from a job executions</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="28841-112">Örnek 2: bir iş yürütmelerinin bir veya daha fazla iş hedef yürütmelerini, adım adına göre filtreleyerek filtreleme</span><span class="sxs-lookup"><span data-stu-id="28841-112">Example 2: Gets one or more job target executions from a job executions - filtering by step name</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="28841-113">Bir veya daha fazla iş hedef yürütmelerini alır</span><span class="sxs-lookup"><span data-stu-id="28841-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="28841-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="28841-114">PARAMETERS</span></span>

### <span data-ttu-id="28841-115">-Active</span><span class="sxs-lookup"><span data-stu-id="28841-115">-Active</span></span>
<span data-ttu-id="28841-116">Etkin yürütmeleri tarafından filtre uygulanacak bayrak.</span><span class="sxs-lookup"><span data-stu-id="28841-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="28841-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="28841-117">-AgentName</span></span>
<span data-ttu-id="28841-118">Aracı adı.</span><span class="sxs-lookup"><span data-stu-id="28841-118">The agent name.</span></span>

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

### <span data-ttu-id="28841-119">-Sayı</span><span class="sxs-lookup"><span data-stu-id="28841-119">-Count</span></span>
<span data-ttu-id="28841-120">Sayı, en yüksek yürütme sayısını verir.</span><span class="sxs-lookup"><span data-stu-id="28841-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28841-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="28841-121">-CreateTimeMax</span></span>
<span data-ttu-id="28841-122">Zaman sınırı oluşturma ölçütü</span><span class="sxs-lookup"><span data-stu-id="28841-122">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28841-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="28841-123">-CreateTimeMin</span></span>
<span data-ttu-id="28841-124">En az oluşturma zamanına göre filtrele</span><span class="sxs-lookup"><span data-stu-id="28841-124">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28841-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28841-125">-DefaultProfile</span></span>
<span data-ttu-id="28841-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="28841-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28841-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="28841-127">-EndTimeMax</span></span>
<span data-ttu-id="28841-128">Bitiş zamanı maks.</span><span class="sxs-lookup"><span data-stu-id="28841-128">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28841-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="28841-129">-EndTimeMin</span></span>
<span data-ttu-id="28841-130">Bitiş saatine göre filtrele.</span><span class="sxs-lookup"><span data-stu-id="28841-130">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28841-131">-Jobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="28841-131">-JobExecutionId</span></span>
<span data-ttu-id="28841-132">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="28841-132">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28841-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="28841-133">-JobName</span></span>
<span data-ttu-id="28841-134">İş adı.</span><span class="sxs-lookup"><span data-stu-id="28841-134">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28841-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="28841-135">-ParentObject</span></span>
<span data-ttu-id="28841-136">İş yürütme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="28841-136">The job execution object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28841-137">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="28841-137">-ParentResourceId</span></span>
<span data-ttu-id="28841-138">İş yürütme kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="28841-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="28841-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28841-139">-ResourceGroupName</span></span>
<span data-ttu-id="28841-140">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="28841-140">The resource group name.</span></span>

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

### <span data-ttu-id="28841-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="28841-141">-ServerName</span></span>
<span data-ttu-id="28841-142">Sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="28841-142">The server name.</span></span>

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

### <span data-ttu-id="28841-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="28841-143">-StepName</span></span>
<span data-ttu-id="28841-144">İş adımı adı.</span><span class="sxs-lookup"><span data-stu-id="28841-144">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28841-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28841-145">CommonParameters</span></span>
<span data-ttu-id="28841-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="28841-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28841-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="28841-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28841-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="28841-148">INPUTS</span></span>

### <span data-ttu-id="28841-149">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="28841-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="28841-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="28841-150">OUTPUTS</span></span>

### <span data-ttu-id="28841-151">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="28841-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="28841-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="28841-152">NOTES</span></span>

## <span data-ttu-id="28841-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="28841-153">RELATED LINKS</span></span>
