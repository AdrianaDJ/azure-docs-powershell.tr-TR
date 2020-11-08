---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104257"
---
# <span data-ttu-id="b669f-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="b669f-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="b669f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b669f-102">SYNOPSIS</span></span>
<span data-ttu-id="b669f-103">Yeni iş kimlik bilgileri oluşturur</span><span class="sxs-lookup"><span data-stu-id="b669f-103">Creates a new job credential</span></span>

## <span data-ttu-id="b669f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b669f-104">SYNTAX</span></span>

### <span data-ttu-id="b669f-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b669f-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b669f-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b669f-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b669f-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b669f-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b669f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b669f-108">DESCRIPTION</span></span>
<span data-ttu-id="b669f-109">New-AzSqlElasticJobCredential cmdlet 'i yeni bir iş kimlik bilgisi oluşturur</span><span class="sxs-lookup"><span data-stu-id="b669f-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="b669f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b669f-110">EXAMPLES</span></span>

### <span data-ttu-id="b669f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b669f-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="b669f-112">Yeni iş kimlik bilgileri oluşturur</span><span class="sxs-lookup"><span data-stu-id="b669f-112">Creates a new job credential</span></span>

## <span data-ttu-id="b669f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b669f-113">PARAMETERS</span></span>

### <span data-ttu-id="b669f-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b669f-114">-AgentName</span></span>
<span data-ttu-id="b669f-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="b669f-115">The agent name</span></span>

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

### <span data-ttu-id="b669f-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="b669f-116">-Credential</span></span>
<span data-ttu-id="b669f-117">Kimlik bilgisi</span><span class="sxs-lookup"><span data-stu-id="b669f-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b669f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b669f-118">-DefaultProfile</span></span>
<span data-ttu-id="b669f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b669f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b669f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b669f-120">-Name</span></span>
<span data-ttu-id="b669f-121">İş kimlik bilgileri adı</span><span class="sxs-lookup"><span data-stu-id="b669f-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b669f-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b669f-122">-ParentObject</span></span>
<span data-ttu-id="b669f-123">Aracı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b669f-123">The agent object</span></span>

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

### <span data-ttu-id="b669f-124">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="b669f-124">-ParentResourceId</span></span>
<span data-ttu-id="b669f-125">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b669f-125">The agent resource id</span></span>

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

### <span data-ttu-id="b669f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b669f-126">-ResourceGroupName</span></span>
<span data-ttu-id="b669f-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b669f-127">The resource group name</span></span>

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

### <span data-ttu-id="b669f-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b669f-128">-ServerName</span></span>
<span data-ttu-id="b669f-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="b669f-129">The server name</span></span>

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

### <span data-ttu-id="b669f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="b669f-130">-Confirm</span></span>
<span data-ttu-id="b669f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b669f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b669f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b669f-132">-WhatIf</span></span>
<span data-ttu-id="b669f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b669f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b669f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b669f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b669f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b669f-135">CommonParameters</span></span>
<span data-ttu-id="b669f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b669f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b669f-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b669f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b669f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b669f-138">INPUTS</span></span>

### <span data-ttu-id="b669f-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="b669f-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="b669f-140">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="b669f-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b669f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b669f-141">OUTPUTS</span></span>

### <span data-ttu-id="b669f-142">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="b669f-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="b669f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b669f-143">NOTES</span></span>

## <span data-ttu-id="b669f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b669f-144">RELATED LINKS</span></span>
