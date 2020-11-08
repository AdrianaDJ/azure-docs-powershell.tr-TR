---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273878"
---
# <span data-ttu-id="3a8ed-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="3a8ed-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="3a8ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3a8ed-103">İş adımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3a8ed-103">Updates a job step</span></span>

## <span data-ttu-id="3a8ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a8ed-104">SYNTAX</span></span>

### <span data-ttu-id="3a8ed-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a8ed-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8ed-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="3a8ed-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a8ed-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="3a8ed-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a8ed-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a8ed-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8ed-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3a8ed-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8ed-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3a8ed-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8ed-111">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="3a8ed-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a8ed-112">Withremoveoutputusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="3a8ed-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a8ed-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3a8ed-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a8ed-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a8ed-114">DESCRIPTION</span></span>
<span data-ttu-id="3a8ed-115">Set-AzSqlElasticJobStep cmdlet bir iş adımını güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3a8ed-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="3a8ed-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a8ed-116">EXAMPLES</span></span>

### <span data-ttu-id="3a8ed-117">Örnek 1: iş için bir iş adımının hedef grubunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3a8ed-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="3a8ed-118">Örnek 2: iş için bir iş adımının T-SQL betiğini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3a8ed-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="3a8ed-119">İş adımını bir işten güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="3a8ed-119">Updates a job step from a job</span></span>

### <span data-ttu-id="3a8ed-120">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3a8ed-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="3a8ed-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a8ed-121">PARAMETERS</span></span>

### <span data-ttu-id="3a8ed-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-122">-AgentName</span></span>
<span data-ttu-id="3a8ed-123">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-123">The agent name</span></span>

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

### <span data-ttu-id="3a8ed-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="3a8ed-124">-CommandText</span></span>
<span data-ttu-id="3a8ed-125">Komut metni</span><span class="sxs-lookup"><span data-stu-id="3a8ed-125">The command text</span></span>

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

### <span data-ttu-id="3a8ed-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-126">-CredentialName</span></span>
<span data-ttu-id="3a8ed-127">Kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="3a8ed-127">The credential name</span></span>

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

### <span data-ttu-id="3a8ed-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a8ed-128">-DefaultProfile</span></span>
<span data-ttu-id="3a8ed-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a8ed-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a8ed-130">-Initialretryıntervalseconds</span><span class="sxs-lookup"><span data-stu-id="3a8ed-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="3a8ed-131">İlk yeniden deneme aralığı saniyeleri</span><span class="sxs-lookup"><span data-stu-id="3a8ed-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="3a8ed-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a8ed-132">-InputObject</span></span>
<span data-ttu-id="3a8ed-133">İş adımı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3a8ed-133">The job step object</span></span>

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

### <span data-ttu-id="3a8ed-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-134">-JobName</span></span>
<span data-ttu-id="3a8ed-135">İş adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-135">The job name</span></span>

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

### <span data-ttu-id="3a8ed-136">-Maximumretryıntervalseconds</span><span class="sxs-lookup"><span data-stu-id="3a8ed-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="3a8ed-137">Maksimum yeniden deneme aralığı saniyesi</span><span class="sxs-lookup"><span data-stu-id="3a8ed-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="3a8ed-138">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a8ed-138">-Name</span></span>
<span data-ttu-id="3a8ed-139">Adım adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-139">The step name</span></span>

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

### <span data-ttu-id="3a8ed-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-140">-OutputCredentialName</span></span>
<span data-ttu-id="3a8ed-141">Çıkış kimlik bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-141">The output credential name</span></span>

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

### <span data-ttu-id="3a8ed-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="3a8ed-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="3a8ed-143">Çıktı veritabanı nesnesi</span><span class="sxs-lookup"><span data-stu-id="3a8ed-143">The output database object</span></span>

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

### <span data-ttu-id="3a8ed-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="3a8ed-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="3a8ed-145">Çıkış veritabanı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3a8ed-145">The output database resource id</span></span>

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

### <span data-ttu-id="3a8ed-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-146">-OutputSchemaName</span></span>
<span data-ttu-id="3a8ed-147">Çıkış şemasının adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-147">The output schema name</span></span>

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

### <span data-ttu-id="3a8ed-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-148">-OutputTableName</span></span>
<span data-ttu-id="3a8ed-149">Çıkış tablosu adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-149">The output table name</span></span>

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

### <span data-ttu-id="3a8ed-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="3a8ed-150">-RemoveOutput</span></span>
<span data-ttu-id="3a8ed-151">Çıktının kaldırılıp çıkmayacağını belirten bayrak</span><span class="sxs-lookup"><span data-stu-id="3a8ed-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="3a8ed-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-152">-ResourceGroupName</span></span>
<span data-ttu-id="3a8ed-153">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-153">The resource group name</span></span>

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

### <span data-ttu-id="3a8ed-154">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a8ed-154">-ResourceId</span></span>
<span data-ttu-id="3a8ed-155">İş adımı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3a8ed-155">The job step resource id</span></span>

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

### <span data-ttu-id="3a8ed-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="3a8ed-156">-RetryAttempts</span></span>
<span data-ttu-id="3a8ed-157">Retry attemps</span><span class="sxs-lookup"><span data-stu-id="3a8ed-157">The retry attemps</span></span>

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

### <span data-ttu-id="3a8ed-158">-Retryınterbackoffmultiplier</span><span class="sxs-lookup"><span data-stu-id="3a8ed-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="3a8ed-159">Yeniden deneme aralığı geri alma çarpanı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="3a8ed-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-160">-ServerName</span></span>
<span data-ttu-id="3a8ed-161">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-161">The server name</span></span>

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

### <span data-ttu-id="3a8ed-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="3a8ed-162">-StepId</span></span>
<span data-ttu-id="3a8ed-163">Adım kimliği metni</span><span class="sxs-lookup"><span data-stu-id="3a8ed-163">The step id text</span></span>

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

### <span data-ttu-id="3a8ed-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="3a8ed-164">-TargetGroupName</span></span>
<span data-ttu-id="3a8ed-165">Hedef grup adı</span><span class="sxs-lookup"><span data-stu-id="3a8ed-165">The target group name</span></span>

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

### <span data-ttu-id="3a8ed-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="3a8ed-166">-TimeoutSeconds</span></span>
<span data-ttu-id="3a8ed-167">Zaman aşımı saniye</span><span class="sxs-lookup"><span data-stu-id="3a8ed-167">The timeout seconds</span></span>

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

### <span data-ttu-id="3a8ed-168">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a8ed-168">-Confirm</span></span>
<span data-ttu-id="3a8ed-169">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a8ed-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a8ed-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a8ed-170">-WhatIf</span></span>
<span data-ttu-id="3a8ed-171">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a8ed-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a8ed-172">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a8ed-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a8ed-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a8ed-173">CommonParameters</span></span>
<span data-ttu-id="3a8ed-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a8ed-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a8ed-175">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3a8ed-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a8ed-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a8ed-176">INPUTS</span></span>

### <span data-ttu-id="3a8ed-177">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="3a8ed-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="3a8ed-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a8ed-178">OUTPUTS</span></span>

### <span data-ttu-id="3a8ed-179">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="3a8ed-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="3a8ed-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a8ed-180">NOTES</span></span>

## <span data-ttu-id="3a8ed-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a8ed-181">RELATED LINKS</span></span>
