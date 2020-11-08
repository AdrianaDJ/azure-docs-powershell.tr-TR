---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275208"
---
# <span data-ttu-id="ec4fb-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="ec4fb-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="ec4fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4fb-103">Projeye iş adımı ekler</span><span class="sxs-lookup"><span data-stu-id="ec4fb-103">Adds a job step to a job</span></span>

## <span data-ttu-id="ec4fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec4fb-104">SYNTAX</span></span>

### <span data-ttu-id="ec4fb-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec4fb-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec4fb-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="ec4fb-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec4fb-107">Withoutputd</span><span class="sxs-lookup"><span data-stu-id="ec4fb-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec4fb-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="ec4fb-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec4fb-109">Withoutputvseçbusingparentobject</span><span class="sxs-lookup"><span data-stu-id="ec4fb-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec4fb-110">Withoutputdbıdusingparentobject</span><span class="sxs-lookup"><span data-stu-id="ec4fb-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec4fb-111">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="ec4fb-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec4fb-112">Withoutputvseçbusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="ec4fb-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec4fb-113">Withoutputdbıdusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="ec4fb-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec4fb-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec4fb-114">DESCRIPTION</span></span>
<span data-ttu-id="ec4fb-115">Add-AzSqlElasticJobStep cmdlet, işe bir iş adımı ekler</span><span class="sxs-lookup"><span data-stu-id="ec4fb-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="ec4fb-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec4fb-116">EXAMPLES</span></span>

### <span data-ttu-id="ec4fb-117">Örnek 1: işe bir adım ekler</span><span class="sxs-lookup"><span data-stu-id="ec4fb-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="ec4fb-118">Projeye iş adımı ekler</span><span class="sxs-lookup"><span data-stu-id="ec4fb-118">Adds a job step to a job</span></span>

## <span data-ttu-id="ec4fb-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec4fb-119">PARAMETERS</span></span>

### <span data-ttu-id="ec4fb-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-120">-AgentName</span></span>
<span data-ttu-id="ec4fb-121">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-121">The agent name</span></span>

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

### <span data-ttu-id="ec4fb-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="ec4fb-122">-CommandText</span></span>
<span data-ttu-id="ec4fb-123">Komut metni</span><span class="sxs-lookup"><span data-stu-id="ec4fb-123">The command text</span></span>

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

### <span data-ttu-id="ec4fb-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-124">-CredentialName</span></span>
<span data-ttu-id="ec4fb-125">Kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="ec4fb-125">The credential name</span></span>

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

### <span data-ttu-id="ec4fb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4fb-126">-DefaultProfile</span></span>
<span data-ttu-id="ec4fb-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec4fb-128">-Initialretryıntervalseconds</span><span class="sxs-lookup"><span data-stu-id="ec4fb-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="ec4fb-129">İlk yeniden deneme aralığı saniyeleri</span><span class="sxs-lookup"><span data-stu-id="ec4fb-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="ec4fb-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-130">-JobName</span></span>
<span data-ttu-id="ec4fb-131">İş adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-131">The job name</span></span>

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

### <span data-ttu-id="ec4fb-132">-Maximumretryıntervalseconds</span><span class="sxs-lookup"><span data-stu-id="ec4fb-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="ec4fb-133">Maksimum yeniden deneme aralığı saniyesi</span><span class="sxs-lookup"><span data-stu-id="ec4fb-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="ec4fb-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec4fb-134">-Name</span></span>
<span data-ttu-id="ec4fb-135">İş adımı adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-135">The job step name</span></span>

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

### <span data-ttu-id="ec4fb-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-136">-OutputCredentialName</span></span>
<span data-ttu-id="ec4fb-137">Çıkış kimlik bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-137">The output credential name</span></span>

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

### <span data-ttu-id="ec4fb-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ec4fb-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="ec4fb-139">Çıktı veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="ec4fb-139">The output database object</span></span>

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

### <span data-ttu-id="ec4fb-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="ec4fb-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="ec4fb-141">Çıkış veritabanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ec4fb-141">The output database resource id</span></span>

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

### <span data-ttu-id="ec4fb-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-142">-OutputSchemaName</span></span>
<span data-ttu-id="ec4fb-143">Çıkış şemasının adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-143">The output schema name</span></span>

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

### <span data-ttu-id="ec4fb-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-144">-OutputTableName</span></span>
<span data-ttu-id="ec4fb-145">Çıkış tablosu adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-145">The output table name</span></span>

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

### <span data-ttu-id="ec4fb-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ec4fb-146">-ParentObject</span></span>
<span data-ttu-id="ec4fb-147">İş nesnesi</span><span class="sxs-lookup"><span data-stu-id="ec4fb-147">The job object</span></span>

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

### <span data-ttu-id="ec4fb-148">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="ec4fb-148">-ParentResourceId</span></span>
<span data-ttu-id="ec4fb-149">İş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="ec4fb-149">The job resource id</span></span>

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

### <span data-ttu-id="ec4fb-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-150">-ResourceGroupName</span></span>
<span data-ttu-id="ec4fb-151">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-151">The resource group name</span></span>

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

### <span data-ttu-id="ec4fb-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="ec4fb-152">-RetryAttempts</span></span>
<span data-ttu-id="ec4fb-153">Yeniden deneme girişimleri</span><span class="sxs-lookup"><span data-stu-id="ec4fb-153">The retry attempts</span></span>

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

### <span data-ttu-id="ec4fb-154">-Retryınterbackoffmultiplier</span><span class="sxs-lookup"><span data-stu-id="ec4fb-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="ec4fb-155">Yeniden deneme aralığı geri çarpanı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="ec4fb-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-156">-ServerName</span></span>
<span data-ttu-id="ec4fb-157">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-157">The server name</span></span>

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

### <span data-ttu-id="ec4fb-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="ec4fb-158">-StepId</span></span>
<span data-ttu-id="ec4fb-159">Adım kimliği</span><span class="sxs-lookup"><span data-stu-id="ec4fb-159">The step id</span></span>

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

### <span data-ttu-id="ec4fb-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="ec4fb-160">-TargetGroupName</span></span>
<span data-ttu-id="ec4fb-161">Hedef grup adı</span><span class="sxs-lookup"><span data-stu-id="ec4fb-161">The target group name</span></span>

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

### <span data-ttu-id="ec4fb-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="ec4fb-162">-TimeoutSeconds</span></span>
<span data-ttu-id="ec4fb-163">Zaman aşımı saniye</span><span class="sxs-lookup"><span data-stu-id="ec4fb-163">The time out seconds</span></span>

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

### <span data-ttu-id="ec4fb-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec4fb-164">-Confirm</span></span>
<span data-ttu-id="ec4fb-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec4fb-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4fb-166">-WhatIf</span></span>
<span data-ttu-id="ec4fb-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec4fb-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec4fb-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4fb-169">CommonParameters</span></span>
<span data-ttu-id="ec4fb-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4fb-171">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec4fb-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4fb-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec4fb-172">INPUTS</span></span>

### <span data-ttu-id="ec4fb-173">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="ec4fb-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="ec4fb-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec4fb-174">OUTPUTS</span></span>

### <span data-ttu-id="ec4fb-175">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="ec4fb-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="ec4fb-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec4fb-176">NOTES</span></span>

## <span data-ttu-id="ec4fb-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec4fb-177">RELATED LINKS</span></span>
