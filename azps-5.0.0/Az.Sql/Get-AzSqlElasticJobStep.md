---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275838"
---
# <span data-ttu-id="0679b-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="0679b-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="0679b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0679b-102">SYNOPSIS</span></span>
<span data-ttu-id="0679b-103">Bir veya daha fazla iş adımını alır</span><span class="sxs-lookup"><span data-stu-id="0679b-103">Gets one or more job steps</span></span>

## <span data-ttu-id="0679b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0679b-104">SYNTAX</span></span>

### <span data-ttu-id="0679b-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0679b-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0679b-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="0679b-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0679b-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="0679b-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0679b-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="0679b-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0679b-109">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="0679b-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0679b-110">Getversionusingparentresourceıd</span><span class="sxs-lookup"><span data-stu-id="0679b-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0679b-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="0679b-111">DESCRIPTION</span></span>
<span data-ttu-id="0679b-112">Get-AzSqlElasticJobStep cmdlet bir işten bir veya daha fazla iş adımını alır</span><span class="sxs-lookup"><span data-stu-id="0679b-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="0679b-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0679b-113">EXAMPLES</span></span>

### <span data-ttu-id="0679b-114">Örnek 1: bir işten iş adımını alır</span><span class="sxs-lookup"><span data-stu-id="0679b-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="0679b-115">İş için bir iş adımını alır</span><span class="sxs-lookup"><span data-stu-id="0679b-115">Gets a job step from a job</span></span>

## <span data-ttu-id="0679b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0679b-116">PARAMETERS</span></span>

### <span data-ttu-id="0679b-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="0679b-117">-AgentName</span></span>
<span data-ttu-id="0679b-118">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="0679b-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0679b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0679b-119">-DefaultProfile</span></span>
<span data-ttu-id="0679b-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0679b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0679b-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="0679b-121">-JobName</span></span>
<span data-ttu-id="0679b-122">İş adı</span><span class="sxs-lookup"><span data-stu-id="0679b-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0679b-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="0679b-123">-Name</span></span>
<span data-ttu-id="0679b-124">İş adımı adı</span><span class="sxs-lookup"><span data-stu-id="0679b-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0679b-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0679b-125">-ParentObject</span></span>
<span data-ttu-id="0679b-126">İş girişi nesnesi</span><span class="sxs-lookup"><span data-stu-id="0679b-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0679b-127">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="0679b-127">-ParentResourceId</span></span>
<span data-ttu-id="0679b-128">İş kaynağı kimliği</span><span class="sxs-lookup"><span data-stu-id="0679b-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0679b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0679b-129">-ResourceGroupName</span></span>
<span data-ttu-id="0679b-130">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0679b-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0679b-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0679b-131">-ServerName</span></span>
<span data-ttu-id="0679b-132">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="0679b-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0679b-133">-Version</span><span class="sxs-lookup"><span data-stu-id="0679b-133">-Version</span></span>
<span data-ttu-id="0679b-134">İş adımı adı</span><span class="sxs-lookup"><span data-stu-id="0679b-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0679b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0679b-135">CommonParameters</span></span>
<span data-ttu-id="0679b-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0679b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0679b-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0679b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0679b-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0679b-138">INPUTS</span></span>

### <span data-ttu-id="0679b-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="0679b-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="0679b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0679b-140">OUTPUTS</span></span>

### <span data-ttu-id="0679b-141">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="0679b-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="0679b-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0679b-142">NOTES</span></span>

## <span data-ttu-id="0679b-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0679b-143">RELATED LINKS</span></span>
