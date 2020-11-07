---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 13878e7ca0ea4ed0b03734f0395c9f819e04d7f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933633"
---
# <span data-ttu-id="e2128-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="e2128-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="e2128-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2128-102">SYNOPSIS</span></span>
<span data-ttu-id="e2128-103">Bir veya daha fazla kimlik bilgisini alır</span><span class="sxs-lookup"><span data-stu-id="e2128-103">Gets one or more credentials</span></span>

## <span data-ttu-id="e2128-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e2128-104">SYNTAX</span></span>

### <span data-ttu-id="e2128-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e2128-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2128-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e2128-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2128-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="e2128-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2128-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e2128-108">DESCRIPTION</span></span>
<span data-ttu-id="e2128-109">Get-AzSqlElasticJobCredential cmdlet 'i bir veya daha fazla iş kimlik bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="e2128-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="e2128-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e2128-110">EXAMPLES</span></span>

### <span data-ttu-id="e2128-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e2128-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="e2128-112">İş kimlik bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="e2128-112">Gets a job credential</span></span>

## <span data-ttu-id="e2128-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e2128-113">PARAMETERS</span></span>

### <span data-ttu-id="e2128-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e2128-114">-AgentName</span></span>
<span data-ttu-id="e2128-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="e2128-115">The agent name</span></span>

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

### <span data-ttu-id="e2128-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2128-116">-DefaultProfile</span></span>
<span data-ttu-id="e2128-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e2128-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2128-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e2128-118">-Name</span></span>
<span data-ttu-id="e2128-119">İş kimlik bilgileri adı</span><span class="sxs-lookup"><span data-stu-id="e2128-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2128-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e2128-120">-ParentObject</span></span>
<span data-ttu-id="e2128-121">Aracı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e2128-121">The agent object</span></span>

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

### <span data-ttu-id="e2128-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="e2128-122">-ParentResourceId</span></span>
<span data-ttu-id="e2128-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e2128-123">The agent resource id</span></span>

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

### <span data-ttu-id="e2128-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2128-124">-ResourceGroupName</span></span>
<span data-ttu-id="e2128-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e2128-125">The resource group name</span></span>

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

### <span data-ttu-id="e2128-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e2128-126">-ServerName</span></span>
<span data-ttu-id="e2128-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="e2128-127">The server name</span></span>

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

### <span data-ttu-id="e2128-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2128-128">CommonParameters</span></span>
<span data-ttu-id="e2128-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e2128-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2128-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e2128-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2128-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e2128-131">INPUTS</span></span>

### <span data-ttu-id="e2128-132">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="e2128-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e2128-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e2128-133">OUTPUTS</span></span>

### <span data-ttu-id="e2128-134">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="e2128-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="e2128-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e2128-135">NOTES</span></span>

## <span data-ttu-id="e2128-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e2128-136">RELATED LINKS</span></span>
