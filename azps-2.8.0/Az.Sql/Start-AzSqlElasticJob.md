---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 13e6a0bd8a4934df4d0426de38d7a56ddd5af19b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933947"
---
# <span data-ttu-id="0b4f9-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="0b4f9-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="0b4f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="0b4f9-103">İş başlatma, durumunu görüntülemek için yoklanabilir iş yürütme kimliği döndürüyor</span><span class="sxs-lookup"><span data-stu-id="0b4f9-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="0b4f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b4f9-104">SYNTAX</span></span>

### <span data-ttu-id="0b4f9-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0b4f9-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b4f9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0b4f9-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b4f9-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="0b4f9-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b4f9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b4f9-108">DESCRIPTION</span></span>
<span data-ttu-id="0b4f9-109">Start-AzSqlElasticJob cmdlet 'i, yeni iş yürütmesini döndüren bir işi başlatır</span><span class="sxs-lookup"><span data-stu-id="0b4f9-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="0b4f9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b4f9-110">EXAMPLES</span></span>

### <span data-ttu-id="0b4f9-111">Örnek 1-yeni iş yürütmesini döndüren bir işi başlatır</span><span class="sxs-lookup"><span data-stu-id="0b4f9-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="0b4f9-112">Yeni iş yürütmesini döndüren işi başlatır</span><span class="sxs-lookup"><span data-stu-id="0b4f9-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="0b4f9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b4f9-113">PARAMETERS</span></span>

### <span data-ttu-id="0b4f9-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0b4f9-114">-AgentName</span></span>
<span data-ttu-id="0b4f9-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="0b4f9-115">The agent name</span></span>

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

### <span data-ttu-id="0b4f9-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="0b4f9-116">-AsJob</span></span>
<span data-ttu-id="0b4f9-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="0b4f9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b4f9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b4f9-118">-DefaultProfile</span></span>
<span data-ttu-id="0b4f9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0b4f9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b4f9-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="0b4f9-120">-JobName</span></span>
<span data-ttu-id="0b4f9-121">İş adı</span><span class="sxs-lookup"><span data-stu-id="0b4f9-121">The job name</span></span>

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

### <span data-ttu-id="0b4f9-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0b4f9-122">-ParentObject</span></span>
<span data-ttu-id="0b4f9-123">İş nesnesi</span><span class="sxs-lookup"><span data-stu-id="0b4f9-123">The job object</span></span>

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

### <span data-ttu-id="0b4f9-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="0b4f9-124">-ParentResourceId</span></span>
<span data-ttu-id="0b4f9-125">İş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="0b4f9-125">The job resource id</span></span>

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

### <span data-ttu-id="0b4f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b4f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b4f9-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0b4f9-127">The resource group name</span></span>

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

### <span data-ttu-id="0b4f9-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b4f9-128">-ServerName</span></span>
<span data-ttu-id="0b4f9-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="0b4f9-129">The server name</span></span>

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

### <span data-ttu-id="0b4f9-130">-Bekleme</span><span class="sxs-lookup"><span data-stu-id="0b4f9-130">-Wait</span></span>
<span data-ttu-id="0b4f9-131">İşin yürütülmesinin bitmesini beklemek için bekle bayrağı</span><span class="sxs-lookup"><span data-stu-id="0b4f9-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="0b4f9-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b4f9-132">-Confirm</span></span>
<span data-ttu-id="0b4f9-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b4f9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b4f9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b4f9-134">-WhatIf</span></span>
<span data-ttu-id="0b4f9-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b4f9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b4f9-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b4f9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b4f9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b4f9-137">CommonParameters</span></span>
<span data-ttu-id="0b4f9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b4f9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b4f9-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0b4f9-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b4f9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b4f9-140">INPUTS</span></span>

### <span data-ttu-id="0b4f9-141">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="0b4f9-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0b4f9-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b4f9-142">OUTPUTS</span></span>

### <span data-ttu-id="0b4f9-143">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobexecutionmodel</span><span class="sxs-lookup"><span data-stu-id="0b4f9-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="0b4f9-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b4f9-144">NOTES</span></span>

## <span data-ttu-id="0b4f9-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b4f9-145">RELATED LINKS</span></span>

## <span data-ttu-id="0b4f9-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b4f9-146">RELATED LINKS</span></span>
