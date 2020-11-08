---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107544"
---
# <span data-ttu-id="7a47c-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="7a47c-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="7a47c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a47c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a47c-103">İş yürütme kimliği verilen işi durdurur</span><span class="sxs-lookup"><span data-stu-id="7a47c-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="7a47c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a47c-104">SYNTAX</span></span>

### <span data-ttu-id="7a47c-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a47c-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7a47c-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a47c-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a47c-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="7a47c-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a47c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a47c-108">DESCRIPTION</span></span>
<span data-ttu-id="7a47c-109">Stop-AzSqlElasticJob cmdlet 'i çalışan bir yürütme ile işi durdurur.</span><span class="sxs-lookup"><span data-stu-id="7a47c-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="7a47c-110">İş yürütmenin geçerli durumunu döndürür</span><span class="sxs-lookup"><span data-stu-id="7a47c-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="7a47c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a47c-111">EXAMPLES</span></span>

### <span data-ttu-id="7a47c-112">Örnek 1: çalışan iş yürütmesiyle işi durdurur</span><span class="sxs-lookup"><span data-stu-id="7a47c-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="7a47c-113">Çalışan iş yürütmesini durdurur ve geçerli durumunu döndürür</span><span class="sxs-lookup"><span data-stu-id="7a47c-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="7a47c-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7a47c-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="7a47c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a47c-115">PARAMETERS</span></span>

### <span data-ttu-id="7a47c-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7a47c-116">-AgentName</span></span>
<span data-ttu-id="7a47c-117">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="7a47c-117">The agent name</span></span>

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

### <span data-ttu-id="7a47c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a47c-118">-DefaultProfile</span></span>
<span data-ttu-id="7a47c-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a47c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a47c-120">-Jobexecutionıd</span><span class="sxs-lookup"><span data-stu-id="7a47c-120">-JobExecutionId</span></span>
<span data-ttu-id="7a47c-121">İş yürütme kimliği.</span><span class="sxs-lookup"><span data-stu-id="7a47c-121">The job execution id.</span></span>

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

### <span data-ttu-id="7a47c-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="7a47c-122">-JobName</span></span>
<span data-ttu-id="7a47c-123">İş adı</span><span class="sxs-lookup"><span data-stu-id="7a47c-123">The job name</span></span>

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

### <span data-ttu-id="7a47c-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7a47c-124">-ParentObject</span></span>
<span data-ttu-id="7a47c-125">Aracı denetimi veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7a47c-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="7a47c-126">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7a47c-126">-ParentResourceId</span></span>
<span data-ttu-id="7a47c-127">İş yürütme kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7a47c-127">The job execution resource id</span></span>

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

### <span data-ttu-id="7a47c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a47c-128">-ResourceGroupName</span></span>
<span data-ttu-id="7a47c-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7a47c-129">The resource group name</span></span>

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

### <span data-ttu-id="7a47c-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a47c-130">-ServerName</span></span>
<span data-ttu-id="7a47c-131">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="7a47c-131">The server name</span></span>

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

### <span data-ttu-id="7a47c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="7a47c-132">-Confirm</span></span>
<span data-ttu-id="7a47c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7a47c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a47c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a47c-134">-WhatIf</span></span>
<span data-ttu-id="7a47c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a47c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a47c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7a47c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a47c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a47c-137">CommonParameters</span></span>
<span data-ttu-id="7a47c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a47c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a47c-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7a47c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a47c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a47c-140">INPUTS</span></span>

### <span data-ttu-id="7a47c-141">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="7a47c-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="7a47c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a47c-142">OUTPUTS</span></span>

### <span data-ttu-id="7a47c-143">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="7a47c-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="7a47c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a47c-144">NOTES</span></span>

## <span data-ttu-id="7a47c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a47c-145">RELATED LINKS</span></span>
