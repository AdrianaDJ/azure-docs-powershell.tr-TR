---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: c0ebc561a047ffe6a62722012fd7ecd3d42e472a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098666"
---
# <span data-ttu-id="503b8-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="503b8-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="503b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="503b8-102">SYNOPSIS</span></span>
<span data-ttu-id="503b8-103">İş adımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="503b8-103">Removes the job step</span></span>

## <span data-ttu-id="503b8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="503b8-104">SYNTAX</span></span>

### <span data-ttu-id="503b8-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="503b8-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="503b8-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="503b8-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="503b8-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="503b8-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="503b8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="503b8-108">DESCRIPTION</span></span>
<span data-ttu-id="503b8-109">Remove-AzSqlElasticJobStep cmdlet 'i işten bir iş adımını kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="503b8-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="503b8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="503b8-110">EXAMPLES</span></span>

### <span data-ttu-id="503b8-111">Örnek 1-işten bir iş adımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="503b8-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="503b8-112">İş adımını bir işten çıkarır</span><span class="sxs-lookup"><span data-stu-id="503b8-112">Removes a job step from a job</span></span>

## <span data-ttu-id="503b8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="503b8-113">PARAMETERS</span></span>

### <span data-ttu-id="503b8-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="503b8-114">-AgentName</span></span>
<span data-ttu-id="503b8-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="503b8-115">The agent name</span></span>

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

### <span data-ttu-id="503b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="503b8-116">-DefaultProfile</span></span>
<span data-ttu-id="503b8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="503b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="503b8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="503b8-118">-InputObject</span></span>
<span data-ttu-id="503b8-119">İş adımı girişi nesnesi</span><span class="sxs-lookup"><span data-stu-id="503b8-119">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="503b8-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="503b8-120">-JobName</span></span>
<span data-ttu-id="503b8-121">İş adı</span><span class="sxs-lookup"><span data-stu-id="503b8-121">The job name</span></span>

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

### <span data-ttu-id="503b8-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="503b8-122">-Name</span></span>
<span data-ttu-id="503b8-123">İş adımı adı</span><span class="sxs-lookup"><span data-stu-id="503b8-123">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="503b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="503b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="503b8-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="503b8-125">The resource group name</span></span>

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

### <span data-ttu-id="503b8-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="503b8-126">-ResourceId</span></span>
<span data-ttu-id="503b8-127">İş adımı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="503b8-127">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="503b8-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="503b8-128">-ServerName</span></span>
<span data-ttu-id="503b8-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="503b8-129">The server name</span></span>

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

### <span data-ttu-id="503b8-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="503b8-130">-Confirm</span></span>
<span data-ttu-id="503b8-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="503b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="503b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="503b8-132">-WhatIf</span></span>
<span data-ttu-id="503b8-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="503b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="503b8-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="503b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="503b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="503b8-135">CommonParameters</span></span>
<span data-ttu-id="503b8-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="503b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="503b8-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="503b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="503b8-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="503b8-138">INPUTS</span></span>

### <span data-ttu-id="503b8-139">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="503b8-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="503b8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="503b8-140">OUTPUTS</span></span>

### <span data-ttu-id="503b8-141">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="503b8-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="503b8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="503b8-142">NOTES</span></span>

## <span data-ttu-id="503b8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="503b8-143">RELATED LINKS</span></span>