---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ff117dfee7f660845389bd62245be4ecfd53b2f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937964"
---
# <span data-ttu-id="e29a9-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="e29a9-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="e29a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e29a9-103">İş yürütme kimliği verilen işi durdurur</span><span class="sxs-lookup"><span data-stu-id="e29a9-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="e29a9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e29a9-104">SYNTAX</span></span>

### <span data-ttu-id="e29a9-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e29a9-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e29a9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e29a9-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29a9-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="e29a9-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29a9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e29a9-108">DESCRIPTION</span></span>
<span data-ttu-id="e29a9-109">Stop-AzSqlElasticJob cmdlet 'i çalışan bir yürütme ile işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="e29a9-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="e29a9-110">İş yürütmenin geçerli durumunu döndürür</span><span class="sxs-lookup"><span data-stu-id="e29a9-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="e29a9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e29a9-111">EXAMPLES</span></span>

### <span data-ttu-id="e29a9-112">Örnek 1-çalışan iş yürütmesiyle işi durdurur</span><span class="sxs-lookup"><span data-stu-id="e29a9-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="e29a9-113">Çalışan iş yürütmesini durdurur ve geçerli durumunu döndürür</span><span class="sxs-lookup"><span data-stu-id="e29a9-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="e29a9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e29a9-114">PARAMETERS</span></span>

### <span data-ttu-id="e29a9-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e29a9-115">-AgentName</span></span>
<span data-ttu-id="e29a9-116">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="e29a9-116">The agent name</span></span>

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

### <span data-ttu-id="e29a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29a9-117">-DefaultProfile</span></span>
<span data-ttu-id="e29a9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e29a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e29a9-119">-Jobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="e29a9-119">-JobExecutionId</span></span>
<span data-ttu-id="e29a9-120">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="e29a9-120">The job execution id.</span></span>

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

### <span data-ttu-id="e29a9-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="e29a9-121">-JobName</span></span>
<span data-ttu-id="e29a9-122">İş adı</span><span class="sxs-lookup"><span data-stu-id="e29a9-122">The job name</span></span>

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

### <span data-ttu-id="e29a9-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e29a9-123">-ParentObject</span></span>
<span data-ttu-id="e29a9-124">Aracı denetimi veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e29a9-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="e29a9-125">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="e29a9-125">-ParentResourceId</span></span>
<span data-ttu-id="e29a9-126">İş yürütme kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e29a9-126">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e29a9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29a9-127">-ResourceGroupName</span></span>
<span data-ttu-id="e29a9-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e29a9-128">The resource group name</span></span>

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

### <span data-ttu-id="e29a9-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e29a9-129">-ServerName</span></span>
<span data-ttu-id="e29a9-130">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="e29a9-130">The server name</span></span>

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

### <span data-ttu-id="e29a9-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="e29a9-131">-Confirm</span></span>
<span data-ttu-id="e29a9-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e29a9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e29a9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29a9-133">-WhatIf</span></span>
<span data-ttu-id="e29a9-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e29a9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29a9-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e29a9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e29a9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29a9-136">CommonParameters</span></span>
<span data-ttu-id="e29a9-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e29a9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29a9-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e29a9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29a9-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e29a9-139">INPUTS</span></span>

### <span data-ttu-id="e29a9-140">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="e29a9-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e29a9-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e29a9-141">OUTPUTS</span></span>

### <span data-ttu-id="e29a9-142">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="e29a9-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="e29a9-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e29a9-143">NOTES</span></span>

## <span data-ttu-id="e29a9-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e29a9-144">RELATED LINKS</span></span>
