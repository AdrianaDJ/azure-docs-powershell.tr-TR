---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: a20de2c2431e1ab6aea5da4d6dd61e6c745a3c56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097941"
---
# <span data-ttu-id="96653-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="96653-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="96653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96653-102">SYNOPSIS</span></span>
<span data-ttu-id="96653-103">Hedef grubu kaldırır</span><span class="sxs-lookup"><span data-stu-id="96653-103">Removes the target group</span></span>

## <span data-ttu-id="96653-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96653-104">SYNTAX</span></span>

### <span data-ttu-id="96653-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="96653-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96653-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="96653-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96653-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="96653-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96653-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="96653-108">DESCRIPTION</span></span>
<span data-ttu-id="96653-109">Remove-AzSqlElasticJobTargetGroup cmdlet 'inin hedefi</span><span class="sxs-lookup"><span data-stu-id="96653-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="96653-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96653-110">EXAMPLES</span></span>

### <span data-ttu-id="96653-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="96653-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="96653-112">Hedef grubu kaldırır ve hedefleri</span><span class="sxs-lookup"><span data-stu-id="96653-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="96653-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96653-113">PARAMETERS</span></span>

### <span data-ttu-id="96653-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="96653-114">-AgentName</span></span>
<span data-ttu-id="96653-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="96653-115">The agent name</span></span>

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

### <span data-ttu-id="96653-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96653-116">-DefaultProfile</span></span>
<span data-ttu-id="96653-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96653-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96653-118">-Force</span><span class="sxs-lookup"><span data-stu-id="96653-118">-Force</span></span>
<span data-ttu-id="96653-119">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="96653-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="96653-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96653-120">-InputObject</span></span>
<span data-ttu-id="96653-121">Hedef Grup nesnesi</span><span class="sxs-lookup"><span data-stu-id="96653-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96653-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="96653-122">-Name</span></span>
<span data-ttu-id="96653-123">Hedef grup adı</span><span class="sxs-lookup"><span data-stu-id="96653-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96653-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96653-124">-ResourceGroupName</span></span>
<span data-ttu-id="96653-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="96653-125">The resource group name</span></span>

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

### <span data-ttu-id="96653-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="96653-126">-ResourceId</span></span>
<span data-ttu-id="96653-127">Hedef Grup kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="96653-127">The target group resource id</span></span>

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

### <span data-ttu-id="96653-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96653-128">-ServerName</span></span>
<span data-ttu-id="96653-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="96653-129">The server name</span></span>

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

### <span data-ttu-id="96653-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="96653-130">-Confirm</span></span>
<span data-ttu-id="96653-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96653-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96653-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96653-132">-WhatIf</span></span>
<span data-ttu-id="96653-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96653-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96653-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96653-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96653-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96653-135">CommonParameters</span></span>
<span data-ttu-id="96653-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96653-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96653-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="96653-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96653-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96653-138">INPUTS</span></span>

### <span data-ttu-id="96653-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobtargetgroupmodel</span><span class="sxs-lookup"><span data-stu-id="96653-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="96653-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96653-140">OUTPUTS</span></span>

### <span data-ttu-id="96653-141">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelavejobtargetgroupmodel</span><span class="sxs-lookup"><span data-stu-id="96653-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="96653-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96653-142">NOTES</span></span>

## <span data-ttu-id="96653-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96653-143">RELATED LINKS</span></span>
