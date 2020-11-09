---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322310"
---
# <span data-ttu-id="314e1-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="314e1-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="314e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="314e1-102">SYNOPSIS</span></span>
<span data-ttu-id="314e1-103">İş kimlik bilgilerini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="314e1-103">Updates a job credential</span></span>

## <span data-ttu-id="314e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="314e1-104">SYNTAX</span></span>

### <span data-ttu-id="314e1-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="314e1-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="314e1-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="314e1-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="314e1-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="314e1-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="314e1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="314e1-108">DESCRIPTION</span></span>
<span data-ttu-id="314e1-109">Set-AzSqlElasticJobCredential cmdlet 'i iş kimlik bilgilerini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="314e1-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="314e1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="314e1-110">EXAMPLES</span></span>

### <span data-ttu-id="314e1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="314e1-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="314e1-112">İş kimlik bilgilerini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="314e1-112">Updates a job credential</span></span>

## <span data-ttu-id="314e1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="314e1-113">PARAMETERS</span></span>

### <span data-ttu-id="314e1-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="314e1-114">-AgentName</span></span>
<span data-ttu-id="314e1-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="314e1-115">The agent name</span></span>

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

### <span data-ttu-id="314e1-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="314e1-116">-Credential</span></span>
<span data-ttu-id="314e1-117">Kimlik bilgisi</span><span class="sxs-lookup"><span data-stu-id="314e1-117">The credential</span></span>

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

### <span data-ttu-id="314e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314e1-118">-DefaultProfile</span></span>
<span data-ttu-id="314e1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="314e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="314e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="314e1-120">-InputObject</span></span>
<span data-ttu-id="314e1-121">İş kimlik bilgileri nesnesi</span><span class="sxs-lookup"><span data-stu-id="314e1-121">The job credential object</span></span>

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

### <span data-ttu-id="314e1-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="314e1-122">-Name</span></span>
<span data-ttu-id="314e1-123">İş kimlik bilgileri adı</span><span class="sxs-lookup"><span data-stu-id="314e1-123">The job credential name</span></span>

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

### <span data-ttu-id="314e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="314e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="314e1-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="314e1-125">The resource group name</span></span>

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

### <span data-ttu-id="314e1-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="314e1-126">-ResourceId</span></span>
<span data-ttu-id="314e1-127">İş kimlik bilgileri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="314e1-127">The job credential resource id</span></span>

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

### <span data-ttu-id="314e1-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="314e1-128">-ServerName</span></span>
<span data-ttu-id="314e1-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="314e1-129">The server name</span></span>

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

### <span data-ttu-id="314e1-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="314e1-130">-Confirm</span></span>
<span data-ttu-id="314e1-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="314e1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="314e1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="314e1-132">-WhatIf</span></span>
<span data-ttu-id="314e1-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="314e1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="314e1-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="314e1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="314e1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314e1-135">CommonParameters</span></span>
<span data-ttu-id="314e1-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="314e1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314e1-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="314e1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314e1-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="314e1-138">INPUTS</span></span>

### <span data-ttu-id="314e1-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="314e1-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="314e1-140">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="314e1-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="314e1-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="314e1-141">OUTPUTS</span></span>

### <span data-ttu-id="314e1-142">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="314e1-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="314e1-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="314e1-143">NOTES</span></span>

## <span data-ttu-id="314e1-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="314e1-144">RELATED LINKS</span></span>
