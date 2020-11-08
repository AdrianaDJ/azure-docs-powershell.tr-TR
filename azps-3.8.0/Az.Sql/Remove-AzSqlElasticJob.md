---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJob.md
ms.openlocfilehash: 03f2e9af6b7225fd7622c03347bdea87c63453c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098669"
---
# <span data-ttu-id="dbdcd-101">Remove-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="dbdcd-101">Remove-AzSqlElasticJob</span></span>

## <span data-ttu-id="dbdcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbdcd-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdcd-103">İşi kaldırır</span><span class="sxs-lookup"><span data-stu-id="dbdcd-103">Removes a job</span></span>

## <span data-ttu-id="dbdcd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dbdcd-104">SYNTAX</span></span>

### <span data-ttu-id="dbdcd-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dbdcd-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbdcd-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="dbdcd-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbdcd-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="dbdcd-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJob [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbdcd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dbdcd-108">DESCRIPTION</span></span>
<span data-ttu-id="dbdcd-109">Remove-AzSqlElasticJob cmdlet 'i işi kaldırıyor</span><span class="sxs-lookup"><span data-stu-id="dbdcd-109">The Remove-AzSqlElasticJob cmdlet removes a job</span></span>

## <span data-ttu-id="dbdcd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dbdcd-110">EXAMPLES</span></span>

### <span data-ttu-id="dbdcd-111">Örnek 1-işi kaldırır</span><span class="sxs-lookup"><span data-stu-id="dbdcd-111">Example 1 - Removes a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="dbdcd-112">İşi kaldırır</span><span class="sxs-lookup"><span data-stu-id="dbdcd-112">Removes a job</span></span>

## <span data-ttu-id="dbdcd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dbdcd-113">PARAMETERS</span></span>

### <span data-ttu-id="dbdcd-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="dbdcd-114">-AgentName</span></span>
<span data-ttu-id="dbdcd-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="dbdcd-115">The agent name</span></span>

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

### <span data-ttu-id="dbdcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdcd-116">-DefaultProfile</span></span>
<span data-ttu-id="dbdcd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dbdcd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbdcd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dbdcd-118">-Force</span></span>
<span data-ttu-id="dbdcd-119">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="dbdcd-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="dbdcd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dbdcd-120">-InputObject</span></span>
<span data-ttu-id="dbdcd-121">İş girişi nesnesi</span><span class="sxs-lookup"><span data-stu-id="dbdcd-121">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbdcd-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="dbdcd-122">-Name</span></span>
<span data-ttu-id="dbdcd-123">İş adı</span><span class="sxs-lookup"><span data-stu-id="dbdcd-123">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbdcd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdcd-124">-ResourceGroupName</span></span>
<span data-ttu-id="dbdcd-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="dbdcd-125">The resource group name</span></span>

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

### <span data-ttu-id="dbdcd-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dbdcd-126">-ResourceId</span></span>
<span data-ttu-id="dbdcd-127">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="dbdcd-127">The agent resource id</span></span>

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

### <span data-ttu-id="dbdcd-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dbdcd-128">-ServerName</span></span>
<span data-ttu-id="dbdcd-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="dbdcd-129">The server name</span></span>

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

### <span data-ttu-id="dbdcd-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="dbdcd-130">-Confirm</span></span>
<span data-ttu-id="dbdcd-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dbdcd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbdcd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbdcd-132">-WhatIf</span></span>
<span data-ttu-id="dbdcd-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dbdcd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbdcd-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dbdcd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbdcd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdcd-135">CommonParameters</span></span>
<span data-ttu-id="dbdcd-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dbdcd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdcd-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dbdcd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdcd-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dbdcd-138">INPUTS</span></span>

### <span data-ttu-id="dbdcd-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="dbdcd-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="dbdcd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dbdcd-140">OUTPUTS</span></span>

### <span data-ttu-id="dbdcd-141">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="dbdcd-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="dbdcd-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dbdcd-142">NOTES</span></span>

## <span data-ttu-id="dbdcd-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dbdcd-143">RELATED LINKS</span></span>