---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 25c9845d0912374baa0e2219c234f63abe381cfc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096752"
---
# <span data-ttu-id="48786-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="48786-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="48786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48786-102">SYNOPSIS</span></span>
<span data-ttu-id="48786-103">Projeye iş adımı ekler</span><span class="sxs-lookup"><span data-stu-id="48786-103">Adds a job step to a job</span></span>

## <span data-ttu-id="48786-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48786-104">SYNTAX</span></span>

### <span data-ttu-id="48786-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="48786-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48786-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="48786-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48786-107">Withoutputd</span><span class="sxs-lookup"><span data-stu-id="48786-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48786-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="48786-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48786-109">Withoutputvseçbusingparentobject</span><span class="sxs-lookup"><span data-stu-id="48786-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48786-110">Withoutputdbıdusingparentobject</span><span class="sxs-lookup"><span data-stu-id="48786-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48786-111">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="48786-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48786-112">Withoutputvseçbusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="48786-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48786-113">Withoutputdbıdusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="48786-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48786-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="48786-114">DESCRIPTION</span></span>
<span data-ttu-id="48786-115">Add-AzSqlElasticJobStep cmdlet, işe bir iş adımı ekler</span><span class="sxs-lookup"><span data-stu-id="48786-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="48786-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48786-116">EXAMPLES</span></span>

### <span data-ttu-id="48786-117">Örnek 1-işe bir adım ekler</span><span class="sxs-lookup"><span data-stu-id="48786-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="48786-118">Projeye iş adımı ekler</span><span class="sxs-lookup"><span data-stu-id="48786-118">Adds a job step to a job</span></span>

## <span data-ttu-id="48786-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48786-119">PARAMETERS</span></span>

### <span data-ttu-id="48786-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="48786-120">-AgentName</span></span>
<span data-ttu-id="48786-121">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="48786-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="48786-122">-CommandText</span></span>
<span data-ttu-id="48786-123">Komut metni</span><span class="sxs-lookup"><span data-stu-id="48786-123">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="48786-124">-CredentialName</span></span>
<span data-ttu-id="48786-125">Kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="48786-125">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48786-126">-DefaultProfile</span></span>
<span data-ttu-id="48786-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48786-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48786-128">-Initialretryıntervalseconds</span><span class="sxs-lookup"><span data-stu-id="48786-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="48786-129">İlk yeniden deneme aralığı saniyeleri</span><span class="sxs-lookup"><span data-stu-id="48786-129">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="48786-130">-JobName</span></span>
<span data-ttu-id="48786-131">İş adı</span><span class="sxs-lookup"><span data-stu-id="48786-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-132">-Maximumretryıntervalseconds</span><span class="sxs-lookup"><span data-stu-id="48786-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="48786-133">Maksimum yeniden deneme aralığı saniyesi</span><span class="sxs-lookup"><span data-stu-id="48786-133">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="48786-134">-Name</span></span>
<span data-ttu-id="48786-135">İş adımı adı</span><span class="sxs-lookup"><span data-stu-id="48786-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="48786-136">-OutputCredentialName</span></span>
<span data-ttu-id="48786-137">Çıkış kimlik bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="48786-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="48786-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="48786-139">Çıktı veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="48786-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="48786-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="48786-141">Çıkış veritabanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="48786-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="48786-142">-OutputSchemaName</span></span>
<span data-ttu-id="48786-143">Çıkış şemasının adı</span><span class="sxs-lookup"><span data-stu-id="48786-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="48786-144">-OutputTableName</span></span>
<span data-ttu-id="48786-145">Çıkış tablosu adı</span><span class="sxs-lookup"><span data-stu-id="48786-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="48786-146">-ParentObject</span></span>
<span data-ttu-id="48786-147">İş nesnesi</span><span class="sxs-lookup"><span data-stu-id="48786-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48786-148">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="48786-148">-ParentResourceId</span></span>
<span data-ttu-id="48786-149">İş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="48786-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48786-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48786-150">-ResourceGroupName</span></span>
<span data-ttu-id="48786-151">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="48786-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="48786-152">-RetryAttempts</span></span>
<span data-ttu-id="48786-153">Yeniden deneme girişimleri</span><span class="sxs-lookup"><span data-stu-id="48786-153">The retry attempts</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-154">-Retryınterbackoffmultiplier</span><span class="sxs-lookup"><span data-stu-id="48786-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="48786-155">Yeniden deneme aralığı geri çarpanı</span><span class="sxs-lookup"><span data-stu-id="48786-155">The retry interval back off multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="48786-156">-ServerName</span></span>
<span data-ttu-id="48786-157">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="48786-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="48786-158">-StepId</span></span>
<span data-ttu-id="48786-159">Adım kimliği</span><span class="sxs-lookup"><span data-stu-id="48786-159">The step id</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="48786-160">-TargetGroupName</span></span>
<span data-ttu-id="48786-161">Hedef grup adı</span><span class="sxs-lookup"><span data-stu-id="48786-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="48786-162">-TimeoutSeconds</span></span>
<span data-ttu-id="48786-163">Zaman aşımı saniye</span><span class="sxs-lookup"><span data-stu-id="48786-163">The time out seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48786-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="48786-164">-Confirm</span></span>
<span data-ttu-id="48786-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="48786-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48786-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48786-166">-WhatIf</span></span>
<span data-ttu-id="48786-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="48786-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48786-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="48786-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48786-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48786-169">CommonParameters</span></span>
<span data-ttu-id="48786-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48786-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48786-171">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="48786-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48786-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48786-172">INPUTS</span></span>

### <span data-ttu-id="48786-173">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="48786-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="48786-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48786-174">OUTPUTS</span></span>

### <span data-ttu-id="48786-175">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="48786-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="48786-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48786-176">NOTES</span></span>

## <span data-ttu-id="48786-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48786-177">RELATED LINKS</span></span>
