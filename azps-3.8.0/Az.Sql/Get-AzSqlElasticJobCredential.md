---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938444"
---
# <span data-ttu-id="b14fc-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="b14fc-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="b14fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b14fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b14fc-103">Bir veya daha fazla kimlik bilgisini alır</span><span class="sxs-lookup"><span data-stu-id="b14fc-103">Gets one or more credentials</span></span>

## <span data-ttu-id="b14fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b14fc-104">SYNTAX</span></span>

### <span data-ttu-id="b14fc-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b14fc-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b14fc-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b14fc-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b14fc-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="b14fc-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b14fc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b14fc-108">DESCRIPTION</span></span>
<span data-ttu-id="b14fc-109">Get-AzSqlElasticJobCredential cmdlet 'i bir veya daha fazla iş kimlik bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="b14fc-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="b14fc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b14fc-110">EXAMPLES</span></span>

### <span data-ttu-id="b14fc-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b14fc-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="b14fc-112">İş kimlik bilgilerini alır</span><span class="sxs-lookup"><span data-stu-id="b14fc-112">Gets a job credential</span></span>

## <span data-ttu-id="b14fc-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b14fc-113">PARAMETERS</span></span>

### <span data-ttu-id="b14fc-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b14fc-114">-AgentName</span></span>
<span data-ttu-id="b14fc-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="b14fc-115">The agent name</span></span>

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

### <span data-ttu-id="b14fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b14fc-116">-DefaultProfile</span></span>
<span data-ttu-id="b14fc-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b14fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b14fc-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b14fc-118">-Name</span></span>
<span data-ttu-id="b14fc-119">İş kimlik bilgileri adı</span><span class="sxs-lookup"><span data-stu-id="b14fc-119">The job credential name</span></span>

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

### <span data-ttu-id="b14fc-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b14fc-120">-ParentObject</span></span>
<span data-ttu-id="b14fc-121">Aracı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b14fc-121">The agent object</span></span>

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

### <span data-ttu-id="b14fc-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="b14fc-122">-ParentResourceId</span></span>
<span data-ttu-id="b14fc-123">Aracı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="b14fc-123">The agent resource id</span></span>

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

### <span data-ttu-id="b14fc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b14fc-124">-ResourceGroupName</span></span>
<span data-ttu-id="b14fc-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b14fc-125">The resource group name</span></span>

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

### <span data-ttu-id="b14fc-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b14fc-126">-ServerName</span></span>
<span data-ttu-id="b14fc-127">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="b14fc-127">The server name</span></span>

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

### <span data-ttu-id="b14fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b14fc-128">CommonParameters</span></span>
<span data-ttu-id="b14fc-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b14fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b14fc-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b14fc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b14fc-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b14fc-131">INPUTS</span></span>

### <span data-ttu-id="b14fc-132">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelayapışjobagentmodel</span><span class="sxs-lookup"><span data-stu-id="b14fc-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b14fc-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b14fc-133">OUTPUTS</span></span>

### <span data-ttu-id="b14fc-134">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="b14fc-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="b14fc-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b14fc-135">NOTES</span></span>

## <span data-ttu-id="b14fc-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b14fc-136">RELATED LINKS</span></span>
