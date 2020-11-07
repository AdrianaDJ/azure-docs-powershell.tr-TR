---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: f39554dacdaabfc42fe44d55a7f3034c1c8b54df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938096"
---
# <span data-ttu-id="7e982-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="7e982-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="7e982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e982-102">SYNOPSIS</span></span>
<span data-ttu-id="7e982-103">İş adımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7e982-103">Updates a job step</span></span>

## <span data-ttu-id="7e982-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e982-104">SYNTAX</span></span>

### <span data-ttu-id="7e982-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e982-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e982-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="7e982-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e982-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="7e982-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e982-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7e982-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e982-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7e982-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e982-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="7e982-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e982-111">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="7e982-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e982-112">Withremoveoutputusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7e982-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e982-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7e982-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e982-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e982-114">DESCRIPTION</span></span>
<span data-ttu-id="7e982-115">Set-AzSqlElasticJobStep cmdlet bir iş adımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7e982-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="7e982-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e982-116">EXAMPLES</span></span>

### <span data-ttu-id="7e982-117">Örnek 1-iş için bir iş adımının hedef grubunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7e982-117">Example 1 - Updates a job step's target group for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="7e982-118">Örnek 2-iş için bir iş adımının T-SQL betiğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7e982-118">Example 2 - Updates a job step's T-SQL script for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="7e982-119">İş adımını bir işten güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="7e982-119">Updates a job step from a job</span></span>

## <span data-ttu-id="7e982-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e982-120">PARAMETERS</span></span>

### <span data-ttu-id="7e982-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7e982-121">-AgentName</span></span>
<span data-ttu-id="7e982-122">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="7e982-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-123">-CommandText</span><span class="sxs-lookup"><span data-stu-id="7e982-123">-CommandText</span></span>
<span data-ttu-id="7e982-124">Komut metni</span><span class="sxs-lookup"><span data-stu-id="7e982-124">The command text</span></span>

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

### <span data-ttu-id="7e982-125">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="7e982-125">-CredentialName</span></span>
<span data-ttu-id="7e982-126">Kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="7e982-126">The credential name</span></span>

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

### <span data-ttu-id="7e982-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e982-127">-DefaultProfile</span></span>
<span data-ttu-id="7e982-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e982-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e982-129">-Initialretryıntervalseconds</span><span class="sxs-lookup"><span data-stu-id="7e982-129">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="7e982-130">İlk yeniden deneme aralığı saniyeleri</span><span class="sxs-lookup"><span data-stu-id="7e982-130">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="7e982-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e982-131">-InputObject</span></span>
<span data-ttu-id="7e982-132">İş adımı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7e982-132">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="7e982-133">-JobName</span></span>
<span data-ttu-id="7e982-134">İş adı</span><span class="sxs-lookup"><span data-stu-id="7e982-134">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-135">-Maximumretryıntervalseconds</span><span class="sxs-lookup"><span data-stu-id="7e982-135">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="7e982-136">Maksimum yeniden deneme aralığı saniyesi</span><span class="sxs-lookup"><span data-stu-id="7e982-136">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="7e982-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e982-137">-Name</span></span>
<span data-ttu-id="7e982-138">Adım adı</span><span class="sxs-lookup"><span data-stu-id="7e982-138">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-139">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="7e982-139">-OutputCredentialName</span></span>
<span data-ttu-id="7e982-140">Çıkış kimlik bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="7e982-140">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-141">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="7e982-141">-OutputDatabaseObject</span></span>
<span data-ttu-id="7e982-142">Çıktı veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7e982-142">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-143">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="7e982-143">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="7e982-144">Çıkış veritabanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7e982-144">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-145">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="7e982-145">-OutputSchemaName</span></span>
<span data-ttu-id="7e982-146">Çıkış şemasının adı</span><span class="sxs-lookup"><span data-stu-id="7e982-146">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-147">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="7e982-147">-OutputTableName</span></span>
<span data-ttu-id="7e982-148">Çıkış tablosu adı</span><span class="sxs-lookup"><span data-stu-id="7e982-148">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-149">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="7e982-149">-RemoveOutput</span></span>
<span data-ttu-id="7e982-150">Çıktının kaldırılıp çıkmayacağını belirten bayrak</span><span class="sxs-lookup"><span data-stu-id="7e982-150">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e982-151">-ResourceGroupName</span></span>
<span data-ttu-id="7e982-152">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7e982-152">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-153">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7e982-153">-ResourceId</span></span>
<span data-ttu-id="7e982-154">İş adımı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7e982-154">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-155">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="7e982-155">-RetryAttempts</span></span>
<span data-ttu-id="7e982-156">Retry attemps</span><span class="sxs-lookup"><span data-stu-id="7e982-156">The retry attemps</span></span>

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

### <span data-ttu-id="7e982-157">-Retryınterbackoffmultiplier</span><span class="sxs-lookup"><span data-stu-id="7e982-157">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="7e982-158">Yeniden deneme aralığı geri alma çarpanı</span><span class="sxs-lookup"><span data-stu-id="7e982-158">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="7e982-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e982-159">-ServerName</span></span>
<span data-ttu-id="7e982-160">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="7e982-160">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e982-161">-StepId</span><span class="sxs-lookup"><span data-stu-id="7e982-161">-StepId</span></span>
<span data-ttu-id="7e982-162">Adım kimliği metni</span><span class="sxs-lookup"><span data-stu-id="7e982-162">The step id text</span></span>

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

### <span data-ttu-id="7e982-163">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="7e982-163">-TargetGroupName</span></span>
<span data-ttu-id="7e982-164">Hedef grup adı</span><span class="sxs-lookup"><span data-stu-id="7e982-164">The target group name</span></span>

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

### <span data-ttu-id="7e982-165">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="7e982-165">-TimeoutSeconds</span></span>
<span data-ttu-id="7e982-166">Zaman aşımı saniye</span><span class="sxs-lookup"><span data-stu-id="7e982-166">The timeout seconds</span></span>

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

### <span data-ttu-id="7e982-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="7e982-167">-Confirm</span></span>
<span data-ttu-id="7e982-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7e982-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e982-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e982-169">-WhatIf</span></span>
<span data-ttu-id="7e982-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7e982-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e982-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7e982-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e982-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e982-172">CommonParameters</span></span>
<span data-ttu-id="7e982-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e982-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e982-174">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e982-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e982-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e982-175">INPUTS</span></span>

### <span data-ttu-id="7e982-176">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="7e982-176">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="7e982-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e982-177">OUTPUTS</span></span>

### <span data-ttu-id="7e982-178">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="7e982-178">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="7e982-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e982-179">NOTES</span></span>

## <span data-ttu-id="7e982-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e982-180">RELATED LINKS</span></span>
