---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1986a773a61f9c0ac1bd9a30992db3843b97e438
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933543"
---
# <span data-ttu-id="3fb1a-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="3fb1a-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="3fb1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fb1a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fb1a-103">Esnek iş kimlik bilgilerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="3fb1a-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="3fb1a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3fb1a-104">SYNTAX</span></span>

### <span data-ttu-id="3fb1a-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3fb1a-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb1a-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="3fb1a-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fb1a-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="3fb1a-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fb1a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3fb1a-108">DESCRIPTION</span></span>
<span data-ttu-id="3fb1a-109">Remove-AzSqlElasticJobCredential cmdlet 'i bir iş kimlik bilgisini kaldırır</span><span class="sxs-lookup"><span data-stu-id="3fb1a-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="3fb1a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3fb1a-110">EXAMPLES</span></span>

### <span data-ttu-id="3fb1a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3fb1a-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="3fb1a-112">İş kimlik bilgilerini kaldırır</span><span class="sxs-lookup"><span data-stu-id="3fb1a-112">Removes a job credential</span></span>

## <span data-ttu-id="3fb1a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3fb1a-113">PARAMETERS</span></span>

### <span data-ttu-id="3fb1a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3fb1a-114">-AgentName</span></span>
<span data-ttu-id="3fb1a-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="3fb1a-115">The agent name</span></span>

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

### <span data-ttu-id="3fb1a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fb1a-116">-DefaultProfile</span></span>
<span data-ttu-id="3fb1a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3fb1a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fb1a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fb1a-118">-InputObject</span></span>
<span data-ttu-id="3fb1a-119">İş kimlik bilgileri nesnesi</span><span class="sxs-lookup"><span data-stu-id="3fb1a-119">The job credential object</span></span>

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

### <span data-ttu-id="3fb1a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3fb1a-120">-Name</span></span>
<span data-ttu-id="3fb1a-121">İş kimlik bilgileri adı</span><span class="sxs-lookup"><span data-stu-id="3fb1a-121">The job credential name</span></span>

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

### <span data-ttu-id="3fb1a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fb1a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3fb1a-123">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="3fb1a-123">The resource group name</span></span>

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

### <span data-ttu-id="3fb1a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3fb1a-124">-ResourceId</span></span>
<span data-ttu-id="3fb1a-125">İş kimlik bilgileri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3fb1a-125">The job credential resource id</span></span>

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

### <span data-ttu-id="3fb1a-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3fb1a-126">-ServerName</span></span>
<span data-ttu-id="3fb1a-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="3fb1a-127">The server name</span></span>

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

### <span data-ttu-id="3fb1a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="3fb1a-128">-Confirm</span></span>
<span data-ttu-id="3fb1a-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3fb1a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fb1a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fb1a-130">-WhatIf</span></span>
<span data-ttu-id="3fb1a-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3fb1a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fb1a-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3fb1a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fb1a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fb1a-133">CommonParameters</span></span>
<span data-ttu-id="3fb1a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3fb1a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fb1a-135">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3fb1a-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fb1a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3fb1a-136">INPUTS</span></span>

### <span data-ttu-id="3fb1a-137">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="3fb1a-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="3fb1a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3fb1a-138">OUTPUTS</span></span>

### <span data-ttu-id="3fb1a-139">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="3fb1a-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="3fb1a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3fb1a-140">NOTES</span></span>

## <span data-ttu-id="3fb1a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3fb1a-141">RELATED LINKS</span></span>
