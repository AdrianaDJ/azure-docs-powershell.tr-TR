---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319789"
---
# <span data-ttu-id="7e273-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="7e273-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="7e273-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e273-102">SYNOPSIS</span></span>
<span data-ttu-id="7e273-103">Bir veya daha fazla iş hedef grubunu alır</span><span class="sxs-lookup"><span data-stu-id="7e273-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="7e273-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7e273-104">SYNTAX</span></span>

### <span data-ttu-id="7e273-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7e273-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e273-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7e273-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e273-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="7e273-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e273-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7e273-108">DESCRIPTION</span></span>
<span data-ttu-id="7e273-109">Get-AzSqlElasticJobTargetGroup cmdlet 'i hedef grubu alır ve hedefler</span><span class="sxs-lookup"><span data-stu-id="7e273-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="7e273-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7e273-110">EXAMPLES</span></span>

### <span data-ttu-id="7e273-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7e273-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="7e273-112">Hedef grubu ve hedeflerini alır</span><span class="sxs-lookup"><span data-stu-id="7e273-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="7e273-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7e273-113">PARAMETERS</span></span>

### <span data-ttu-id="7e273-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7e273-114">-AgentName</span></span>
<span data-ttu-id="7e273-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="7e273-115">The agent name</span></span>

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

### <span data-ttu-id="7e273-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e273-116">-DefaultProfile</span></span>
<span data-ttu-id="7e273-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7e273-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e273-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="7e273-118">-Name</span></span>
<span data-ttu-id="7e273-119">Hedef grup adı</span><span class="sxs-lookup"><span data-stu-id="7e273-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e273-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7e273-120">-ParentObject</span></span>
<span data-ttu-id="7e273-121">Aracı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7e273-121">The agent object</span></span>

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

### <span data-ttu-id="7e273-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7e273-122">-ParentResourceId</span></span>
<span data-ttu-id="7e273-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7e273-123">The agent resource id</span></span>

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

### <span data-ttu-id="7e273-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e273-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e273-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="7e273-125">The resource group name</span></span>

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

### <span data-ttu-id="7e273-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7e273-126">-ServerName</span></span>
<span data-ttu-id="7e273-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="7e273-127">The server name</span></span>

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

### <span data-ttu-id="7e273-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e273-128">CommonParameters</span></span>
<span data-ttu-id="7e273-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7e273-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e273-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7e273-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e273-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7e273-131">INPUTS</span></span>

### <span data-ttu-id="7e273-132">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="7e273-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="7e273-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7e273-133">OUTPUTS</span></span>

### <span data-ttu-id="7e273-134">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobtargetgroupmodel</span><span class="sxs-lookup"><span data-stu-id="7e273-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="7e273-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7e273-135">NOTES</span></span>

## <span data-ttu-id="7e273-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7e273-136">RELATED LINKS</span></span>
