---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 688926d05b56234ce11d4524afdcce326c5e09e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933634"
---
# <span data-ttu-id="db673-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="db673-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="db673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db673-102">SYNOPSIS</span></span>
<span data-ttu-id="db673-103">Bir veya daha fazla iş alır</span><span class="sxs-lookup"><span data-stu-id="db673-103">Gets one or more jobs</span></span>

## <span data-ttu-id="db673-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db673-104">SYNTAX</span></span>

### <span data-ttu-id="db673-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="db673-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db673-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="db673-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="db673-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="db673-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="db673-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="db673-108">DESCRIPTION</span></span>
<span data-ttu-id="db673-109">Get-AzSqlElasticJob cmdlet 'i bir veya daha fazla iş alır</span><span class="sxs-lookup"><span data-stu-id="db673-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="db673-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db673-110">EXAMPLES</span></span>

### <span data-ttu-id="db673-111">Örnek 1-iş alır</span><span class="sxs-lookup"><span data-stu-id="db673-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="db673-112">İş alır</span><span class="sxs-lookup"><span data-stu-id="db673-112">Gets a job</span></span>

## <span data-ttu-id="db673-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db673-113">PARAMETERS</span></span>

### <span data-ttu-id="db673-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="db673-114">-AgentName</span></span>
<span data-ttu-id="db673-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="db673-115">The agent name</span></span>

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

### <span data-ttu-id="db673-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db673-116">-DefaultProfile</span></span>
<span data-ttu-id="db673-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db673-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db673-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="db673-118">-Name</span></span>
<span data-ttu-id="db673-119">İş adı</span><span class="sxs-lookup"><span data-stu-id="db673-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db673-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="db673-120">-ParentObject</span></span>
<span data-ttu-id="db673-121">Aracı giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="db673-121">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db673-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="db673-122">-ParentResourceId</span></span>
<span data-ttu-id="db673-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="db673-123">The agent resource id</span></span>

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

### <span data-ttu-id="db673-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db673-124">-ResourceGroupName</span></span>
<span data-ttu-id="db673-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="db673-125">The resource group name</span></span>

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

### <span data-ttu-id="db673-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db673-126">-ServerName</span></span>
<span data-ttu-id="db673-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="db673-127">The server name</span></span>

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

### <span data-ttu-id="db673-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db673-128">CommonParameters</span></span>
<span data-ttu-id="db673-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db673-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db673-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="db673-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db673-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db673-131">INPUTS</span></span>

### <span data-ttu-id="db673-132">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="db673-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="db673-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db673-133">OUTPUTS</span></span>

### <span data-ttu-id="db673-134">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="db673-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="db673-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db673-135">NOTES</span></span>

## <span data-ttu-id="db673-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db673-136">RELATED LINKS</span></span>
