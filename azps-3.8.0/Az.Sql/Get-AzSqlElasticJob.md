---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 60dac0ad09f30f339da82d84cf6200a44fe11859
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096993"
---
# <span data-ttu-id="a312c-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="a312c-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="a312c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a312c-102">SYNOPSIS</span></span>
<span data-ttu-id="a312c-103">Bir veya daha fazla iş alır</span><span class="sxs-lookup"><span data-stu-id="a312c-103">Gets one or more jobs</span></span>

## <span data-ttu-id="a312c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a312c-104">SYNTAX</span></span>

### <span data-ttu-id="a312c-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a312c-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a312c-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a312c-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a312c-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="a312c-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a312c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a312c-108">DESCRIPTION</span></span>
<span data-ttu-id="a312c-109">Get-AzSqlElasticJob cmdlet 'i bir veya daha fazla iş alır</span><span class="sxs-lookup"><span data-stu-id="a312c-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="a312c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a312c-110">EXAMPLES</span></span>

### <span data-ttu-id="a312c-111">Örnek 1-iş alır</span><span class="sxs-lookup"><span data-stu-id="a312c-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="a312c-112">İş alır</span><span class="sxs-lookup"><span data-stu-id="a312c-112">Gets a job</span></span>

## <span data-ttu-id="a312c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a312c-113">PARAMETERS</span></span>

### <span data-ttu-id="a312c-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a312c-114">-AgentName</span></span>
<span data-ttu-id="a312c-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="a312c-115">The agent name</span></span>

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

### <span data-ttu-id="a312c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a312c-116">-DefaultProfile</span></span>
<span data-ttu-id="a312c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a312c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a312c-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a312c-118">-Name</span></span>
<span data-ttu-id="a312c-119">İş adı</span><span class="sxs-lookup"><span data-stu-id="a312c-119">The job name</span></span>

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

### <span data-ttu-id="a312c-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a312c-120">-ParentObject</span></span>
<span data-ttu-id="a312c-121">Aracı giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="a312c-121">The agent input object</span></span>

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

### <span data-ttu-id="a312c-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="a312c-122">-ParentResourceId</span></span>
<span data-ttu-id="a312c-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a312c-123">The agent resource id</span></span>

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

### <span data-ttu-id="a312c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a312c-124">-ResourceGroupName</span></span>
<span data-ttu-id="a312c-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a312c-125">The resource group name</span></span>

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

### <span data-ttu-id="a312c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a312c-126">-ServerName</span></span>
<span data-ttu-id="a312c-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="a312c-127">The server name</span></span>

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

### <span data-ttu-id="a312c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a312c-128">CommonParameters</span></span>
<span data-ttu-id="a312c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a312c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a312c-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a312c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a312c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a312c-131">INPUTS</span></span>

### <span data-ttu-id="a312c-132">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="a312c-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a312c-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a312c-133">OUTPUTS</span></span>

### <span data-ttu-id="a312c-134">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobmodel</span><span class="sxs-lookup"><span data-stu-id="a312c-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="a312c-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a312c-135">NOTES</span></span>

## <span data-ttu-id="a312c-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a312c-136">RELATED LINKS</span></span>
