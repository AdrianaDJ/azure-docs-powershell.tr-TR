---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273778"
---
# <span data-ttu-id="d2e31-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="d2e31-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="d2e31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e31-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e31-103">Çalışma alanındaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d2e31-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="d2e31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2e31-104">SYNTAX</span></span>

### <span data-ttu-id="d2e31-105">GetByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d2e31-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2e31-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="d2e31-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e31-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2e31-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e31-108">**Get-AzSynapseDataset** cmdlet 'i çalışma alanındaki veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d2e31-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="d2e31-109">Bir veri kümesinin adını belirtirseniz, bu cmdlet bu veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d2e31-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="d2e31-110">Bir ad belirtmezseniz, bu cmdlet çalışma alanındaki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d2e31-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="d2e31-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2e31-111">EXAMPLES</span></span>

### <span data-ttu-id="d2e31-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d2e31-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d2e31-113">Bu komut, ContosoWorkspace adındaki çalışma alanındaki tüm veri kümeleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d2e31-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d2e31-114">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d2e31-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="d2e31-115">Bu komut, ContosoWorkspace adlı çalışma alanında ContosoDataset adlı veri kümesi hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="d2e31-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="d2e31-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2e31-116">PARAMETERS</span></span>

### <span data-ttu-id="d2e31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e31-117">-DefaultProfile</span></span>
<span data-ttu-id="d2e31-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d2e31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e31-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="d2e31-119">-Name</span></span>
<span data-ttu-id="d2e31-120">Veri kümesi adı.</span><span class="sxs-lookup"><span data-stu-id="d2e31-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e31-121">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d2e31-121">-WorkspaceName</span></span>
<span data-ttu-id="d2e31-122">SYNAPSE çalışma alanının adı.</span><span class="sxs-lookup"><span data-stu-id="d2e31-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e31-123">-</span><span class="sxs-lookup"><span data-stu-id="d2e31-123">-WorkspaceObject</span></span>
<span data-ttu-id="d2e31-124">genellikle ardışık düzen aracılığıyla geçen çalışma alanı giriş nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="d2e31-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e31-125">CommonParameters</span></span>
<span data-ttu-id="d2e31-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2e31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e31-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d2e31-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e31-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2e31-128">INPUTS</span></span>

### <span data-ttu-id="d2e31-129">Microsoft. Azure. Commands. SYNAPSE. modeller. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2e31-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d2e31-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2e31-130">OUTPUTS</span></span>

### <span data-ttu-id="d2e31-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="d2e31-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="d2e31-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2e31-132">NOTES</span></span>

## <span data-ttu-id="d2e31-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2e31-133">RELATED LINKS</span></span>
