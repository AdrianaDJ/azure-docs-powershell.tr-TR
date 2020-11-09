---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: ea27b23174d9555e4153dc5ef8c4d053ef5a49b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323518"
---
# <span data-ttu-id="1549c-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1549c-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="1549c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1549c-102">SYNOPSIS</span></span>
<span data-ttu-id="1549c-103">SYNAPSE Analytics SQL havuzunu sürdürür.</span><span class="sxs-lookup"><span data-stu-id="1549c-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1549c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1549c-104">SYNTAX</span></span>

### <span data-ttu-id="1549c-105">ResumeByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1549c-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1549c-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1549c-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1549c-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1549c-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1549c-108">Resumebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1549c-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1549c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1549c-109">DESCRIPTION</span></span>
<span data-ttu-id="1549c-110">**Resume-AzSynapseSqlPool** cmdlet 'ı bir Azure SYNAPSE Analytics SQL havuzunu sürdürür.</span><span class="sxs-lookup"><span data-stu-id="1549c-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1549c-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1549c-111">EXAMPLES</span></span>

### <span data-ttu-id="1549c-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1549c-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="1549c-113">Bu komut, askıya alınmış bir Azure SYNAPSE Analytics SQL havuzunu sürdürür.</span><span class="sxs-lookup"><span data-stu-id="1549c-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1549c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1549c-114">PARAMETERS</span></span>

### <span data-ttu-id="1549c-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="1549c-115">-AsJob</span></span>
<span data-ttu-id="1549c-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1549c-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1549c-117">-DefaultProfile</span></span>
<span data-ttu-id="1549c-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1549c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1549c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1549c-119">-InputObject</span></span>
<span data-ttu-id="1549c-120">Genellikle ardışık düzen aracılığıyla iletilen SQL havuzu giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1549c-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="1549c-121">-Name</span></span>
<span data-ttu-id="1549c-122">SYNAPSE SQL havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="1549c-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1549c-123">-PassThru</span></span>
<span data-ttu-id="1549c-124">Bu cmdlet varsayılan olarak bir nesne döndürmez.</span><span class="sxs-lookup"><span data-stu-id="1549c-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1549c-125">Bu anahtar belirtilmişse, başarılı olduğunda doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="1549c-125">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1549c-126">-ResourceGroupName</span></span>
<span data-ttu-id="1549c-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1549c-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1549c-128">-ResourceId</span></span>
<span data-ttu-id="1549c-129">SYNAPSE SQL havuzunun kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1549c-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-130">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="1549c-130">-WorkspaceName</span></span>
<span data-ttu-id="1549c-131">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="1549c-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-132">-</span><span class="sxs-lookup"><span data-stu-id="1549c-132">-WorkspaceObject</span></span>
<span data-ttu-id="1549c-133">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="1549c-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="1549c-134">-Confirm</span></span>
<span data-ttu-id="1549c-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1549c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1549c-136">-WhatIf</span></span>
<span data-ttu-id="1549c-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1549c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1549c-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1549c-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1549c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1549c-139">CommonParameters</span></span>
<span data-ttu-id="1549c-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1549c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1549c-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1549c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1549c-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1549c-142">INPUTS</span></span>

### <span data-ttu-id="1549c-143">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1549c-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1549c-144">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1549c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1549c-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1549c-145">OUTPUTS</span></span>

### <span data-ttu-id="1549c-146">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1549c-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1549c-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1549c-147">NOTES</span></span>

## <span data-ttu-id="1549c-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1549c-148">RELATED LINKS</span></span>
