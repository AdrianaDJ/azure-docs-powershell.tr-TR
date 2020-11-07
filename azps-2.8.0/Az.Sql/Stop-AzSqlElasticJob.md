---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: 0b7fc702ad331a2ad51e1adfaf4aefd6ae440259
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933938"
---
# <span data-ttu-id="8c470-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="8c470-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="8c470-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c470-102">SYNOPSIS</span></span>
<span data-ttu-id="8c470-103">İş yürütme kimliği verilen işi durdurur</span><span class="sxs-lookup"><span data-stu-id="8c470-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="8c470-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8c470-104">SYNTAX</span></span>

### <span data-ttu-id="8c470-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8c470-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c470-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8c470-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c470-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="8c470-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c470-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8c470-108">DESCRIPTION</span></span>
<span data-ttu-id="8c470-109">Stop-AzSqlElasticJob cmdlet 'i çalışan bir yürütme ile işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="8c470-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="8c470-110">İş yürütmenin geçerli durumunu döndürür</span><span class="sxs-lookup"><span data-stu-id="8c470-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="8c470-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8c470-111">EXAMPLES</span></span>

### <span data-ttu-id="8c470-112">Örnek 1-çalışan iş yürütmesiyle işi durdurur</span><span class="sxs-lookup"><span data-stu-id="8c470-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="8c470-113">Çalışan iş yürütmesini durdurur ve geçerli durumunu döndürür</span><span class="sxs-lookup"><span data-stu-id="8c470-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="8c470-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8c470-114">PARAMETERS</span></span>

### <span data-ttu-id="8c470-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8c470-115">-AgentName</span></span>
<span data-ttu-id="8c470-116">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="8c470-116">The agent name</span></span>

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

### <span data-ttu-id="8c470-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c470-117">-DefaultProfile</span></span>
<span data-ttu-id="8c470-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8c470-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c470-119">-Jobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="8c470-119">-JobExecutionId</span></span>
<span data-ttu-id="8c470-120">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="8c470-120">The job execution id.</span></span>

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

### <span data-ttu-id="8c470-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="8c470-121">-JobName</span></span>
<span data-ttu-id="8c470-122">İş adı</span><span class="sxs-lookup"><span data-stu-id="8c470-122">The job name</span></span>

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

### <span data-ttu-id="8c470-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8c470-123">-ParentObject</span></span>
<span data-ttu-id="8c470-124">Aracı denetimi veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="8c470-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="8c470-125">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="8c470-125">-ParentResourceId</span></span>
<span data-ttu-id="8c470-126">İş yürütme kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="8c470-126">The job execution resource id</span></span>

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

### <span data-ttu-id="8c470-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c470-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c470-128">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="8c470-128">The resource group name</span></span>

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

### <span data-ttu-id="8c470-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8c470-129">-ServerName</span></span>
<span data-ttu-id="8c470-130">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="8c470-130">The server name</span></span>

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

### <span data-ttu-id="8c470-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="8c470-131">-Confirm</span></span>
<span data-ttu-id="8c470-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8c470-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c470-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c470-133">-WhatIf</span></span>
<span data-ttu-id="8c470-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8c470-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c470-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8c470-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c470-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c470-136">CommonParameters</span></span>
<span data-ttu-id="8c470-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8c470-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c470-138">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8c470-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c470-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8c470-139">INPUTS</span></span>

### <span data-ttu-id="8c470-140">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="8c470-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="8c470-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8c470-141">OUTPUTS</span></span>

### <span data-ttu-id="8c470-142">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="8c470-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="8c470-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8c470-143">NOTES</span></span>

## <span data-ttu-id="8c470-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c470-144">RELATED LINKS</span></span>

## <span data-ttu-id="8c470-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8c470-145">RELATED LINKS</span></span>
