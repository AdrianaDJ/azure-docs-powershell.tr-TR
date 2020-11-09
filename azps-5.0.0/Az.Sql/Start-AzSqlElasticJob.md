---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322058"
---
# <span data-ttu-id="59a70-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="59a70-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="59a70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59a70-102">SYNOPSIS</span></span>
<span data-ttu-id="59a70-103">İş başlatma, durumunu görüntülemek için yoklanabilir iş yürütme kimliği döndürüyor</span><span class="sxs-lookup"><span data-stu-id="59a70-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="59a70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59a70-104">SYNTAX</span></span>

### <span data-ttu-id="59a70-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59a70-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59a70-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="59a70-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59a70-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="59a70-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59a70-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="59a70-108">DESCRIPTION</span></span>
<span data-ttu-id="59a70-109">Start-AzSqlElasticJob cmdlet 'i, yeni iş yürütmesini döndüren bir işi başlatır</span><span class="sxs-lookup"><span data-stu-id="59a70-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="59a70-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59a70-110">EXAMPLES</span></span>

### <span data-ttu-id="59a70-111">Örnek 1-yeni iş yürütmesini döndüren bir işi başlatır</span><span class="sxs-lookup"><span data-stu-id="59a70-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="59a70-112">Yeni iş yürütmesini döndüren işi başlatır</span><span class="sxs-lookup"><span data-stu-id="59a70-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="59a70-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59a70-113">PARAMETERS</span></span>

### <span data-ttu-id="59a70-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="59a70-114">-AgentName</span></span>
<span data-ttu-id="59a70-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="59a70-115">The agent name</span></span>

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

### <span data-ttu-id="59a70-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="59a70-116">-AsJob</span></span>
<span data-ttu-id="59a70-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="59a70-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59a70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59a70-118">-DefaultProfile</span></span>
<span data-ttu-id="59a70-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59a70-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59a70-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="59a70-120">-JobName</span></span>
<span data-ttu-id="59a70-121">İş adı</span><span class="sxs-lookup"><span data-stu-id="59a70-121">The job name</span></span>

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

### <span data-ttu-id="59a70-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="59a70-122">-ParentObject</span></span>
<span data-ttu-id="59a70-123">İş nesnesi</span><span class="sxs-lookup"><span data-stu-id="59a70-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59a70-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="59a70-124">-ParentResourceId</span></span>
<span data-ttu-id="59a70-125">İş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="59a70-125">The job resource id</span></span>

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

### <span data-ttu-id="59a70-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59a70-126">-ResourceGroupName</span></span>
<span data-ttu-id="59a70-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="59a70-127">The resource group name</span></span>

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

### <span data-ttu-id="59a70-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="59a70-128">-ServerName</span></span>
<span data-ttu-id="59a70-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="59a70-129">The server name</span></span>

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

### <span data-ttu-id="59a70-130">-Bekleme</span><span class="sxs-lookup"><span data-stu-id="59a70-130">-Wait</span></span>
<span data-ttu-id="59a70-131">İşin yürütülmesinin bitmesini beklemek için bekle bayrağı</span><span class="sxs-lookup"><span data-stu-id="59a70-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="59a70-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="59a70-132">-Confirm</span></span>
<span data-ttu-id="59a70-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59a70-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59a70-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59a70-134">-WhatIf</span></span>
<span data-ttu-id="59a70-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59a70-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59a70-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59a70-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59a70-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59a70-137">CommonParameters</span></span>
<span data-ttu-id="59a70-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59a70-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59a70-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="59a70-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59a70-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59a70-140">INPUTS</span></span>

### <span data-ttu-id="59a70-141">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="59a70-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="59a70-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59a70-142">OUTPUTS</span></span>

### <span data-ttu-id="59a70-143">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="59a70-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="59a70-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59a70-144">NOTES</span></span>

## <span data-ttu-id="59a70-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59a70-145">RELATED LINKS</span></span>
