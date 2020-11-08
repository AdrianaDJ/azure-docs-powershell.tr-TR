---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266795"
---
# <span data-ttu-id="6f5b2-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="6f5b2-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="6f5b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f5b2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5b2-103">İş adımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="6f5b2-103">Removes the job step</span></span>

## <span data-ttu-id="6f5b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f5b2-104">SYNTAX</span></span>

### <span data-ttu-id="6f5b2-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6f5b2-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f5b2-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f5b2-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f5b2-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="6f5b2-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f5b2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f5b2-108">DESCRIPTION</span></span>
<span data-ttu-id="6f5b2-109">Remove-AzSqlElasticJobStep cmdlet 'i işten bir iş adımını kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="6f5b2-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="6f5b2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f5b2-110">EXAMPLES</span></span>

### <span data-ttu-id="6f5b2-111">Örnek 1: iş adımını bir işten çıkarır</span><span class="sxs-lookup"><span data-stu-id="6f5b2-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="6f5b2-112">İş adımını bir işten çıkarır</span><span class="sxs-lookup"><span data-stu-id="6f5b2-112">Removes a job step from a job</span></span>

### <span data-ttu-id="6f5b2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6f5b2-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="6f5b2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f5b2-114">PARAMETERS</span></span>

### <span data-ttu-id="6f5b2-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="6f5b2-115">-AgentName</span></span>
<span data-ttu-id="6f5b2-116">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="6f5b2-116">The agent name</span></span>

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

### <span data-ttu-id="6f5b2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5b2-117">-DefaultProfile</span></span>
<span data-ttu-id="6f5b2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f5b2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f5b2-119">-InputObject</span></span>
<span data-ttu-id="6f5b2-120">İş adımı girişi nesnesi</span><span class="sxs-lookup"><span data-stu-id="6f5b2-120">The job step input object</span></span>

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

### <span data-ttu-id="6f5b2-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="6f5b2-121">-JobName</span></span>
<span data-ttu-id="6f5b2-122">İş adı</span><span class="sxs-lookup"><span data-stu-id="6f5b2-122">The job name</span></span>

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

### <span data-ttu-id="6f5b2-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="6f5b2-123">-Name</span></span>
<span data-ttu-id="6f5b2-124">İş adımı adı</span><span class="sxs-lookup"><span data-stu-id="6f5b2-124">The job step name</span></span>

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

### <span data-ttu-id="6f5b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f5b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f5b2-126">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6f5b2-126">The resource group name</span></span>

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

### <span data-ttu-id="6f5b2-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="6f5b2-127">-ResourceId</span></span>
<span data-ttu-id="6f5b2-128">İş adımı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6f5b2-128">The job step resource id</span></span>

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

### <span data-ttu-id="6f5b2-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6f5b2-129">-ServerName</span></span>
<span data-ttu-id="6f5b2-130">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="6f5b2-130">The server name</span></span>

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

### <span data-ttu-id="6f5b2-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f5b2-131">-Confirm</span></span>
<span data-ttu-id="6f5b2-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f5b2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f5b2-133">-WhatIf</span></span>
<span data-ttu-id="6f5b2-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f5b2-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f5b2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5b2-136">CommonParameters</span></span>
<span data-ttu-id="6f5b2-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5b2-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6f5b2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5b2-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f5b2-139">INPUTS</span></span>

### <span data-ttu-id="6f5b2-140">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="6f5b2-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="6f5b2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f5b2-141">OUTPUTS</span></span>

### <span data-ttu-id="6f5b2-142">Microsoft. Azure. Commands. Sql. Elakjobs. model. Azuresqlelavejobstepmodel</span><span class="sxs-lookup"><span data-stu-id="6f5b2-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="6f5b2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f5b2-143">NOTES</span></span>

## <span data-ttu-id="6f5b2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f5b2-144">RELATED LINKS</span></span>
