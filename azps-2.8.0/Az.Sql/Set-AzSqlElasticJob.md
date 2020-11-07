---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 04f182cb410e77a9ca61aa6f80da14c08e517406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933710"
---
# <span data-ttu-id="995b2-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="995b2-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="995b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="995b2-102">SYNOPSIS</span></span>
<span data-ttu-id="995b2-103">İş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="995b2-103">Updates a job</span></span>

## <span data-ttu-id="995b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="995b2-104">SYNTAX</span></span>

### <span data-ttu-id="995b2-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="995b2-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="995b2-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="995b2-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="995b2-107">Günlük</span><span class="sxs-lookup"><span data-stu-id="995b2-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="995b2-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="995b2-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="995b2-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="995b2-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="995b2-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="995b2-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="995b2-111">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="995b2-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="995b2-112">Runonceusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="995b2-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="995b2-113">Recurringusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="995b2-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="995b2-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="995b2-114">DESCRIPTION</span></span>
<span data-ttu-id="995b2-115">Set-AzSqlElasticJob cmdlet bir işi güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="995b2-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="995b2-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="995b2-116">EXAMPLES</span></span>

### <span data-ttu-id="995b2-117">Örnek 1-Şu andan itibaren bir saat sonra başlayacak bir iş güncelleştirir ve 1 saatte bir yineler</span><span class="sxs-lookup"><span data-stu-id="995b2-117">Example 1 - Updates a job to start an hour from now and repeat every 1 hour</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="995b2-118">İş güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="995b2-118">Updates a job</span></span>

## <span data-ttu-id="995b2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="995b2-119">PARAMETERS</span></span>

### <span data-ttu-id="995b2-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="995b2-120">-AgentName</span></span>
<span data-ttu-id="995b2-121">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="995b2-121">The agent name</span></span>

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

### <span data-ttu-id="995b2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="995b2-122">-DefaultProfile</span></span>
<span data-ttu-id="995b2-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="995b2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="995b2-124">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="995b2-124">-Description</span></span>
<span data-ttu-id="995b2-125">İş açıklaması</span><span class="sxs-lookup"><span data-stu-id="995b2-125">The job description</span></span>

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

### <span data-ttu-id="995b2-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="995b2-126">-Enable</span></span>
<span data-ttu-id="995b2-127">Müşterinin bu işin etkinleştirilmesini istediğini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="995b2-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="995b2-128">-Bitişsaati</span><span class="sxs-lookup"><span data-stu-id="995b2-128">-EndTime</span></span>
<span data-ttu-id="995b2-129">İş zamanlaması bitiş zamanı</span><span class="sxs-lookup"><span data-stu-id="995b2-129">The job schedule end time</span></span>

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

### <span data-ttu-id="995b2-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="995b2-130">-InputObject</span></span>
<span data-ttu-id="995b2-131">İş girişi nesnesi</span><span class="sxs-lookup"><span data-stu-id="995b2-131">The job input object</span></span>

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

### <span data-ttu-id="995b2-132">-Interncount</span><span class="sxs-lookup"><span data-stu-id="995b2-132">-IntervalCount</span></span>
<span data-ttu-id="995b2-133">Yinelenen zamanlama aralığı sayısı</span><span class="sxs-lookup"><span data-stu-id="995b2-133">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="995b2-134">-Intertip türü</span><span class="sxs-lookup"><span data-stu-id="995b2-134">-IntervalType</span></span>
<span data-ttu-id="995b2-135">Yinelenen zamanlama aralığı türü; dakika, saat, gün, hafta, ay olabilir</span><span class="sxs-lookup"><span data-stu-id="995b2-135">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="995b2-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="995b2-136">-Name</span></span>
<span data-ttu-id="995b2-137">İş adı</span><span class="sxs-lookup"><span data-stu-id="995b2-137">The job name</span></span>

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

### <span data-ttu-id="995b2-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="995b2-138">-ResourceGroupName</span></span>
<span data-ttu-id="995b2-139">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="995b2-139">The resource group name</span></span>

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

### <span data-ttu-id="995b2-140">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="995b2-140">-ResourceId</span></span>
<span data-ttu-id="995b2-141">İş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="995b2-141">The job resource id</span></span>

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

### <span data-ttu-id="995b2-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="995b2-142">-RunOnce</span></span>
<span data-ttu-id="995b2-143">İş bir kez çalışacak şekilde işaretle</span><span class="sxs-lookup"><span data-stu-id="995b2-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="995b2-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="995b2-144">-ServerName</span></span>
<span data-ttu-id="995b2-145">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="995b2-145">The server name</span></span>

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

### <span data-ttu-id="995b2-146">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="995b2-146">-StartTime</span></span>
<span data-ttu-id="995b2-147">İş zamanlaması başlangıç saati</span><span class="sxs-lookup"><span data-stu-id="995b2-147">The job schedule start time</span></span>

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

### <span data-ttu-id="995b2-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="995b2-148">-Confirm</span></span>
<span data-ttu-id="995b2-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="995b2-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="995b2-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="995b2-150">-WhatIf</span></span>
<span data-ttu-id="995b2-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="995b2-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="995b2-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="995b2-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="995b2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="995b2-153">CommonParameters</span></span>
<span data-ttu-id="995b2-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="995b2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="995b2-155">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="995b2-155">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="995b2-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="995b2-156">INPUTS</span></span>

### <span data-ttu-id="995b2-157">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="995b2-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="995b2-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="995b2-158">OUTPUTS</span></span>

### <span data-ttu-id="995b2-159">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="995b2-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="995b2-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="995b2-160">NOTES</span></span>

## <span data-ttu-id="995b2-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="995b2-161">RELATED LINKS</span></span>
