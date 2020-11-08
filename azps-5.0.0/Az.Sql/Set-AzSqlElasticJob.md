---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279591"
---
# <span data-ttu-id="4d83c-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="4d83c-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="4d83c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d83c-102">SYNOPSIS</span></span>
<span data-ttu-id="4d83c-103">İş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4d83c-103">Updates a job</span></span>

## <span data-ttu-id="4d83c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d83c-104">SYNTAX</span></span>

### <span data-ttu-id="4d83c-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4d83c-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d83c-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="4d83c-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d83c-107">Günlük</span><span class="sxs-lookup"><span data-stu-id="4d83c-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d83c-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4d83c-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d83c-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4d83c-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d83c-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4d83c-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d83c-111">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="4d83c-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d83c-112">Runonceusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="4d83c-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d83c-113">Recurringusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="4d83c-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d83c-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d83c-114">DESCRIPTION</span></span>
<span data-ttu-id="4d83c-115">Set-AzSqlElasticJob cmdlet bir işi güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="4d83c-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="4d83c-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d83c-116">EXAMPLES</span></span>

### <span data-ttu-id="4d83c-117">Örnek 1: Şu andan itibaren saat başı</span><span class="sxs-lookup"><span data-stu-id="4d83c-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="4d83c-118">İş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4d83c-118">Updates a job</span></span>

### <span data-ttu-id="4d83c-119">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="4d83c-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="4d83c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d83c-120">PARAMETERS</span></span>

### <span data-ttu-id="4d83c-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4d83c-121">-AgentName</span></span>
<span data-ttu-id="4d83c-122">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="4d83c-122">The agent name</span></span>

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

### <span data-ttu-id="4d83c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d83c-123">-DefaultProfile</span></span>
<span data-ttu-id="4d83c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4d83c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d83c-125">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="4d83c-125">-Description</span></span>
<span data-ttu-id="4d83c-126">İş açıklaması</span><span class="sxs-lookup"><span data-stu-id="4d83c-126">The job description</span></span>

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

### <span data-ttu-id="4d83c-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="4d83c-127">-Enable</span></span>
<span data-ttu-id="4d83c-128">Müşterinin bu işin etkinleştirilmesini istediğini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="4d83c-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="4d83c-129">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="4d83c-129">-EndTime</span></span>
<span data-ttu-id="4d83c-130">İş zamanlaması bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="4d83c-130">The job schedule end time</span></span>

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

### <span data-ttu-id="4d83c-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d83c-131">-InputObject</span></span>
<span data-ttu-id="4d83c-132">İş girişi nesnesi</span><span class="sxs-lookup"><span data-stu-id="4d83c-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d83c-133">-Interncount</span><span class="sxs-lookup"><span data-stu-id="4d83c-133">-IntervalCount</span></span>
<span data-ttu-id="4d83c-134">Yinelenen zamanlama aralığı sayısı</span><span class="sxs-lookup"><span data-stu-id="4d83c-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="4d83c-135">-Intertip türü</span><span class="sxs-lookup"><span data-stu-id="4d83c-135">-IntervalType</span></span>
<span data-ttu-id="4d83c-136">Yinelenen zamanlama aralığı türü; dakika, saat, gün, hafta, ay olabilir</span><span class="sxs-lookup"><span data-stu-id="4d83c-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="4d83c-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d83c-137">-Name</span></span>
<span data-ttu-id="4d83c-138">İş adı</span><span class="sxs-lookup"><span data-stu-id="4d83c-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d83c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d83c-139">-ResourceGroupName</span></span>
<span data-ttu-id="4d83c-140">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="4d83c-140">The resource group name</span></span>

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

### <span data-ttu-id="4d83c-141">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4d83c-141">-ResourceId</span></span>
<span data-ttu-id="4d83c-142">İş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="4d83c-142">The job resource id</span></span>

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

### <span data-ttu-id="4d83c-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="4d83c-143">-RunOnce</span></span>
<span data-ttu-id="4d83c-144">İş bir kez çalışacak şekilde işaretle</span><span class="sxs-lookup"><span data-stu-id="4d83c-144">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="4d83c-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4d83c-145">-ServerName</span></span>
<span data-ttu-id="4d83c-146">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="4d83c-146">The server name</span></span>

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

### <span data-ttu-id="4d83c-147">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="4d83c-147">-StartTime</span></span>
<span data-ttu-id="4d83c-148">İş zamanlaması başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="4d83c-148">The job schedule start time</span></span>

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

### <span data-ttu-id="4d83c-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d83c-149">-Confirm</span></span>
<span data-ttu-id="4d83c-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d83c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d83c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d83c-151">-WhatIf</span></span>
<span data-ttu-id="4d83c-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d83c-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d83c-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d83c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d83c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d83c-154">CommonParameters</span></span>
<span data-ttu-id="4d83c-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d83c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d83c-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4d83c-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d83c-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d83c-157">INPUTS</span></span>

### <span data-ttu-id="4d83c-158">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="4d83c-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4d83c-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d83c-159">OUTPUTS</span></span>

### <span data-ttu-id="4d83c-160">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="4d83c-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="4d83c-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d83c-161">NOTES</span></span>

## <span data-ttu-id="4d83c-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d83c-162">RELATED LINKS</span></span>
