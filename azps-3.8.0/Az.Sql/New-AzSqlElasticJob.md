---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 98c019c8dedf767fc2b75bb2133f7c545ffd03ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937416"
---
# <span data-ttu-id="22ec0-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="22ec0-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="22ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="22ec0-103">Yeni iş oluşturur</span><span class="sxs-lookup"><span data-stu-id="22ec0-103">Creates a new job</span></span>

## <span data-ttu-id="22ec0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22ec0-104">SYNTAX</span></span>

### <span data-ttu-id="22ec0-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="22ec0-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ec0-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="22ec0-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ec0-107">Günlük</span><span class="sxs-lookup"><span data-stu-id="22ec0-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ec0-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="22ec0-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ec0-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="22ec0-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ec0-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="22ec0-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ec0-111">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="22ec0-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ec0-112">Runonceusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="22ec0-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ec0-113">Recurringusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="22ec0-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22ec0-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="22ec0-114">DESCRIPTION</span></span>
<span data-ttu-id="22ec0-115">New-AzSqlElasticJob cmdlet 'i yeni bir iş oluşturur</span><span class="sxs-lookup"><span data-stu-id="22ec0-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="22ec0-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22ec0-116">EXAMPLES</span></span>

### <span data-ttu-id="22ec0-117">Örnek 1-yeni bir iş oluşturur</span><span class="sxs-lookup"><span data-stu-id="22ec0-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="22ec0-118">Yeni iş oluşturur</span><span class="sxs-lookup"><span data-stu-id="22ec0-118">Creates a new job</span></span>

## <span data-ttu-id="22ec0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22ec0-119">PARAMETERS</span></span>

### <span data-ttu-id="22ec0-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="22ec0-120">-AgentName</span></span>
<span data-ttu-id="22ec0-121">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="22ec0-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ec0-122">-DefaultProfile</span></span>
<span data-ttu-id="22ec0-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22ec0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22ec0-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="22ec0-124">-Description</span></span>
<span data-ttu-id="22ec0-125">İş açıklaması</span><span class="sxs-lookup"><span data-stu-id="22ec0-125">The job description</span></span>

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

### <span data-ttu-id="22ec0-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="22ec0-126">-Enable</span></span>
<span data-ttu-id="22ec0-127">Müşterinin bu işin etkinleştirilmesini istediğini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="22ec0-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="22ec0-128">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="22ec0-128">-EndTime</span></span>
<span data-ttu-id="22ec0-129">İş zamanlaması bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="22ec0-129">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-130">-Interncount</span><span class="sxs-lookup"><span data-stu-id="22ec0-130">-IntervalCount</span></span>
<span data-ttu-id="22ec0-131">Yinelenen zamanlama aralığı sayısı</span><span class="sxs-lookup"><span data-stu-id="22ec0-131">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-132">-Intertip türü</span><span class="sxs-lookup"><span data-stu-id="22ec0-132">-IntervalType</span></span>
<span data-ttu-id="22ec0-133">Yinelenen zamanlama aralığı türü; dakika, saat, gün, hafta, ay olabilir</span><span class="sxs-lookup"><span data-stu-id="22ec0-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="22ec0-134">-Name</span></span>
<span data-ttu-id="22ec0-135">İş adı</span><span class="sxs-lookup"><span data-stu-id="22ec0-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="22ec0-136">-ParentObject</span></span>
<span data-ttu-id="22ec0-137">Aracı giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="22ec0-137">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-138">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="22ec0-138">-ParentResourceId</span></span>
<span data-ttu-id="22ec0-139">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="22ec0-139">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ec0-140">-ResourceGroupName</span></span>
<span data-ttu-id="22ec0-141">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="22ec0-141">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="22ec0-142">-RunOnce</span></span>
<span data-ttu-id="22ec0-143">İş bir kez çalışacak şekilde işaretle</span><span class="sxs-lookup"><span data-stu-id="22ec0-143">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="22ec0-144">-ServerName</span></span>
<span data-ttu-id="22ec0-145">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="22ec0-145">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-146">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="22ec0-146">-StartTime</span></span>
<span data-ttu-id="22ec0-147">İş zamanlaması başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="22ec0-147">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22ec0-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="22ec0-148">-Confirm</span></span>
<span data-ttu-id="22ec0-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="22ec0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ec0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ec0-150">-WhatIf</span></span>
<span data-ttu-id="22ec0-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="22ec0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ec0-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="22ec0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ec0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ec0-153">CommonParameters</span></span>
<span data-ttu-id="22ec0-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22ec0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ec0-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="22ec0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ec0-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22ec0-156">INPUTS</span></span>

### <span data-ttu-id="22ec0-157">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="22ec0-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="22ec0-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22ec0-158">OUTPUTS</span></span>

### <span data-ttu-id="22ec0-159">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="22ec0-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="22ec0-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22ec0-160">NOTES</span></span>

## <span data-ttu-id="22ec0-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22ec0-161">RELATED LINKS</span></span>
