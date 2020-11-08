---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleDefinition.md
ms.openlocfilehash: f2ac7efad3c08a351e515eccbe519306a89f06a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277963"
---
# <span data-ttu-id="49278-101">Get-AzSynapseRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="49278-101">Get-AzSynapseRoleDefinition</span></span>

## <span data-ttu-id="49278-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49278-102">SYNOPSIS</span></span>
<span data-ttu-id="49278-103">SYNAPSE Analytics rol tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="49278-103">Gets a Synapse Analytics role definition.</span></span>

## <span data-ttu-id="49278-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="49278-104">SYNTAX</span></span>

### <span data-ttu-id="49278-105">GetByWorkspaceNameAndIdParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="49278-105">GetByWorkspaceNameAndIdParameterSet (Default)</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Id <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49278-106">GetByWorkspaceNameAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="49278-106">GetByWorkspaceNameAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49278-107">Getbyıo Nesnetandidparameterset</span><span class="sxs-lookup"><span data-stu-id="49278-107">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> -Id <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49278-108">Getbyıo Nesnetandnameparameterset</span><span class="sxs-lookup"><span data-stu-id="49278-108">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleDefinition -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49278-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="49278-109">DESCRIPTION</span></span>
<span data-ttu-id="49278-110">**Get-AzSynapseRoleDefinition** cmdlet 'ı bir Azure SYNAPSE Analytics rol tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="49278-110">The **Get-AzSynapseRoleDefinition** cmdlet gets an Azure Synapse Analytics Role Definition.</span></span>
<span data-ttu-id="49278-111">Rol adı veya rol kimliği belirtmezseniz, bu cmdlet tüm rol tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="49278-111">If you do not specify a role name or a role Id, this cmdlet gets all role definitions.</span></span>

## <span data-ttu-id="49278-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="49278-112">EXAMPLES</span></span>

### <span data-ttu-id="49278-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="49278-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="49278-114">Bu komut, çalışma alanı altındaki tüm rol tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="49278-114">This command gets all role definitions under a workspace.</span></span>

### <span data-ttu-id="49278-115">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="49278-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseRoleDefinition -WorkspaceName ContosoWorkspace -Name ContosoRole
```

<span data-ttu-id="49278-116">Bu komut, ad alanı olan ContosoWorkspace 'in altındaki rol tanımını ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="49278-116">This command gets the role definition under workspace ContosoWorkspace with name ContosoRole.</span></span>

### <span data-ttu-id="49278-117">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="49278-117">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleDefinition
```

<span data-ttu-id="49278-118">Bu komut, ardışık düzen aracılığıyla tüm rol tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="49278-118">This command gets all role definitions under a workspace through pipeline.</span></span>

## <span data-ttu-id="49278-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="49278-119">PARAMETERS</span></span>

### <span data-ttu-id="49278-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49278-120">-DefaultProfile</span></span>
<span data-ttu-id="49278-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="49278-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49278-122">-ID</span><span class="sxs-lookup"><span data-stu-id="49278-122">-Id</span></span>
<span data-ttu-id="49278-123">Sorumluya atanmış olan rolün kimliği.</span><span class="sxs-lookup"><span data-stu-id="49278-123">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49278-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="49278-124">-Name</span></span>
<span data-ttu-id="49278-125">Sorumluya atanmış rolün adı.</span><span class="sxs-lookup"><span data-stu-id="49278-125">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49278-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="49278-126">-WorkspaceName</span></span>
<span data-ttu-id="49278-127">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="49278-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49278-128">-</span><span class="sxs-lookup"><span data-stu-id="49278-128">-WorkspaceObject</span></span>
<span data-ttu-id="49278-129">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="49278-129">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49278-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49278-130">CommonParameters</span></span>
<span data-ttu-id="49278-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="49278-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49278-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="49278-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49278-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="49278-133">INPUTS</span></span>

### <span data-ttu-id="49278-134">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="49278-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="49278-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="49278-135">OUTPUTS</span></span>

### <span data-ttu-id="49278-136">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseRole</span><span class="sxs-lookup"><span data-stu-id="49278-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseRole</span></span>

## <span data-ttu-id="49278-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="49278-137">NOTES</span></span>

## <span data-ttu-id="49278-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="49278-138">RELATED LINKS</span></span>
