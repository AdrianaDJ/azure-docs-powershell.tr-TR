---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataset.md
ms.openlocfilehash: d2471320a27b1af96dba6b5e2b552a01ff5b50e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279747"
---
# <span data-ttu-id="b2071-101">Set-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="b2071-101">Set-AzSynapseDataset</span></span>

## <span data-ttu-id="b2071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2071-102">SYNOPSIS</span></span>
<span data-ttu-id="b2071-103">Çalışma alanında bir veri kümesi oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="b2071-103">Creates or updates a dataset in workspace.</span></span>

## <span data-ttu-id="b2071-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b2071-104">SYNTAX</span></span>

### <span data-ttu-id="b2071-105">SetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b2071-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataset -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2071-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="b2071-106">SetByObject</span></span>
```
Set-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2071-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b2071-107">DESCRIPTION</span></span>
<span data-ttu-id="b2071-108">**Set-AzSynapseDataset** cmdlet 'i çalışma alanında var olan bir veri kümesini güncelleştirir veya</span><span class="sxs-lookup"><span data-stu-id="b2071-108">The **Set-AzSynapseDataset** cmdlet creates a dataset or updates an existing dataset in workspace.</span></span>

## <span data-ttu-id="b2071-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b2071-109">EXAMPLES</span></span>

### <span data-ttu-id="b2071-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b2071-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset -DefinitionFile "C:\\samples\\Dataset.json"
```

<span data-ttu-id="b2071-111">Bu komut, ContosoWorkspace adlı çalışma alanında ContosoDataset adlı bir veri kümesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b2071-111">This command creates a dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="b2071-112">Komut, veri kümesini Dataset.jsdosyadaki bilgilerde temel alır.</span><span class="sxs-lookup"><span data-stu-id="b2071-112">The command bases the dataset on information in the Dataset.json file.</span></span>

## <span data-ttu-id="b2071-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b2071-113">PARAMETERS</span></span>

### <span data-ttu-id="b2071-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b2071-114">-AsJob</span></span>
<span data-ttu-id="b2071-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b2071-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2071-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2071-116">-DefaultProfile</span></span>
<span data-ttu-id="b2071-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b2071-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2071-118">-Definitionfıle</span><span class="sxs-lookup"><span data-stu-id="b2071-118">-DefinitionFile</span></span>
<span data-ttu-id="b2071-119">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="b2071-119">The JSON file path.</span></span>

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

### <span data-ttu-id="b2071-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="b2071-120">-Name</span></span>
<span data-ttu-id="b2071-121">Veri kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="b2071-121">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2071-122">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="b2071-122">-WorkspaceName</span></span>
<span data-ttu-id="b2071-123">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="b2071-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b2071-124">-</span><span class="sxs-lookup"><span data-stu-id="b2071-124">-WorkspaceObject</span></span>
<span data-ttu-id="b2071-125">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="b2071-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b2071-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b2071-126">-Confirm</span></span>
<span data-ttu-id="b2071-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b2071-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2071-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2071-128">-WhatIf</span></span>
<span data-ttu-id="b2071-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b2071-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2071-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b2071-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2071-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2071-131">CommonParameters</span></span>
<span data-ttu-id="b2071-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b2071-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2071-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b2071-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2071-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b2071-134">INPUTS</span></span>

### <span data-ttu-id="b2071-135">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b2071-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b2071-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b2071-136">OUTPUTS</span></span>

### <span data-ttu-id="b2071-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="b2071-137">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="b2071-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b2071-138">NOTES</span></span>

## <span data-ttu-id="b2071-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b2071-139">RELATED LINKS</span></span>
