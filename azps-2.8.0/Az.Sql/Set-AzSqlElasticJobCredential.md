---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: b3e3aa1414b24324278f4191fd53a28a75d0cfab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933709"
---
# <span data-ttu-id="c4a7d-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="c4a7d-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="c4a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a7d-103">İş kimlik bilgilerini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c4a7d-103">Updates a job credential</span></span>

## <span data-ttu-id="c4a7d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c4a7d-104">SYNTAX</span></span>

### <span data-ttu-id="c4a7d-105">DefaultSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c4a7d-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4a7d-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c4a7d-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4a7d-107">Resourceıdset</span><span class="sxs-lookup"><span data-stu-id="c4a7d-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a7d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c4a7d-108">DESCRIPTION</span></span>
<span data-ttu-id="c4a7d-109">Set-AzSqlElasticJobCredential cmdlet 'i iş kimlik bilgilerini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c4a7d-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="c4a7d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c4a7d-110">EXAMPLES</span></span>

### <span data-ttu-id="c4a7d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c4a7d-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="c4a7d-112">İş kimlik bilgilerini güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="c4a7d-112">Updates a job credential</span></span>

## <span data-ttu-id="c4a7d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c4a7d-113">PARAMETERS</span></span>

### <span data-ttu-id="c4a7d-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c4a7d-114">-AgentName</span></span>
<span data-ttu-id="c4a7d-115">Aracı adı</span><span class="sxs-lookup"><span data-stu-id="c4a7d-115">The agent name</span></span>

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

### <span data-ttu-id="c4a7d-116">-Credential</span><span class="sxs-lookup"><span data-stu-id="c4a7d-116">-Credential</span></span>
<span data-ttu-id="c4a7d-117">Kimlik bilgisi</span><span class="sxs-lookup"><span data-stu-id="c4a7d-117">The credential</span></span>

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

### <span data-ttu-id="c4a7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a7d-118">-DefaultProfile</span></span>
<span data-ttu-id="c4a7d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c4a7d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a7d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4a7d-120">-InputObject</span></span>
<span data-ttu-id="c4a7d-121">İş kimlik bilgileri nesnesi</span><span class="sxs-lookup"><span data-stu-id="c4a7d-121">The job credential object</span></span>

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

### <span data-ttu-id="c4a7d-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c4a7d-122">-Name</span></span>
<span data-ttu-id="c4a7d-123">İş kimlik bilgileri adı</span><span class="sxs-lookup"><span data-stu-id="c4a7d-123">The job credential name</span></span>

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

### <span data-ttu-id="c4a7d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a7d-124">-ResourceGroupName</span></span>
<span data-ttu-id="c4a7d-125">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c4a7d-125">The resource group name</span></span>

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

### <span data-ttu-id="c4a7d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c4a7d-126">-ResourceId</span></span>
<span data-ttu-id="c4a7d-127">İş kimlik bilgileri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c4a7d-127">The job credential resource id</span></span>

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

### <span data-ttu-id="c4a7d-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c4a7d-128">-ServerName</span></span>
<span data-ttu-id="c4a7d-129">Sunucu adı</span><span class="sxs-lookup"><span data-stu-id="c4a7d-129">The server name</span></span>

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

### <span data-ttu-id="c4a7d-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c4a7d-130">-Confirm</span></span>
<span data-ttu-id="c4a7d-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c4a7d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a7d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a7d-132">-WhatIf</span></span>
<span data-ttu-id="c4a7d-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c4a7d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a7d-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c4a7d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a7d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a7d-135">CommonParameters</span></span>
<span data-ttu-id="c4a7d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c4a7d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a7d-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c4a7d-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a7d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c4a7d-138">INPUTS</span></span>

### <span data-ttu-id="c4a7d-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="c4a7d-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="c4a7d-140">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="c4a7d-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="c4a7d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c4a7d-141">OUTPUTS</span></span>

### <span data-ttu-id="c4a7d-142">Microsoft. Azure. Commands. Sql. Elavejobs. model. Azuresqlelakjobcredentialmodel</span><span class="sxs-lookup"><span data-stu-id="c4a7d-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="c4a7d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c4a7d-143">NOTES</span></span>

## <span data-ttu-id="c4a7d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c4a7d-144">RELATED LINKS</span></span>
