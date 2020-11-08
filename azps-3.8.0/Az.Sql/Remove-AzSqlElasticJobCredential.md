---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: e9d684be7119ccc0ed991f825d8c7c372e7fdc6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098670"
---
# <span data-ttu-id="68b66-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="68b66-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="68b66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b66-102">SYNOPSIS</span></span>
<span data-ttu-id="68b66-103">Esnek iş kimlik bilgilerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="68b66-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="68b66-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="68b66-104">SYNTAX</span></span>

### <span data-ttu-id="68b66-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="68b66-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b66-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="68b66-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b66-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="68b66-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68b66-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="68b66-108">DESCRIPTION</span></span>
<span data-ttu-id="68b66-109">Remove-AzSqlElasticJobCredential cmdlet 'i bir iş kimlik bilgisini kaldırır</span><span class="sxs-lookup"><span data-stu-id="68b66-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="68b66-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="68b66-110">EXAMPLES</span></span>

### <span data-ttu-id="68b66-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="68b66-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="68b66-112">İş kimlik bilgilerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="68b66-112">Removes a job credential</span></span>

## <span data-ttu-id="68b66-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="68b66-113">PARAMETERS</span></span>

### <span data-ttu-id="68b66-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="68b66-114">-AgentName</span></span>
<span data-ttu-id="68b66-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="68b66-115">The agent name</span></span>

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

### <span data-ttu-id="68b66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b66-116">-DefaultProfile</span></span>
<span data-ttu-id="68b66-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="68b66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b66-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68b66-118">-InputObject</span></span>
<span data-ttu-id="68b66-119">İş kimlik bilgileri nesnesi</span><span class="sxs-lookup"><span data-stu-id="68b66-119">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68b66-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="68b66-120">-Name</span></span>
<span data-ttu-id="68b66-121">İş kimlik bilgileri adı</span><span class="sxs-lookup"><span data-stu-id="68b66-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68b66-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b66-122">-ResourceGroupName</span></span>
<span data-ttu-id="68b66-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="68b66-123">The resource group name</span></span>

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

### <span data-ttu-id="68b66-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="68b66-124">-ResourceId</span></span>
<span data-ttu-id="68b66-125">İş kimlik bilgileri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="68b66-125">The job credential resource id</span></span>

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

### <span data-ttu-id="68b66-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68b66-126">-ServerName</span></span>
<span data-ttu-id="68b66-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="68b66-127">The server name</span></span>

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

### <span data-ttu-id="68b66-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="68b66-128">-Confirm</span></span>
<span data-ttu-id="68b66-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="68b66-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b66-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b66-130">-WhatIf</span></span>
<span data-ttu-id="68b66-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="68b66-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68b66-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="68b66-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b66-133">CommonParameters</span></span>
<span data-ttu-id="68b66-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="68b66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b66-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="68b66-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b66-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="68b66-136">INPUTS</span></span>

### <span data-ttu-id="68b66-137">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="68b66-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="68b66-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="68b66-138">OUTPUTS</span></span>

### <span data-ttu-id="68b66-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="68b66-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="68b66-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="68b66-140">NOTES</span></span>

## <span data-ttu-id="68b66-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="68b66-141">RELATED LINKS</span></span>
