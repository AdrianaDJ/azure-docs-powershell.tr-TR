---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275841"
---
# <span data-ttu-id="c5b53-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="c5b53-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="c5b53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b53-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b53-103">Azure SQL esnek Iş aracısını alır</span><span class="sxs-lookup"><span data-stu-id="c5b53-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="c5b53-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5b53-104">SYNTAX</span></span>

### <span data-ttu-id="c5b53-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5b53-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5b53-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c5b53-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5b53-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="c5b53-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5b53-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5b53-108">DESCRIPTION</span></span>
<span data-ttu-id="c5b53-109">Get-AzSqlElasticJobAgent cmdlet bir veya daha fazla esnek Iş Aracısı alır</span><span class="sxs-lookup"><span data-stu-id="c5b53-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="c5b53-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5b53-110">EXAMPLES</span></span>

### <span data-ttu-id="c5b53-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c5b53-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="c5b53-112">Esnek bir Iş Aracısı alır</span><span class="sxs-lookup"><span data-stu-id="c5b53-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="c5b53-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5b53-113">PARAMETERS</span></span>

### <span data-ttu-id="c5b53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b53-114">-DefaultProfile</span></span>
<span data-ttu-id="c5b53-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5b53-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5b53-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5b53-116">-Name</span></span>
<span data-ttu-id="c5b53-117">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="c5b53-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b53-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c5b53-118">-ParentObject</span></span>
<span data-ttu-id="c5b53-119">Sunucu giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="c5b53-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b53-120">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="c5b53-120">-ParentResourceId</span></span>
<span data-ttu-id="c5b53-121">Sunucu kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c5b53-121">The server resource id</span></span>

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

### <span data-ttu-id="c5b53-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b53-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5b53-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c5b53-123">The resource group name</span></span>

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

### <span data-ttu-id="c5b53-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c5b53-124">-ServerName</span></span>
<span data-ttu-id="c5b53-125">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="c5b53-125">The server name</span></span>

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

### <span data-ttu-id="c5b53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b53-126">CommonParameters</span></span>
<span data-ttu-id="c5b53-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5b53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b53-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c5b53-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b53-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5b53-129">INPUTS</span></span>

### <span data-ttu-id="c5b53-130">Microsoft. Azure. Commands. Sql. Server. model. Azuressqlservermodel</span><span class="sxs-lookup"><span data-stu-id="c5b53-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c5b53-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5b53-131">OUTPUTS</span></span>

### <span data-ttu-id="c5b53-132">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="c5b53-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="c5b53-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5b53-133">NOTES</span></span>

## <span data-ttu-id="c5b53-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5b53-134">RELATED LINKS</span></span>
