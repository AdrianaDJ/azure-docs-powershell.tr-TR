---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268938"
---
# <span data-ttu-id="b69ca-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="b69ca-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="b69ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b69ca-102">SYNOPSIS</span></span>
<span data-ttu-id="b69ca-103">Çalışma alanında veri akışı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b69ca-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="b69ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b69ca-104">SYNTAX</span></span>

### <span data-ttu-id="b69ca-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b69ca-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b69ca-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="b69ca-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b69ca-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b69ca-107">DESCRIPTION</span></span>
<span data-ttu-id="b69ca-108">**Set-AzSynapseDataFlow** cmdlet 'i veri akışı oluşturur veya çalışma alanında var olan bir veri akışını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b69ca-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="b69ca-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b69ca-109">EXAMPLES</span></span>

### <span data-ttu-id="b69ca-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b69ca-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="b69ca-111">Bu komut, ContosoWorkspace adlı çalışma alanında ContosoDataFlow adlı bir veri akışı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b69ca-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="b69ca-112">Komut, veri akışını DataFlow.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="b69ca-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="b69ca-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b69ca-113">PARAMETERS</span></span>

### <span data-ttu-id="b69ca-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b69ca-114">-AsJob</span></span>
<span data-ttu-id="b69ca-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b69ca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b69ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b69ca-116">-DefaultProfile</span></span>
<span data-ttu-id="b69ca-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b69ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b69ca-118">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="b69ca-118">-DefinitionFile</span></span>
<span data-ttu-id="b69ca-119">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="b69ca-119">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b69ca-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b69ca-120">-Name</span></span>
<span data-ttu-id="b69ca-121">Veri akışı adı.</span><span class="sxs-lookup"><span data-stu-id="b69ca-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b69ca-122">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="b69ca-122">-WorkspaceName</span></span>
<span data-ttu-id="b69ca-123">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="b69ca-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b69ca-124">-</span><span class="sxs-lookup"><span data-stu-id="b69ca-124">-WorkspaceObject</span></span>
<span data-ttu-id="b69ca-125">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="b69ca-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b69ca-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b69ca-126">-Confirm</span></span>
<span data-ttu-id="b69ca-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b69ca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b69ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b69ca-128">-WhatIf</span></span>
<span data-ttu-id="b69ca-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b69ca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b69ca-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b69ca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b69ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b69ca-131">CommonParameters</span></span>
<span data-ttu-id="b69ca-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b69ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b69ca-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b69ca-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b69ca-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b69ca-134">INPUTS</span></span>

### <span data-ttu-id="b69ca-135">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b69ca-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b69ca-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b69ca-136">OUTPUTS</span></span>

### <span data-ttu-id="b69ca-137">Microsoft.Azure.Commands.Synapse.Models.PSDAtaakışkaynağı</span><span class="sxs-lookup"><span data-stu-id="b69ca-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="b69ca-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b69ca-138">NOTES</span></span>

## <span data-ttu-id="b69ca-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b69ca-139">RELATED LINKS</span></span>
